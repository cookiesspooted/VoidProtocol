# VoidProtocol

**Version :** 1.0 (Draft)  
**Auteur :** [7ka1](https://github.com/cookiesspooted)  
**Statut :** En développement  
**Type :** Protocole de chiffrement symétrique confidentiel et sécurisé

---

## Présentation

**VoidProtocol** est un protocole de chiffrement nouvelle génération conçu pour répondre aux exigences de la cybersécurité moderne. Il combine un chiffrement par blocs robuste, un traitement par IV unique, et des transformations internes dynamiques, garantissant une forte confidentialité et une résistance accrue aux attaques connues.

> *Confidentialité. Intégrité. Résilience.*

---

## Fonctionnalités clés

- Chiffrement par blocs (128 bits)
- Clé de 256 bits (SHA-256 ou Argon2)
- Mode CBC customisé avec IV unique
- Padding sécurisé (PKCS7)
- Encodage final Base64
- Code source Python clair et documenté
- Extensible vers les protocoles post-quantiques (Kyber/Falcon) [à venir]

---

## Exemple d’utilisation

```python
from voidprotocol import VoidCipher

# Clé secrète (peut être dérivée d'un mot de passe)
key = b"my_super_secret_key"

# Donnée à chiffrer
data = b"Message confidentiel."

cipher = VoidCipher(key)

# Chiffrement
encrypted = cipher.encrypt(data)
print("Encrypted:", encrypted)

# Déchiffrement
decrypted = cipher.decrypt(encrypted)
print("Decrypted:", decrypted)
