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
# <a name="data-encryption-and-decryption"></a><span data-ttu-id="aed64-104">Chiffrement et déchiffrement des données</span><span class="sxs-lookup"><span data-stu-id="aed64-104">Data Encryption and Decryption</span></span>

<span data-ttu-id="aed64-105">Le chiffrement est le processus de conversion de données en texte brut (texte en [*clair*](../secgloss/p-gly.md)) en un contenu qui semble aléatoire et inutile ([*texte chiffré*](../secgloss/c-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="aed64-105">Encryption is the process of translating plain text data ([*plaintext*](../secgloss/p-gly.md)) into something that appears to be random and meaningless ([*ciphertext*](../secgloss/c-gly.md)).</span></span> <span data-ttu-id="aed64-106">Le déchiffrement est le processus de conversion du texte chiffré en texte en clair.</span><span class="sxs-lookup"><span data-stu-id="aed64-106">Decryption is the process of converting ciphertext back to plaintext.</span></span>

<span data-ttu-id="aed64-107">Pour chiffrer plus d’une petite quantité de données, le [*chiffrement symétrique*](../secgloss/s-gly.md) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="aed64-107">To encrypt more than a small amount of data, [*symmetric encryption*](../secgloss/s-gly.md) is used.</span></span> <span data-ttu-id="aed64-108">Une [*clé symétrique*](../secgloss/s-gly.md) est utilisée au cours du processus de chiffrement et de déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="aed64-108">A [*symmetric key*](../secgloss/s-gly.md) is used during both the encryption and decryption processes.</span></span> <span data-ttu-id="aed64-109">Pour déchiffrer un élément de texte chiffré particulier, vous devez utiliser la clé qui a été utilisée pour chiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="aed64-109">To decrypt a particular piece of ciphertext, the key that was used to encrypt the data must be used.</span></span>

<span data-ttu-id="aed64-110">L’objectif de chaque algorithme de chiffrement est de le rendre aussi difficile que possible de déchiffrer le texte chiffré généré sans utiliser la clé.</span><span class="sxs-lookup"><span data-stu-id="aed64-110">The goal of every encryption algorithm is to make it as difficult as possible to decrypt the generated ciphertext without using the key.</span></span> <span data-ttu-id="aed64-111">Si un algorithme de chiffrement correct est utilisé, il n’y a aucune technique nettement plus efficace que d’essayer méthodiquement chaque clé possible.</span><span class="sxs-lookup"><span data-stu-id="aed64-111">If a really good encryption algorithm is used, there is no technique significantly better than methodically trying every possible key.</span></span> <span data-ttu-id="aed64-112">Pour ce type d’algorithme, plus la clé est longue, plus il est difficile de déchiffrer un morceau de texte chiffré sans posséder la clé.</span><span class="sxs-lookup"><span data-stu-id="aed64-112">For such an algorithm, the longer the key, the more difficult it is to decrypt a piece of ciphertext without possessing the key.</span></span>

<span data-ttu-id="aed64-113">Il est difficile de déterminer la qualité d’un algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="aed64-113">It is difficult to determine the quality of an encryption algorithm.</span></span> <span data-ttu-id="aed64-114">Les algorithmes qui semblent prometteurs sont parfois très faciles à casser, en raison de l’attaque appropriée.</span><span class="sxs-lookup"><span data-stu-id="aed64-114">Algorithms that look promising sometimes turn out to be very easy to break, given the proper attack.</span></span> <span data-ttu-id="aed64-115">Lorsque vous sélectionnez un algorithme de chiffrement, il est judicieux de choisir un algorithme qui a été utilisé depuis plusieurs années et qui a résisté à toutes les attaques.</span><span class="sxs-lookup"><span data-stu-id="aed64-115">When selecting an encryption algorithm, it is a good idea to choose one that has been in use for several years and has successfully resisted all attacks.</span></span>

<span data-ttu-id="aed64-116">Pour plus d’informations, consultez [fonctions de chiffrement et de déchiffrement des données](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="aed64-116">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md).</span></span>

 

 
