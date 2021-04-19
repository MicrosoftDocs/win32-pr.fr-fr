---
description: Répertorie les modifications apportées aux fonctionnalités d’enveloppement des données.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Ajouts de données enveloppées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527844"
---
# <a name="enveloped-data-additions"></a><span data-ttu-id="44c6c-103">Ajouts de données enveloppées</span><span class="sxs-lookup"><span data-stu-id="44c6c-103">Enveloped Data Additions</span></span>

<span data-ttu-id="44c6c-104">Les modifications suivantes ont été apportées aux fonctionnalités de données enveloppées :</span><span class="sxs-lookup"><span data-stu-id="44c6c-104">The following changes have been made to enveloped data capabilities:</span></span>

-   <span data-ttu-id="44c6c-105">L’identification du destinataire peut être effectuée non seulement par l’émetteur et le numéro de série (PKCS \# 7 1,5), mais également par l’identificateur de clé.</span><span class="sxs-lookup"><span data-stu-id="44c6c-105">Recipient identification can be done not only by Issuer and Serial Number (PKCS \#7 1.5), but also by Key Identifier.</span></span>
-   <span data-ttu-id="44c6c-106">Trois options d’échange de clés de destinataire sont fournies :</span><span class="sxs-lookup"><span data-stu-id="44c6c-106">Three recipient key exchange choices are provided:</span></span>
    -   <span data-ttu-id="44c6c-107">Transport de clé à l’aide de clés RSA.</span><span class="sxs-lookup"><span data-stu-id="44c6c-107">Key Transport using RSA keys.</span></span>
    -   <span data-ttu-id="44c6c-108">Accord de clé à l’aide de Ephemeral-Static Diffie-Hellman les clés d’algorithme encapsulées avec 3DES ou RC2, ou Ephemeral-Static les clés d’algorithme Diffie-Hellman elliptique Curve encapsulées avec AES.</span><span class="sxs-lookup"><span data-stu-id="44c6c-108">Key Agreement using either Ephemeral-Static Diffie-Hellman algorithm keys wrapped with 3DES or RC2, or Ephemeral-Static Elliptic Curve Diffie-Hellman algorithm keys wrapped with AES.</span></span>
    -   <span data-ttu-id="44c6c-109">Clé de chiffrement de clé ou transfert de clé de liste de messagerie où la clé utilisée pour chiffrer la clé de chiffrement de contenu a déjà été distribuée aux destinataires.</span><span class="sxs-lookup"><span data-stu-id="44c6c-109">Key Encryption Key or Mail List key transfer where the key used to encrypt the content encryption key has already been distributed to the recipients.</span></span> <span data-ttu-id="44c6c-110">RC2, 3DES et AES sont autorisés en tant qu’algorithmes de renvoi à la clé.</span><span class="sxs-lookup"><span data-stu-id="44c6c-110">RC2, 3DES and AES are allowed as key-wrapping algorithms.</span></span>
-   <span data-ttu-id="44c6c-111">Les attributs non protégés peuvent être inclus dans le message.</span><span class="sxs-lookup"><span data-stu-id="44c6c-111">Unprotected attributes can be included in the message.</span></span>
-   <span data-ttu-id="44c6c-112">Un champ **OriginatorInfo** contenant des informations sur l’expéditeur a été ajouté et peut contenir des certificats et des listes de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="44c6c-112">An **OriginatorInfo** field that contains information about the originator has been added that can contain certificates and CRLs.</span></span>
-   <span data-ttu-id="44c6c-113">Les algorithmes basés sur le chiffrement à courbe elliptique (ECC) et AES requièrent Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="44c6c-113">Elliptic Curve Cryptography (ECC) based algorithms and AES require Windows Vista or later.</span></span>

 

 



