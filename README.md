# cough classifier: teaching ai to listen

## tldr

building an ml model that can tell what's wrong with you just by hearing you cough. think shazam but for your lungs.

---

## the problem

respiratory diseases are everywhere. covid, tb, asthma, pneumonia - they all make you cough differently but doctors can't always tell just by listening. 

current diagnosis is:
- expensive (imaging, lab tests)
- slow (waiting for appointments, results)
- inaccessible (not everyone has a pulmonologist nearby)
- subjective (depends on doctor's experience)

your cough literally contains data about what's going on in your lungs. we're just not using it.

---

## why this actually works

### your phone is already a medical device

everyone has a microphone in their pocket. no special equipment needed. just record and analyze.

### different diseases = different sounds

- dry cough vs wet cough
- short vs long
- frequency patterns
- intensity changes

ai can pick up on patterns humans miss.

### real impact

- screen people before they even see a doctor
- monitor chronic conditions from home
- catch outbreaks early
- help underserved communities

---

## how ml fits in

### the pipeline

1. collect cough recordings (with diagnoses)
2. turn audio into features computers understand
3. train model to recognize patterns
4. test on new coughs
5. deploy as app

### tech stack ideas

**audio processing:**
- spectrograms (visual representation of sound)
- mfccs (audio fingerprinting)
- noise filtering

**models:**
- cnns for pattern recognition
- transformer models (like gpt but for audio)
- transfer learning from pretrained audio models

**what we're classifying:**
- healthy cough
- covid
- asthma/copd
- pneumonia
- tb

### challenges (keeping it real)

- privacy is huge - health data is sensitive
- rare diseases = less training data
- background noise messes things up
- everyone coughs differently (age, gender, body type)
- needs actual clinical testing, not just good accuracy scores
- might need fda approval

### important notes

this isn't replacing doctors. it's a screening tool. think of it like a smart thermometer - helpful data point, not a diagnosis.

---

## what we're building

- robust ml pipeline for cough audio
- clinically useful accuracy
- works across different demographics  
- proof-of-concept app
- fully documented for future research

---

## references

1. **sharma et al. (2020).** "coswara — a database of breathing, cough, and voice sounds for covid-19 diagnosis." interspeech 2020.
   - crowdsourced covid cough dataset, proves the concept works

2. **pramono et al. (2017).** "automatic adventitious respiratory sound analysis: a systematic review." plos one.
   - comprehensive review of how to analyze lung sounds with computers

---

## next moves

- [ ] find datasets
- [ ] build preprocessing pipeline  
- [ ] train baseline model
- [ ] validate performance
- [ ] test with real users
- [ ] figure out regulatory stuff
