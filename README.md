# Audio denoising (Speech-enchancement)

[![Build Status](https://travis-ci.com/vbelz/Speech-enhancement.svg?branch=master)](https://travis-ci.com/vbelz/Speech-enhancement)


(Inference and weights) Author, blog and sourcecode
>Vincent Belz : vincent.belz@gmail.com
>
>Published in towards data science : [Speech-enhancement with Deep learning](https://towardsdatascience.com/speech-enhancement-with-deep-learning-36a1991d3d8d)

> Repository: https://github.com/vbelz/Speech-enhancement

(Web application) Author: check license.

# How to run 

## Web version

Clic [here](https://audio-denoising.herokuapp.com/) to see the demo of speech-enchancement in action for audio (<10min).

## Docker version

To downloand the image and run the contaider in detach mode, run the code below.

```bash
docker container run -p 8501:8501 --rm -d pablogod/audio-denoising:latest
```
To shutdown the docker type this:

```bash
docker ps -aq # Check which id was assigned for the audio-denoising instance
docker stop <weird id of audio-denoising> # Type the id
```

## Local computer

Run this code locally on Linux based distros:
```bash
# Clone and install requirements
git clone https://github.com/DZDL/audio-denoising
cd audio-denoising
pip3 install -r requirements.txt
# Run streamlit
streamlit run app.py
# Then a webapp will open, check console output.
```

## Deploy docker on Heroku

Only maintainers of the repository can do this.
```bash
heroku login
docker ps
heroku container:login
heroku container:push web -a audio-denoising
heroku container:release web -a audio-denoising
```

## References (Model code from Speech-enhancement)

>Jansson, Andreas, Eric J. Humphrey, Nicola Montecchio, Rachel M. Bittner, Aparna Kumar and Tillman Weyde.**Singing Voice Separation with Deep U-Net Convolutional Networks.** *ISMIR* (2017).
>
>[https://ejhumphrey.com/assets/pdf/jansson2017singing.pdf]

>Grais, Emad M. and Plumbley, Mark D., **Single Channel Audio Source Separation using Convolutional Denoising Autoencoders** (2017).
>
>[https://arxiv.org/abs/1703.08019]

>Ronneberger O., Fischer P., Brox T. (2015) **U-Net: Convolutional Networks for Biomedical Image Segmentation**. In: Navab N., Hornegger J., Wells W., Frangi A. (eds) *Medical Image Computing and Computer-Assisted Intervention – MICCAI 2015*. MICCAI 2015. Lecture Notes in Computer Science, vol 9351. Springer, Cham
>
>[https://arxiv.org/abs/1505.04597]

> K. J. Piczak. **ESC: Dataset for Environmental Sound Classification**. *Proceedings of the 23rd Annual ACM Conference on Multimedia*, Brisbane, Australia, 2015.
>
> [DOI: http://dx.doi.org/10.1145/2733373.2806390]

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
