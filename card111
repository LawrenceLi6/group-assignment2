#include"Card.h"
#include<stdio.h>
#include<stdlib.h>
#include<assert.h>
#include<err.h>

// Create a new card.
// These values can only be set at creation time.
// The number should be between 0x0 and 0xF.

typedef struct _card {
    suit s;
    value val;
    color c;
} card;

Card newCard(value value, color color, suit suit) {
    Card new = calloc(1,sizeof(card));
    if (new == NULL) {
        err(EXIT_FAILURE, "False");
    }
    new->s = suit;
    new->c = color;
    new->val = value;
    return new;
}

// Destroy an existing card.
void destroyCard(Card card) {
    assert(card != NULL);
    free(card);
}

// Get the card's suit (HEARTS, DIAMONDS, etc).
suit cardSuit(Card card) {
    assert(card != NULL);
    return card->s;
}

// Get the card's number (0x0 through 0xF).
value cardValue(Card card) {
    assert(card != NULL);
    return card->val;
}

// Get the card's color (RED, BLUE, etc).
color cardColor(Card card) {
    assert(card != NULL);
    return card->c;
}
