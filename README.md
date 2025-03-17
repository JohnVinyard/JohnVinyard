## Contents

- [Current Research](#current-research)
- [Fun Web Audio Toys](#fun-web-audio-toys)
- [Hire Me](#hire-me)
- [Sponsor Me](#sponsor-me)
  

My current area of research is in sparse, interpretable and easy-to-manipulate models of audio (especially music).  My ambitous goal is to define and build an audio codec that is sparse, compressive, perceptually lossless, and directly manipulatable.  In this nascent codec, some types of musical composition might take directly in the codec space, rather than in a DAW, or other specialized tool.  My ideal is that this codec will be:

- sparse and event based, enumerating conceptually-distinct events and their times of occurrence
- sample-rate independent, not rasterized, and not dependent on block-coding of fixed-size frames, with audio generated using something akin to neural operators, NERF, or SIREN-type models
- perceptually-losseless, taking advantage of masking, invariances over phase, the loss of phase-locking starting at 5khz, and other perceptual phenomena
- compressive at a rate _at least_ as competitive as that of current codecs like MP3 or Ogg Vorbis

## Current Research

### [Toward a Sparse, Interpretable Audio Codec]()

<img src="https://github.com/user-attachments/assets/424f803e-d969-4d69-9aa7-f8fc5f2dd739" alt="Sparse audio events" height="200" width="100%" />

[This evolving work](https://blog.cochlea.xyz/sparse-interpretable-audio-codec-paper.html) describes a deep-learning architecture for decomposing musical audio into a sparse, event-based representation iteratively, something like neural matching pursuit.

### [Learning Playable State-Space Models from Audio](https://blog.cochlea.xyz/rnn.html)

<img src="https://github.com/user-attachments/assets/95993a48-3829-4de1-870b-c65f242e5c1d" alt="Sparse control signal" height="200" />

[This work](https://blog.cochlea.xyz/rnn.html) posits that one key to sparsity is something like a "resonance prior" that factors audio signals into two distinct parts:

- A model of the dynamics of the instrument, room, synth, vocal tract, or combination thereof
- A sparse "control signal" that describes how energy is injected into this system by a performer

In addition to sparsity, this factorization also means that a playable instrument of sorts might be extracted from an audio signal, allowing new compositions to be created by altering the sparse control signal while holding the model constant.

## Fun Web Audio Toys

### [Web Audio Spring-Mass Synthesis](https://blog.cochlea.xyz/string.html)

[This Web Audio demo](https://blog.cochlea.xyz/string.html) uses a custom [`AudioWorklet`](https://developer.mozilla.org/en-US/docs/Web/API/AudioWorklet) to perform physical-modeling synthesis using a spring-mass system.  It was inspired by the amazing work of [mi-creative](https://github.com/mi-creative).  Models with physics-based assumptions baked in are a natural tool for deriving sparser audio representations and imposing the "resonance prior".  This toy was a fun way to start learning about this topic!

### [Web Audio RNN Inference](https://blog.cochlea.xyz/rnn.html)

Each "Interactive Instrument" section in the [Playable State-Space Models article](https://blog.cochlea.xyz/rnn.html) includes a custom [`AudioWorklet`](https://developer.mozilla.org/en-US/docs/Web/API/AudioWorklet) that performs inference given the weights of pre-trained, single layer RNN, using them to produce real-time audio!

## Hire Me

I'm an Austin TX-based software engineer with over 20 years of experience.  In addition to deep familiarity with [`NumPy`](https://numpy.org/), [`scipy`](https://scipy.org/), [`PyTorch`](https://pytorch.org/) and scientific computing in general, I am also a full-stack engineer who has worked extensively designing and building APIs and frontends on teams large and small.  Feel free to reach out if you have a project that you think I'd be a good fit for!

## Sponsor Me

If you find my research and would like to see more, I'd be deeply appreciative if you wanted to [sponsor me](https://github.com/sponsors/JohnVinyard)!
