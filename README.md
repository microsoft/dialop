# 📠 The DialOp Environments

_Collaborative decision-oriented dialogue environments for humans and LLM agents._

These environments are associated with the paper **Decision-Oriented Dialogue For Human-AI Collaboration**.

[[Paper]](https://arxiv.org/abs/2305.20076)
[[Website]](https://collaborative-dialogue.github.io/)

![](assets/envs.png)

# Play against GPT-3

Get started and play the games with GPT-3 as an assistant:
```
pip install -e .
vim dialop/.api_key
python dialop/play_gpt3.py --game {optimization, planning, mediation}
```

# Overview

<p align="center">
<img src="assets/overview.png" width="500">
</p>

- `games`: define game logic, environment data generation
- `envs`: text-based interfaces for games
- `apps`: web app interfaces for games for human-human play


| Name         | Description   | Human UI           | Agent Text Interface | Hosted UI             |
| ------------ | ------------- | ------------------ | --------------------------------- | ------- |
| `Optimization` | Assign the best reviewers for conference papers | ![Optimization UI](assets/optimization_ui.png) | ![Optimization Text Interface](assets/optimization_text.png) | [Play now](http://reviewer-matching.herokuapp.com/) |
| `Planning` | Plan the best itinerary with the least travel and price | ![Planning UI](assets/planning_ui.png) | ![Planning Text Interface](assets/planning_text.png) | [Play now](https://itinerary-planning.herokuapp.com/)
| `Mediation` | Coordinate a set of group flights that works well for everyone | ![Mediation UI](assets/mediation_ui.png) | ![Mediation Text Interface](assets/mediation_text.png) | [Play now](https://collaborative-dialogue.herokuapp.com/)

**To play against yourself with the text-based environment:**
```
python dialop/play.py --game {optimization, planning, mediation}
```
**To play against yourself with the web UI:**
```
cd dialop/apps
game={optimization, planning, mediation} flask run
```
For Planning, you'll need to input a MapboxGL access key in `static/client.js` to show the map on the agent side.

# Human-Human Dialogues

To see human-human dialogues:
```
unzip dialop/data.zip
```

# Self-Play and Prompted Self-Play Evaluation

Coming soon!

# Citation
```
@article{lin2023decision,
  title={Decision-Oriented Dialogue for Human-AI Collaboration},
  author={Lin, Jessy and Tomlin, Nicholas and Andreas, Jacob and Eisner, Jason},
  journal={Transactions of the Association for Computational Linguistics}
  year={2024}
}
```

# Trademarks

This project may contain trademarks or logos for projects, products,
or services. Authorized use of Microsoft trademarks or logos is subject to and
must follow Microsoft’s Trademark & Brand Guidelines. Use of Microsoft
trademarks or logos in modified versions of this project must not cause
confusion or imply Microsoft sponsorship. Any use of third-party trademarks or
logos are subject to those third-party’s policies.
