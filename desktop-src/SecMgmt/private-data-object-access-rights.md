---
description: Répertorie et décrit les droits d’accès de l’objet de données privées.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Droits d’accès à un objet de données privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484577"
---
# <a name="private-data-object-access-rights"></a><span data-ttu-id="c261c-103">Droits d’accès à un objet de données privées</span><span class="sxs-lookup"><span data-stu-id="c261c-103">Private Data Object Access Rights</span></span>

<span data-ttu-id="c261c-104">Les types d’accès de ce type d’objet sont :</span><span class="sxs-lookup"><span data-stu-id="c261c-104">The access types of this object type are:</span></span>



| <span data-ttu-id="c261c-105">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c261c-105">Access type</span></span>          | <span data-ttu-id="c261c-106">Description</span><span class="sxs-lookup"><span data-stu-id="c261c-106">Description</span></span>                                      |
|----------------------|--------------------------------------------------|
| <span data-ttu-id="c261c-107">valeur de la \_ requête secrète \_</span><span class="sxs-lookup"><span data-stu-id="c261c-107">SECRET\_QUERY\_VALUE</span></span> | <span data-ttu-id="c261c-108">Ce type d’accès est nécessaire pour récupérer un secret.</span><span class="sxs-lookup"><span data-stu-id="c261c-108">This access type is needed to retrieve a secret.</span></span> |
| <span data-ttu-id="c261c-109">valeur de l’ensemble de secrets \_ \_</span><span class="sxs-lookup"><span data-stu-id="c261c-109">SECRET\_SET\_VALUE</span></span>   | <span data-ttu-id="c261c-110">Ce type d’accès est nécessaire pour modifier un secret.</span><span class="sxs-lookup"><span data-stu-id="c261c-110">This access type is needed to modify a secret.</span></span>   |



 

## <a name="generic-access-masks"></a><span data-ttu-id="c261c-111">Masques d’accès génériques</span><span class="sxs-lookup"><span data-stu-id="c261c-111">Generic Access Masks</span></span>

<span data-ttu-id="c261c-112">Ce type d’objet contient les mappages d’accès génériques suivants :</span><span class="sxs-lookup"><span data-stu-id="c261c-112">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="c261c-113">Types d’accès standard :</span><span class="sxs-lookup"><span data-stu-id="c261c-113">Standard Access Types:</span></span>

<span data-ttu-id="c261c-114">Cet objet ne prend pas en charge le type d’accès standard SYNCHRONIZE (facultatif).</span><span class="sxs-lookup"><span data-stu-id="c261c-114">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="c261c-115">Tous les types d’accès requis sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c261c-115">All required access types are supported.</span></span> <span data-ttu-id="c261c-116">Le masque de tous les types d’accès pris en charge pour ce type d’objet est :</span><span class="sxs-lookup"><span data-stu-id="c261c-116">The mask of all supported access types for this object type is:</span></span>

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



