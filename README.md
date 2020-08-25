var count = 0;
function cc (card) {
  var regex = /[JQKA]/;
  if (1 < card && card < 7) {
    count++;
  } else if (String(card).match(regex) || card === 10) {
    count--;
  }
  if (count > 0) return count + " Bet";
  return count + " Hold";
};

cc(2); cc(3); cc(7); cc('K'); cc('A');
