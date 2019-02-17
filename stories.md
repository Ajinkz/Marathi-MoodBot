## mast path               <!-- name of the story - just for debugging -->
* namaskar
  - utter_namaskar
* mast               <!-- user utterance -->
  - utter_mast

## sad path 1               <!-- this is already the start of the next story -->
* namaskar
  - utter_namaskar             <!-- action of the bot to execute -->
* udas
  - utter_khus_ho
  - utter_madat_upyogi_padli_ka
* hokar
  - utter_mast

## sad path 2
* namaskar
  - utter_namaskar
* udas
  - utter_khus_ho
  - utter_madat_upyogi_padli_ka
* nakar
  - utter_alvida

## say alvida
* alvida
  - utter_alvida

