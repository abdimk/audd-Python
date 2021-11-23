```yaml
'''python audd.io wrapper'''

# Example


#os.environ['api_token'] = 'YOUR API TOKEN FROM https://dashboard.audd.io/'
from utils import music_finder
from utils.music_finder import MusicFinder
from utils.extractor import Data
import config
import os
config.SPOTIFY = True  # if you don't want result from spotify make it false
config.APPLE_MUSIC = True
# You can't make both variables flase at the same time

music = MusicFinder('True', 'https://github.com/abdimk/audd-python/raw/main/samples(Records)/test_audio5.m4a')
# print(music.finder()) # return all the result as json
audio_data = Data(music.finder())


def var():
    print(f'''
title: {audio_data.title()}
artistName: {audio_data.artistName()}
ComposerName: {audio_data.composerName()}
release date: {audio_data.release_date()}
Spotify link: {audio_data.SPOTIFY_spotify()}
apple music preview: {audio_data.apple_music_previews_url()}''')


var()
```
