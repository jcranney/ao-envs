# ao-envs
A collection of Adaptive Optics simulations environments, targeted at specific difficult problems in the AO world, wrapped in [Gymnasium](https://gymnasium.farama.org/) to enable rapid ML development. Check out an [example environment](#environment), or [contribute](#contributing) your own for others to experiment with!

The goal of this collection is to enable rapid development of solutions to difficult problems in the world of AO. Gymnasium Environments allow a standardised API for interaction with these problems, enabling both classical control/estimation solutions, as well as AI-based ones.

If you have any feedback/suggestions/questions, or if there is an environment you would love to see simulated, please open an [issue](https://github.com/jcranney/ao-envs/issues).

## Getting Started
 1) choose an environment from the [list below](#environment)
 2) clone the environment, e.g.,:
    ```bash
    git clone https://github.com/jcranney/segment-phasing-fp-env
    cd segment-phasing-fp-env
    ```
 3) install it:
    ```bash
    pip install .
    ```
 4) import it:
    ```python
    import segment_phasing_fp_env  # noqa
    env = gymnasium.make("SegmentPhasingFP-v0")
    ```
 5) run it:
    ```python
    observation,info = env.reset()
    # compute action based on observation
    # ...
    env.step(action)
    ```

## Environments
### [`segment-phasing-fp-env`](https://github.com/jcranney/segment-phasing-fp-env)
This environment simulates the sensing and phasing of segment piston using a focal plane wavefront sensor, as in the Giant Magellan Telescope On-Instrument Wavefront Sensor (GMT OIWFS) for GMTNIRS and GMTIFS.

## Contributing
If you have developed or found an environment that you think is relevant, then please share it by:
 - [forking](https://github.com/jcranney/ao-envs/fork) this repository,
 - adding your *environment* details to this file in the list of [Environments](#environments) above,
 - creating a [pull request](https://github.com/jcranney/ao-envs/pulls).

 Please make sure that your `environment` inherits from the [`Gymansium.Env`](https://gymnasium.farama.org/api/env/) class, so that the API is consistent across these AO environments. If you are new to Gymnasium Environments, check out one of the examples above, or any of the examples provided by Farama, [here](https://gymnasium.farama.org/environments/third_party_environments/).