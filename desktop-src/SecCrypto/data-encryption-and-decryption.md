---
description: Le chiffrement est le processus de conversion de données en texte brut (texte en clair) en un contenu qui semble aléatoire et inutile (texte chiffré). Le déchiffrement est le processus de conversion du texte chiffré en texte en clair.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Chiffrement et déchiffrement des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112675"
---
# <a name="data-encryption-and-decryption"></a>Chiffrement et déchiffrement des données

Le chiffrement est le processus de conversion de données en texte brut (texte en [*clair*](../secgloss/p-gly.md)) en un contenu qui semble aléatoire et inutile ([*texte chiffré*](../secgloss/c-gly.md)). Le déchiffrement est le processus de conversion du texte chiffré en texte en clair.

Pour chiffrer plus d’une petite quantité de données, le [*chiffrement symétrique*](../secgloss/s-gly.md) est utilisé. Une [*clé symétrique*](../secgloss/s-gly.md) est utilisée au cours du processus de chiffrement et de déchiffrement. Pour déchiffrer un élément de texte chiffré particulier, vous devez utiliser la clé qui a été utilisée pour chiffrer les données.

L’objectif de chaque algorithme de chiffrement est de le rendre aussi difficile que possible de déchiffrer le texte chiffré généré sans utiliser la clé. Si un algorithme de chiffrement correct est utilisé, il n’y a aucune technique nettement plus efficace que d’essayer méthodiquement chaque clé possible. Pour ce type d’algorithme, plus la clé est longue, plus il est difficile de déchiffrer un morceau de texte chiffré sans posséder la clé.

Il est difficile de déterminer la qualité d’un algorithme de chiffrement. Les algorithmes qui semblent prometteurs sont parfois très faciles à casser, en raison de l’attaque appropriée. Lorsque vous sélectionnez un algorithme de chiffrement, il est judicieux de choisir un algorithme qui a été utilisé depuis plusieurs années et qui a résisté à toutes les attaques.

Pour plus d’informations, consultez [fonctions de chiffrement et de déchiffrement des données](cryptography-functions.md).

 

 
