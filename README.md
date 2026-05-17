# aura-fight
the best game
# =========================
# 1000 AVATARS GENERATOR
# =========================

avatars = {}

avatar_words_1 = [
    "Fire", "Ice", "Shadow", "Galaxy", "Dragon", "Thunder",
    "Dark", "Light", "Storm", "Magic", "Golden", "Silver",
    "Ultra", "Mega", "Hyper", "Cyber", "Ghost", "Moon",
    "Sun", "Crystal"
]

avatar_words_2 = [
    "Ninja", "Warrior", "Samurai", "Knight", "Hunter",
    "Fighter", "Demon", "Hero", "King", "Queen",
    "Master", "Legend", "Wizard", "Titan", "Phoenix",
    "Wolf", "Tiger", "Dragon", "Robot", "Guardian"
]

special_avatars = [
    "Banana Avatar",
    "Strawberry Avatar",
    "Naruto Avatar",
    "Pizza Avatar",
    "Rainbow Avatar",
    "Lava Avatar",
    "Zombie Avatar",
    "Diamond Avatar",
    "Angel Avatar",
    "Demon Avatar"
]

# Add special avatars first
for avatar in special_avatars:
    avatars[avatar] = {
        "power": 100
    }

# Generate 1000 avatars
count = 0

while len(avatars) < 1000:

    word1 = avatar_words_1[count % len(avatar_words_1)]
    word2 = avatar_words_2[(count // len(avatar_words_1)) % len(avatar_words_2)]

    avatar_name = f"{word1} {word2} #{count}"

    avatars[avatar_name] = {
        "power": 50 + (count % 200)
    }

    count += 1

# Show first 50 avatars
print("\n=== FIRST 50 AVATARS ===\n")

show_count = 0

for avatar, data in avatars.items():
    print(f"{avatar} | Power: {data['power']}")

    show_count += 1

    if show_count >= 50:
        break

print("\nTOTAL AVATARS:", len(avatars))
