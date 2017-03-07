Step 1
======
Get an Amazon Alexa device and play with it

Try a tutorial
==============
https://developer.amazon.com/alexa-skills-kit/alexa-skill-quick-start-tutorial

1. Join Amazon AWS https://console.aws.amazon.com/console/home
2. Go to Lambda
3. Choose a region, choose only US East (N. Virginia) or EU (Ireland)!
4. use alexa-skills-kit-color-expert-python blueprint
5. create a custom handler role (to run it under)
6. create the function
7. copy the arn (arn:aws:lambda:eu-west-1:918093719737:function:myColourSkill)

8. sign in the the Developer Portal https://developer.amazon.com/login.html
9. Alexa tab
10. Skills Kit -> get started
11. Add a skill with a name and an invocation. Users will say, "open *invocation*"
12. give it an intent schema

{
  "intents": [
    {
      "intent": "MyColorIsIntent",
      "slots": [
        {
          "name": "Color",
          "type": "LIST_OF_COLORS"
        }
      ]
    },
    {
      "intent": "WhatsMyColorIntent"
    },
    {
      "intent": "AMAZON.HelpIntent"
    }
  ]
}

13. add a slot type LIST_OF_COLORS

green
red
blue
orange
gold
silver
yellow
black
white

14. Give it some sample utterances. To be used as examples

WhatsMyColorIntent what's my favorite color
WhatsMyColorIntent what is my favorite color
WhatsMyColorIntent what's my color
WhatsMyColorIntent what is my color
WhatsMyColorIntent my color
WhatsMyColorIntent my favorite color
WhatsMyColorIntent get my color
WhatsMyColorIntent get my favorite color
WhatsMyColorIntent give me my favorite color
WhatsMyColorIntent give me my color
WhatsMyColorIntent what my color is
WhatsMyColorIntent what my favorite color is
WhatsMyColorIntent yes
WhatsMyColorIntent yup
WhatsMyColorIntent sure
WhatsMyColorIntent yes please
MyColorIsIntent my favorite color is {Color}

15. Specify our ARN as the endpoint
