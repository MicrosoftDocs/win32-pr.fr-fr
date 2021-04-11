---
title: Syntaxe d’intervalle
description: Représente une valeur d’intervalle de temps.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de syntaxe d’intervalle
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385319"
---
# <a name="interval-syntax"></a><span data-ttu-id="81915-104">Syntaxe d’intervalle</span><span class="sxs-lookup"><span data-stu-id="81915-104">Interval syntax</span></span>

<span data-ttu-id="81915-105">Représente une valeur d’intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="81915-105">Represents a time interval value.</span></span> <span data-ttu-id="81915-106">Les unités de temps réelles dépendent de l’attribut qui utilise cette syntaxe.</span><span class="sxs-lookup"><span data-stu-id="81915-106">The actual time units depend on which attribute is using this syntax.</span></span> <span data-ttu-id="81915-107">Cette syntaxe est identique à la syntaxe [**LargeInteger**](s-largeinteger.md) , sauf que les valeurs haute et basse sont des entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="81915-107">This syntax is identical to the [**LargeInteger**](s-largeinteger.md) syntax, except the high and low values are unsigned integers.</span></span>



| <span data-ttu-id="81915-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="81915-108">Entry</span></span> | <span data-ttu-id="81915-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="81915-109">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81915-110">Nom</span><span class="sxs-lookup"><span data-stu-id="81915-110">Name</span></span>         | <span data-ttu-id="81915-111">Intervalle</span><span class="sxs-lookup"><span data-stu-id="81915-111">Interval</span></span>                                                                           |
| <span data-ttu-id="81915-112">ID de syntaxe</span><span class="sxs-lookup"><span data-stu-id="81915-112">Syntax ID</span></span>    | <span data-ttu-id="81915-113">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="81915-113">2.5.5.16</span></span>                                                                           |
| <span data-ttu-id="81915-114">ID OM</span><span class="sxs-lookup"><span data-stu-id="81915-114">OM ID</span></span>        | <span data-ttu-id="81915-115">65</span><span class="sxs-lookup"><span data-stu-id="81915-115">65</span></span>                                                                                 |
| <span data-ttu-id="81915-116">Type MAPI</span><span class="sxs-lookup"><span data-stu-id="81915-116">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="81915-117">Type ADS</span><span class="sxs-lookup"><span data-stu-id="81915-117">ADS Type</span></span>     | <span data-ttu-id="81915-118">\_entier long \_ ADSTYPE</span><span class="sxs-lookup"><span data-stu-id="81915-118">ADSTYPE\_LARGE\_INTEGER</span></span>                                                            |
| <span data-ttu-id="81915-119">Type de variante</span><span class="sxs-lookup"><span data-stu-id="81915-119">Variant Type</span></span> | <span data-ttu-id="81915-120">\_distribution vt</span><span class="sxs-lookup"><span data-stu-id="81915-120">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="81915-121">SDS, type</span><span class="sxs-lookup"><span data-stu-id="81915-121">SDS Type</span></span>     | <span data-ttu-id="81915-122">Objet COM pouvant être casté en [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span><span class="sxs-lookup"><span data-stu-id="81915-122">A COM object that can be cast to an [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span></span> |



## <a name="see-also"></a><span data-ttu-id="81915-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81915-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81915-124">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="81915-124">**IADsLargeInteger**</span></span>](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[<span data-ttu-id="81915-125">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="81915-125">**LargeInteger**</span></span>](s-largeinteger.md)
</dt> </dl>

 

 
