---
description: Avec les fonctions de hachage et de signature numérique, un utilisateur peut signer numériquement des données afin que n’importe quel autre utilisateur puisse vérifier que les données n’ont pas été modifiées depuis qu’il a été signé. L’identité de l’utilisateur qui a signé les données peut également être vérifiée.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hachages et signatures numériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521111"
---
# <a name="hashes-and-digital-signatures"></a><span data-ttu-id="3af8b-104">Hachages et signatures numériques</span><span class="sxs-lookup"><span data-stu-id="3af8b-104">Hashes and Digital Signatures</span></span>

<span data-ttu-id="3af8b-105">Avec les [fonctions de hachage et de signature numérique](cryptography-functions.md), un utilisateur peut signer numériquement des données afin que n’importe quel autre utilisateur puisse vérifier que les données n’ont pas été modifiées depuis qu’il a été signé.</span><span class="sxs-lookup"><span data-stu-id="3af8b-105">With [Hash and Digital Signature Functions](cryptography-functions.md), a user can digitally sign data so that any other user can verify that the data has not been changed since it was signed.</span></span> <span data-ttu-id="3af8b-106">L’identité de l’utilisateur qui a signé les données peut également être vérifiée.</span><span class="sxs-lookup"><span data-stu-id="3af8b-106">The identity of the user who signed the data can also be verified.</span></span>

<span data-ttu-id="3af8b-107">Une [*signature numérique*](../secgloss/d-gly.md) est constituée d’une petite quantité de données binaires, en général moins de 256 octets.</span><span class="sxs-lookup"><span data-stu-id="3af8b-107">A [*digital signature*](../secgloss/d-gly.md) consists of a small amount of binary data, typically less than 256 bytes.</span></span> <span data-ttu-id="3af8b-108">Cette signature peut être regroupée avec le message signé ou stockée séparément, en fonction de la façon dont une application particulière a été implémentée.</span><span class="sxs-lookup"><span data-stu-id="3af8b-108">This signature can be bundled with the signed message or stored separately, depending on how a particular application has been implemented.</span></span>

<span data-ttu-id="3af8b-109">Le fournisseur de services de chiffrement fort Microsoft crée des signatures numériques conformes aux [*normes de chiffrement de clé publique*](../secgloss/p-gly.md) RSA (PKCS) \# 1.</span><span class="sxs-lookup"><span data-stu-id="3af8b-109">The Microsoft Strong Cryptographic Provider creates digital signatures that conform to the RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1.</span></span>

 

 
