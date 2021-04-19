---
description: Répertorie et décrit les droits d’accès de l’objet TrustedDomain.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Droits d’accès à l’objet TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f79dc44b54ff907cbe3d1f700cc673f75a40d57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515002"
---
# <a name="trusteddomain-object-access-rights"></a><span data-ttu-id="095e9-103">Droits d’accès à l’objet TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="095e9-103">TrustedDomain Object Access Rights</span></span>

<span data-ttu-id="095e9-104">Le type d’objet [**trustedDomain**](trusteddomain-object.md) a les types d’accès suivants :</span><span class="sxs-lookup"><span data-stu-id="095e9-104">The [**TrustedDomain**](trusteddomain-object.md) object type has the following access types:</span></span>



| <span data-ttu-id="095e9-105">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="095e9-105">Access type</span></span>                  | <span data-ttu-id="095e9-106">Description</span><span class="sxs-lookup"><span data-stu-id="095e9-106">Description</span></span>                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="095e9-107">nom de domaine de la \_ requête approuvée \_ \_</span><span class="sxs-lookup"><span data-stu-id="095e9-107">TRUSTED\_QUERY\_DOMAIN\_NAME</span></span> | <span data-ttu-id="095e9-108">Ce type d’accès est nécessaire pour interroger le nom du domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="095e9-108">This access type is needed to query the name of the trusted domain.</span></span>              |
| <span data-ttu-id="095e9-109">\_contrôleurs de jeu approuvés \_</span><span class="sxs-lookup"><span data-stu-id="095e9-109">TRUSTED\_SET\_CONTROLLERS</span></span>    | <span data-ttu-id="095e9-110">Ce type d’accès est nécessaire pour définir la liste des contrôleurs du domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="095e9-110">This access type is needed to set the list of controllers of the trusted domain.</span></span> |
| <span data-ttu-id="095e9-111">requête de confiance \_ \_ POSIX</span><span class="sxs-lookup"><span data-stu-id="095e9-111">TRUSTED\_QUERY\_POSIX</span></span>        | <span data-ttu-id="095e9-112">Ce type d’accès est nécessaire pour récupérer le décalage d’ID POSIX d’un domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="095e9-112">This access type is needed to retrieve the Posix ID offset of a trusted domain.</span></span>  |
| <span data-ttu-id="095e9-113">jeu de confiance \_ \_ POSIX</span><span class="sxs-lookup"><span data-stu-id="095e9-113">TRUSTED\_SET\_POSIX</span></span>          | <span data-ttu-id="095e9-114">Ce type d’accès est nécessaire pour définir le décalage d’ID POSIX d’un domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="095e9-114">This access type is needed to set the Posix ID offset of a trusted domain.</span></span>       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="095e9-115">Masques d’accès génériques</span><span class="sxs-lookup"><span data-stu-id="095e9-115">Generic Access Masks</span></span>

<span data-ttu-id="095e9-116">Ce type d’objet contient les mappages d’accès génériques suivants :</span><span class="sxs-lookup"><span data-stu-id="095e9-116">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a><span data-ttu-id="095e9-117">Types d’accès standard</span><span class="sxs-lookup"><span data-stu-id="095e9-117">Standard Access Types</span></span>

<span data-ttu-id="095e9-118">Cet objet ne prend pas en charge le type d’accès standard SYNCHRONIZE (facultatif).</span><span class="sxs-lookup"><span data-stu-id="095e9-118">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="095e9-119">Tous les types d’accès requis sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="095e9-119">All required access types are supported.</span></span> <span data-ttu-id="095e9-120">Le masque de tous les types d’accès pris en charge pour ce type d’objet est :</span><span class="sxs-lookup"><span data-stu-id="095e9-120">The mask of all supported access types for this object type is:</span></span>

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



