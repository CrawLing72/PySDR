.. _intro-chapter:

#############
소개
#############

***************************
목적과 대상 독자들
***************************

맨 먼저 가장 중요한 건, 한 쌍의 단어들입니다.

**Software-Defined Radio (SDR):**
    *개념* 적으로는 이는 소프트웨어를 사용해 하드웨어에서 수행되던 전통적인 신호 처리 작업을, 라디오/RF 애플리케이션에서 수행하는 것을 의미합니다. 이 소프트웨어는 범용 컴퓨터(CPU)나 FPGA, 심지어 GPU에서도 실행될 수 있으며 실시간 애플리케이션이나 입력 신호의 오프라인 처리에 사용할 수 있습니다. 유사한 용어로는 소프트웨어 라디오(Software Radio)와 RF 디지털 신호 처리(RF digital signal processing)이 있습니다.

    *일반* 적으로는 "SDR"은 안테나를 연결해 RF 신호를 수신할 수 있는 장치를 의미 하며, 디지털화된 RF 샘플은 처리 또는 기록을 위해 컴퓨터로 전송됩니다. (예: USB, PCI, 이더넷) 또한 많은 SDR에는 송신 기능이 있어서, 컴퓨터가 샘플을 SDR로 전송한 후 지정된 RF 주파수로 신호를 전송할 수 있습니다. 일부 임베디드의 성격을 띄는 SDR에는 컴퓨터가 내장되어 있기도 합니다.

**Digital Signal Processing (DSP):**
    신호를 디지털로 처리하는 것을 말하는데, PySDR의 경우는 RF(라디오 신호)가 됩니다.

이 가이드는 DSP, SDR 및 무선 통신 분야에 대한 실습 튜토리얼 입니다. 그리고 이는 아래와 같은 분들께 좋습니다:

#. 간지나는걸 하기 위해 SDR에 관심이 있으신 분
#. 파이썬 잘하시는 분
#. DSP, 무선 통신, SDR에 상대적으로 처음이신 분
#. 머리 아픈 방정식 대신에 애니메이션 같은 시각 자료를 좋아하시는 분
#. 개념을 배운 후 방정식을 더 잘이해하시는 분
#. 1000페이지 짜리 머리 아픈 교과서가 아니라, 간결한 설명을 찾고 계시는 분

An example is a Computer Science student interested in a job involving wireless communications after graduation, although it can be used by anyone itching to learn about SDR who has programming experience.  As such, it covers the necessary theory to understand DSP techniques without the intense math that is usually included in DSP courses.  Instead of burying ourselves in equations, an abundance of images and animations are used to help convey the concepts, such as the Fourier series complex plane animation below.  I believe that equations are best understood *after* learning the concepts through visuals and practical exercises.  The heavy use of animations is why PySDR will never have a hard copy version being sold on Amazon.  

.. image:: ../_images/fft_logo_wide.gif
   :scale: 70 %   
   :align: center
   :alt: The PySDR logo created using a Fourier transform
   
This textbook is meant to introduce concepts quickly and smoothly, enabling the reader to perform DSP and use SDRs intelligently.  It's not meant to be a reference textbook for all DSP/SDR topics; there are plenty of great textbooks already out there, such as `Analog Device's SDR textbook
<https://www.analog.com/en/education/education-library/software-defined-radio-for-engineers.html>`_ and `dspguide.com <http://www.dspguide.com/>`_.  You can always use Google to recall trig identities or the Shannon limit.  Think of this textbook like a gateway into the world of DSP and SDR: it's lighter and less of a time and monetary commitment, when compared to more traditional courses and textbooks.

To cover foundational DSP theory, an entire semester of "Signals and Systems", a typical course within electrical engineering, is condensed into a few chapters.  Once the DSP fundamentals are covered, we launch into SDRs, although DSP and wireless communications concepts continue to come up throughout the textbook.

Code examples are provided in Python.  They utilize NumPy, which is Python's standard library for arrays and high-level math.  The examples also rely upon Matplotlib, which is a Python plotting library that provides an easy way to visualize signals, arrays, and complex numbers.  Note that while Python is "slower" than C++ in general, most math functions within Python/NumPy are implemented in C/C++ and heavily optimized.  Likewise, the SDR API we use is simply a set of Python bindings for C/C++ functions/classes.  Those who have little Python experience yet a solid foundation in MATLAB, Ruby, or Perl will likely be fine after familiarizing themselves with Python's syntax.


***************
Contributing
***************

If you got value from PySDR, please share it with colleagues, students, and other lifelong learners who may be interested in the material.  You can also donate through the `PySDR Patreon <https://www.patreon.com/PySDR>`_ as a way to say thanks and get your name on the left of every page below the chapter list.

If you get through any amount of this textbook and email me at marc@pysdr.org with questions/comments/suggestions, then congratulations, you will have contributed to this textbook!  You can also edit the source material directly on the `textbook's GitHub page <https://github.com/777arc/PySDR/tree/master/content>`_ (your change will start a new pull request).  Feel free to submit an issue or even a Pull Request (PR) with fixes or improvements.  Those who submit valuable feedback/fixes will be permanently added to the acknowledgments section below.  Not good at Git but have changes to suggest?  Feel free to email me at marc@pysdr.org.

*****************
Acknowledgements
*****************

Thank you to anyone who has read any portion of this textbook and provided feedback, and especially to:

- `Barry Duggan <http://github.com/duggabe>`_
- Matthew Hannon
- James Hayek
- Deidre Stuffer
- Tarik Benaddi for `translating PySDR to French <https://pysdr.org/fr/index-fr.html>`_
- `Daniel Versluis <https://versd.bitbucket.io/content/about.html>`_ for `translating PySDR to Dutch <https://pysdr.org/nl/index-nl.html>`_
- `mrbloom <https://github.com/mrbloom>`_ for `translating PySDR to Ukrainian <https://pysdr.org/ukraine/index-ukraine.html>`_
- `Yimin Zhao <https://github.com/doctormin>`_ for `translating PySDR to Simplified Chinese <https://pysdr.org/zh/index-zh.html>`_
- `Eduardo Chancay <https://github.com/edulchan>`_ for `translating PySDR to Spanish <https://pysdr.org/es/index-es.html>`_

As well as all `PySDR Patreon <https://www.patreon.com/PySDR>`_ supporters!
