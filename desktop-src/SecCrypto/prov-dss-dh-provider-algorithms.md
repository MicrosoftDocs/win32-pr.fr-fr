---
description: Algorithmes pris en charge par le fournisseur de services de chiffrement DSS de base Microsoft et Diffie-Hellman.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: Algorithmes de fournisseur d’PROV_DSS_DH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532308"
---
# <a name="prov_dss_dh-provider-algorithms"></a><span data-ttu-id="83809-103">Algorithmes PROVen du \_ \_ fournisseur DH DSS</span><span class="sxs-lookup"><span data-stu-id="83809-103">PROV\_DSS\_DH Provider Algorithms</span></span>

<span data-ttu-id="83809-104">Le tableau suivant répertorie les algorithmes pris en charge par Microsoft Base DSS et Diffie-Hellman fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="83809-104">The following table lists the algorithms supported by the Microsoft Base DSS and Diffie-Hellman Cryptographic Provider.</span></span>



| <span data-ttu-id="83809-105">ID d’algorithme</span><span class="sxs-lookup"><span data-stu-id="83809-105">Algorithm ID</span></span>      | <span data-ttu-id="83809-106">Description</span><span class="sxs-lookup"><span data-stu-id="83809-106">Description</span></span>                                 | <span data-ttu-id="83809-107">Commentaires</span><span class="sxs-lookup"><span data-stu-id="83809-107">Comments</span></span>                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83809-108">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="83809-108">CALG\_MD5</span></span>         | <span data-ttu-id="83809-109">Algorithme de hachage MD5.</span><span class="sxs-lookup"><span data-stu-id="83809-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="83809-110">Fourni uniquement pour le hachage.</span><span class="sxs-lookup"><span data-stu-id="83809-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="83809-111">CALG \_ SHA</span><span class="sxs-lookup"><span data-stu-id="83809-111">CALG\_SHA</span></span>         | <span data-ttu-id="83809-112">Algorithme de hachage SHA.</span><span class="sxs-lookup"><span data-stu-id="83809-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="83809-113">Doit être utilisé pour les signatures DSS.</span><span class="sxs-lookup"><span data-stu-id="83809-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="83809-114">CALG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="83809-114">CALG\_SHA1</span></span>        | <span data-ttu-id="83809-115">Identique à CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="83809-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="83809-116">Aucun commentaire.</span><span class="sxs-lookup"><span data-stu-id="83809-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="83809-117">CALG \_ DSS \_</span><span class="sxs-lookup"><span data-stu-id="83809-117">CALG\_DSS\_SIGN</span></span>   | <span data-ttu-id="83809-118">Algorithme de signature de clé publique/privée DSS.</span><span class="sxs-lookup"><span data-stu-id="83809-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="83809-119">Longueur de clé : peut être défini, 512 bits à 1 024 bits dans des incréments de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="83809-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="83809-120">Longueur de clé par défaut : 1 024 bits.</span><span class="sxs-lookup"><span data-stu-id="83809-120">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="83809-121">CALG \_ DH \_ DF</span><span class="sxs-lookup"><span data-stu-id="83809-121">CALG\_DH\_SF</span></span>      | <span data-ttu-id="83809-122">Échange de clé D-H pour le stockage et le transfert.</span><span class="sxs-lookup"><span data-stu-id="83809-122">Store and Forward D-H key exchange.</span></span>         | <span data-ttu-id="83809-123">Longueur de clé : peut être définie, 384 bits à 512 bits par incréments de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="83809-123">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="83809-124">Longueur de clé par défaut : 512 bits.</span><span class="sxs-lookup"><span data-stu-id="83809-124">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="83809-125">CALG \_ DH \_ EPHEM</span><span class="sxs-lookup"><span data-stu-id="83809-125">CALG\_DH\_EPHEM</span></span>   | <span data-ttu-id="83809-126">Échange de clé D-H éphémère.</span><span class="sxs-lookup"><span data-stu-id="83809-126">Ephemeral D-H key exchange.</span></span>                 | <span data-ttu-id="83809-127">Longueur de clé : peut être définie, 384 bits à 512 bits par incréments de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="83809-127">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="83809-128">Longueur de clé par défaut : 512 bits.</span><span class="sxs-lookup"><span data-stu-id="83809-128">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="83809-129">CALG \_ CYLINK \_ MEK</span><span class="sxs-lookup"><span data-stu-id="83809-129">CALG\_CYLINK\_MEK</span></span> | <span data-ttu-id="83809-130">Variante 40 bits d’une clé DES.</span><span class="sxs-lookup"><span data-stu-id="83809-130">A 40-bit variant of a DES key.</span></span>              | <span data-ttu-id="83809-131">Longueur de clé : 40 bits.</span><span class="sxs-lookup"><span data-stu-id="83809-131">Key Length: 40 bits.</span></span>                                                                                            |



 

 

 




