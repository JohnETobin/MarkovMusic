---------------------------------------------------------------------------
CSC151-03 Final Project: Generating Classical Music Melodies
---------------------------------------------------------------------------
Authors: Jiyoung Chang, Chase Holdener, and John Tobin


What does our code do?

Our code is designed to take a range of song files (in the format
of the Orchset song text files), anaylze the pattern of the various 
notes and their durations in those songs, and use this analysis to
generate a new song through weighted random selection! The result 
is a new song file that can be manually entered into a midi file 
generator to listen to.


Instructions to operate our code:

1. Download the zipped Orchset dataset to a location where the folder
   can be unzipped, and then unzip it at that location. (We saved it on the desktop.)
2. Within the "Orchset" folder, there is a "GT" folder. Note the
   location pathway to get to the "GT" folder on your computer.  
   You will need this pathway later as a parameter for our procedure.
3. Open the "Final_Code_Music_Generator.rkt" Racket file and run the
   interactions pane.
4. Call the procedure "make-song" with 4 parameters: 
   (make-song <song-length> <location-path> <l-bound> <u-bound>)

      song-length = the desired number of measures for the song,
                    entered as an integer (Our code was designed
                    to generate music in the 4/4 time signature at
                    120 bpm, so each measure will correspond to 2
                    seconds of song.)
      location-path = the location pathway to the GT folder saved on 
                      your computer as a string
      l-bound = the lower bound of the range of songs you want included
                in generating the database that the new song will be 
                based on, an integer (see note below)
      u-bound = the upper bound of the range of songs you want included
                in generating the database that the new song will be 
                based on, an integer (see note below)

      NOTE on song ranges:
       The bounds for song ranges can span from 0-63. 0 marks the first
       song listed in the order provided in the Orchset file, 63 marks
       the last song in the Orchset file. If you open the "GT" folder 
       in Orchset you can see this ordering of songs that our procedure
       is based on. Depending on which values you choose for l-bound and
       u-bound you can generate music based on specific composers/ groups
       of composers. The documentation of the "make-song" procedure 
       provides more info.

5. Yay you've generated a song (hopefully)! Now, if you want to hear your
   masterpiece, you can go to a midi file song generator website and enter
   the notes with their respective durations. Start at the top of the outputted
   list, and work your way down entering the notes into the midi generator.
   https://onlinesequencer.net/ is a good website to try. Jam out!