class player:
  def player(self):
    print("The Player is playing Cricket!")
class Batsman(player):
  def play(self):
    print("The Batsman is Batting!")
class Bowler(player):
  def play(self):
    print("The Bowler  is Bowling!")
batsman=Batsman()
bowler=Bowler()
batsman.play()
bowler.play()