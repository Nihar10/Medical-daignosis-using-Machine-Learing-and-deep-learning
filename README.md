# Improving the accuracy of medical diagnosis with causal machine learning
## Paper

Improving the accuracy of medical diagnosis with causal machine learning, by Jonathan G. Richens, Ciarán M. Lee & Saurabh Johri. Published in nature communications. 

URL https://www.nature.com/articles/s41467-020-17419-7

## Citation
```
@article{richens2020improving,
  title={Improving the accuracy of medical diagnosis with causal machine learning},
  author={Richens, Jonathan G and Lee, Ciar{\'a}n M and Johri, Saurabh},
  journal={Nature communications},
  volume={11},
  number={1},
  pages={1--9},
  year={2020},
  publisher={Nature Publishing Group}
}
```

## Requirements

Use `python > 3.6` and install the requirements:

```
pip install -r requiurements.txt
```

## Running

The upcoming release of the code will include an API to allow the vignettes to be run on the models used in the [1]. In the interim, the --reproduce flag runs the code on precompied results to produce the results presented in [1]. Running run.py without --reproduce will run the inference engine on the models included in the repo, which are random noisy-OR networks. To run your own models, replace these and run the create_marginals method. 

**Please note that any information not used to generate the results in [1] is not included in the clinical vignettes. This includes doctor and patient information, and specifics such as disease and symptom concepts (other than the rareness of a disease)**

To reproduce the results from the paper:

```
python run.py --results my_results_dir --reproduce
```

To run on your own models, replace data/test_networks with your own network dictionary.

```
python run.py --first 10 
```

## Copyright and Licence

Copyright 2019-2020 Babylon Health (Babylon Partners Limited).

GNU General Public License v3.0

The algorithms presented in [1] and implimented here are protected under U.S. Patent Application No. 16/520,280. 

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
