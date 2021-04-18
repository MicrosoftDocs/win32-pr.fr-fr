---
description: Le tableau suivant répertorie les algorithmes pris en charge par le fournisseur de services de chiffrement DSS Microsoft.
ms.assetid: 2a7aecf8-e242-4087-83ee-aaa637a9ec71
title: Algorithmes du fournisseur DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0bd9346da7a9ab1490e2646d9d2559c07359b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533887"
---
# <a name="dss-provider-algorithms"></a><span data-ttu-id="b7265-103">Algorithmes du fournisseur DSS</span><span class="sxs-lookup"><span data-stu-id="b7265-103">DSS Provider Algorithms</span></span>

<span data-ttu-id="b7265-104">Le tableau suivant répertorie les algorithmes pris en charge par le fournisseur de services de chiffrement DSS Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7265-104">The following table lists the algorithms supported by the Microsoft DSS Cryptographic Provider.</span></span>



| <span data-ttu-id="b7265-105">ID d’algorithme</span><span class="sxs-lookup"><span data-stu-id="b7265-105">Algorithm ID</span></span>    | <span data-ttu-id="b7265-106">Description</span><span class="sxs-lookup"><span data-stu-id="b7265-106">Description</span></span>                                 | <span data-ttu-id="b7265-107">Commentaires</span><span class="sxs-lookup"><span data-stu-id="b7265-107">Comments</span></span>                                                                                                        |
|-----------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7265-108">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="b7265-108">CALG\_MD5</span></span>       | <span data-ttu-id="b7265-109">Algorithme de hachage MD5.</span><span class="sxs-lookup"><span data-stu-id="b7265-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="b7265-110">Fourni uniquement pour le hachage.</span><span class="sxs-lookup"><span data-stu-id="b7265-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="b7265-111">CALG \_ SHA</span><span class="sxs-lookup"><span data-stu-id="b7265-111">CALG\_SHA</span></span>       | <span data-ttu-id="b7265-112">Algorithme de hachage SHA.</span><span class="sxs-lookup"><span data-stu-id="b7265-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="b7265-113">Doit être utilisé pour les signatures DSS.</span><span class="sxs-lookup"><span data-stu-id="b7265-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="b7265-114">CALG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="b7265-114">CALG\_SHA1</span></span>      | <span data-ttu-id="b7265-115">Identique à CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="b7265-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="b7265-116">Aucun commentaire.</span><span class="sxs-lookup"><span data-stu-id="b7265-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="b7265-117">CALG \_ DSS \_</span><span class="sxs-lookup"><span data-stu-id="b7265-117">CALG\_DSS\_SIGN</span></span> | <span data-ttu-id="b7265-118">Algorithme de signature de clé publique/privée DSS.</span><span class="sxs-lookup"><span data-stu-id="b7265-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="b7265-119">Longueur de clé : peut être défini, 512 bits à 1 024 bits dans des incréments de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b7265-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="b7265-120">Longueur de clé par défaut : 1 024 bits.</span><span class="sxs-lookup"><span data-stu-id="b7265-120">Default key length: 1,024 bits.</span></span><br/> |



 

 

 




