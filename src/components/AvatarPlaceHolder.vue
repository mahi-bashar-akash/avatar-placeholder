<template>
  <div :class="size + ' ' + backgroundColor + ' ' + textColor + ' ' + radius + ` avatar `">
    {{ nameChange() }}
  </div>
</template>

<script>
export default {
  name: 'AvatarPlaceHolder',
  props: {
    size: {
      type: String,
      default: 'size-32',
    },
    backgroundColor: {
      type: String,
      default: 'bg-blue',
    },
    textColor: {
      type: String,
      default: 'text-white',
    },
    radius: {
      type: String,
      default: 'rounded-none',
    },
    name: {
      type: String,
      required: true,
    }
  },
  watch: {},
  data() {
    return {}
  },
  mounted() {

  },
  methods: {

    nameChange() {

      // declare name into variable
      let name = this.name

      // take 3 words of name as first and last index name
      let firstName, secondName, thirdName, firstWord, lastWord;

      // words split as words
      const words = name.split(" ")

      // when third name provided
      if (thirdName !== '' || undefined) {

        // word takes 0 as first name and third is last name of index
        firstName = words[0];
        thirdName = words[2];

        // provided for loops for first name
        for (let i = 0; i < firstName.length; i++) {
          firstWord = firstName.split('')[0]
        }

        // provided for loops for third name
        for (let i = 0; i < thirdName.length; i++) {
          lastWord = thirdName.split('')[0]
        }

        // return first word and last word
        return firstWord + lastWord;

      } else if (secondName !== '' || undefined) {

        // word takes 0 as first name and second is last name of index
        firstName = words[0];
        secondName = words[1];

        // provided for loops for first name
        for (let i = 0; i < firstName.length; i++) {
          firstWord = firstName.split('')[0]
        }

        // provided for loops for second name
        for (let i = 0; i < secondName.length; i++) {
          lastWord = secondName.split('')[0]
        }

        // return first word and last word
        return firstWord + lastWord;

      } else {

        // word takes 0 as first name
        firstName = words[0];

        // provided for loops for first name
        for (let i = 0; i < firstName.length; i++) {
          firstWord = firstName.split('')[0]
        }

        // default first word
        return firstWord;

      }

    }

  }
}
</script>

<style>
  @import '../css/style.css';
</style>