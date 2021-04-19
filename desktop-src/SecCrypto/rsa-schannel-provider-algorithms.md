---
description: Les algorithmes peuvent être pris en charge par le fournisseur de services de chiffrement Microsoft RSA/Schannel.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Algorithmes de fournisseur RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512996"
---
# <a name="rsaschannel-provider-algorithms"></a><span data-ttu-id="54d1f-103">Algorithmes de fournisseur RSA/Schannel</span><span class="sxs-lookup"><span data-stu-id="54d1f-103">RSA/Schannel Provider Algorithms</span></span>

<span data-ttu-id="54d1f-104">Les algorithmes suivants peuvent être pris en charge par le fournisseur de services de chiffrement Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="54d1f-104">The following algorithms might be supported by the Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider.</span></span>



| <span data-ttu-id="54d1f-105">ID d’algorithme</span><span class="sxs-lookup"><span data-stu-id="54d1f-105">Algorithm ID</span></span>    | <span data-ttu-id="54d1f-106">Description</span><span class="sxs-lookup"><span data-stu-id="54d1f-106">Description</span></span>                                                                                                                         | <span data-ttu-id="54d1f-107">Commentaires</span><span class="sxs-lookup"><span data-stu-id="54d1f-107">Comments</span></span>                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54d1f-108">CALG \_ RSA \_ KEYX</span><span class="sxs-lookup"><span data-stu-id="54d1f-108">CALG\_RSA\_KEYX</span></span> | <span data-ttu-id="54d1f-109">[ *Algorithme d’échange de clés* publiques RSA](../secgloss/k-gly.md)</span><span class="sxs-lookup"><span data-stu-id="54d1f-109">RSA public key [*key exchange algorithm*](../secgloss/k-gly.md)</span></span> | <span data-ttu-id="54d1f-110">Longueur de clé : peut être définie, 384 bits à 16 384 bits par incréments de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="54d1f-110">Key length: Can be set, 384 bits to 16,384 bits in 8 bit increments.</span></span> <span data-ttu-id="54d1f-111">Longueur de clé par défaut : 1 024 bits.</span><span class="sxs-lookup"><span data-stu-id="54d1f-111">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="54d1f-112">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="54d1f-112">CALG\_MD5</span></span>       | <span data-ttu-id="54d1f-113">Algorithme de hachage MD5.</span><span class="sxs-lookup"><span data-stu-id="54d1f-113">MD5 hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="54d1f-114">Fourni uniquement pour le hachage.</span><span class="sxs-lookup"><span data-stu-id="54d1f-114">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="54d1f-115">CALG \_ SHA</span><span class="sxs-lookup"><span data-stu-id="54d1f-115">CALG\_SHA</span></span>       | <span data-ttu-id="54d1f-116">Algorithme de hachage SHA.</span><span class="sxs-lookup"><span data-stu-id="54d1f-116">SHA hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="54d1f-117">Doit être utilisé pour les signatures DSS.</span><span class="sxs-lookup"><span data-stu-id="54d1f-117">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="54d1f-118">CALG \_ RC2</span><span class="sxs-lookup"><span data-stu-id="54d1f-118">CALG\_RC2</span></span>       | <span data-ttu-id="54d1f-119">Algorithme de chiffrement par bloc RC2.</span><span class="sxs-lookup"><span data-stu-id="54d1f-119">RC2 block encryption algorithm.</span></span>                                                                                                     | <span data-ttu-id="54d1f-120">Longueur de clé : 40 à 88 bits</span><span class="sxs-lookup"><span data-stu-id="54d1f-120">Key length: 40 to 88 bits</span></span>                                                                                       |
| <span data-ttu-id="54d1f-121">CALG \_ RC4</span><span class="sxs-lookup"><span data-stu-id="54d1f-121">CALG\_RC4</span></span>       | <span data-ttu-id="54d1f-122">Algorithme de chiffrement de flux RC4.</span><span class="sxs-lookup"><span data-stu-id="54d1f-122">RC4 stream encryption algorithm.</span></span>                                                                                                    | <span data-ttu-id="54d1f-123">Longueur de clé : 40 à 88 bits</span><span class="sxs-lookup"><span data-stu-id="54d1f-123">Key length: 40 to 88 bits</span></span>                                                                                       |



 

 

 
