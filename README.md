# Vocal Synthesis
Author: Chenzhi Sun
* **README.md**: Explains the Vocal_Synthesis program
* **logatomes.wav**: The set of logatomes in *wav* format
* **logatomes.TextGrid**: The set of logatomes in *TextGrid* format (Praat annotations)
* **dico-UTF8.txt**: The dictionary (spelling-phoneme) including all relevant words
* **script_python.ipynb**: The program used to achieve this synthesis
* **results**: The results corresponding to the program


## Description
This Python-based project showcases detailed sound synthesis through phonetic manipulation of audio files. Users select a predefined French phrase, which is then phonetically analyzed, processed, and synthesized into speech using segmental diphones. The final output is a new audio file containing the synthesized speech.

## How to Use
1. **Start the Notebook**: Open the Jupyter notebook.
2. **Run the Notebook**: Execute the cells sequentially.
3. **Select a Phrase**: Input a number to choose one of the predefined phrases for synthesis.
4. **Output**: The synthesized audio file will be saved in the project directory as `phrase<number>.wav`, where `<number>` corresponds to the selected phrase.

    1. "Le cours de master un plurital de monsieur Gendrot est très intéressant"
    ```markdown
    Diphones : _l l@ @k ku uR Rd d@ @m ma as st t2 2R RI Ip pl ly yR Ri it ta al ld d2 2m m@ @s sj j@ @Z ZA Ad dR Ro oE Et tR RE Ez zI It tR RE Es sA A_
    ```
    2. "Le cours de master un plurital de madame Taravella est très difficile"
    ```markdown
    Diphones : _l l@ @k ku uR Rd d@ @m ma as st t2 2R RI Ip pl ly yR Ri it ta al ld d2 2m ma ad da am mt ta aR Ra av vE El la aE Et tR RE Ed di if fi is si il l_
    ```
    3. "Je suis un étudiant chinois qui vient de Paris trois"
    ```markdown
    Diphones : _Z Z@ @s sH Hi iI In nE Et ty yd dj jA AS Si in nw wa ak ki iv vj jI Id d@ @p pa aR Ri it tR Rw Wa a_
    ```
    4. "L'acquisition du langage chez l'enfant est un sujet intéressant"
    ```markdown
    Diphones : _l la ak ki iz zi is sj jO~ O~d dy yl lA Ag ga aZ ZS SE El lA Af fA AE Et tI Is sy yZ ZE EI It tE ER RE Es sA A_
    ```
    5. "Les enfants qui jouent avec les chiens sont très mignons"
    ```markdown
    Diphones : _l lE Ez zA Af fA Ak ki iZ Zu ua av vE Ek kl lE ES Sj jI Is sO~ O~t tR RE Em mi iN NO~ O~_
    ```

### Detailed Functionality
- **Phonetic Analysis**: Extracts phonetic details from the base audio file using the TextGrid annotations.
- **Diphone Extraction**: Identifies and extracts diphones from the phonetic data.
- **Sound Synthesis**: Concatenates diphone sounds based on the selected phrase to create seamless synthesized speech.


The Python notebook provided contains several code cells but no markdown cells. Here's a summary of what the code does:

1. **Imports**: The code uses libraries such as `parselmouth`, `textgrids`, and `matplotlib` to manipulate and analyze sound data.
2. **User Interaction**: It prompts the user to select a phrase for synthesis from a list of predefined phrases in French, related to academic courses or everyday observations.
3. **Sound File Manipulation**: The script loads a sound file and a corresponding TextGrid file, processes phonetic segments, extracts diphones, and uses these to synthesize the selected phrase.
4. **Dictionary Use**: A dictionary file is utilized to convert written text to its phonetic representation, and then this representation is used to generate sound segments.
5. **Sound Synthesis**: It concatenates sound segments to produce a synthesized voice output of the chosen phrase, and saves this output to a new sound file.

