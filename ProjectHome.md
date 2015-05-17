A fast, free and open source Transliterator, which could be easily extended to support other languages.

The included language files supports transliteration from:
English -> Sinhalese
English -> Tamil
Sinhalese -> Tamil
Sinhalese -> English
Tamil -> Sinhalese
Tamil -> English

The language data files could be easily updated to improve the accuracy of the transliterator. The implementation performs a dictionary based lookup for each word, and where an entry is not found, uses phonetic language rules to transliterate the word.

Note: This implementation is designed to be only dependent on the JDK (not even a logging library) and is optimized for speed, and thus caches the dictionaries into heap memory (about 1.25MB for English/Sinhala/Tamil)

The source code of the project is released under the GNU Affero General Public License v3
**http://www.gnu.org/licenses/agpl-3.0.html**

## Refer to the [User Guide](http://code.google.com/p/translit/wiki/UserGuide) for more details ##