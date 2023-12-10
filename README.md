# paper2podcast
Convert research paper to friendly &amp; digestible podcast.


* CLI + Dashboard (Reflex/pure-python) + Docker container
* Fully open-source, including open-models
* Fully configurable, pick your own TTS and LLM model
* Input: pdf or arxiv link
* Output: [streaming] mp3

```python
def get_paper(pdf|url):
	// stuff
	return str(paper)
	
def get_transcript(paper <- str, style <- str) :
	// LLM CoT + style
	return transcript
	
def get_audio(stream=False):
	// stuff
	if stream:
		// more stuff
		yield
		
	return audio
	
def main():
	paper = get_user_input()
	paper_text = get_paper(paper)
	transcript = get_transcript(paper_text, style="rude, energetic")
	audio = get_audio(stream=True)
	audio.play()
```
