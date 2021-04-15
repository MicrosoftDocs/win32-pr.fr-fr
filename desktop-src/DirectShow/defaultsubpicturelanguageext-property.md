---
description: La propriété DefaultSubpictureLanguageExt récupère l’extension du langage de sous-image de DVD par défaut.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Propriété DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520748"
---
# <a name="defaultsubpicturelanguageext-property"></a><span data-ttu-id="06010-103">Propriété DefaultSubpictureLanguageExt</span><span class="sxs-lookup"><span data-stu-id="06010-103">DefaultSubpictureLanguageExt Property</span></span>

> [!Note]  
> <span data-ttu-id="06010-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="06010-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="06010-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="06010-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="06010-106">La `DefaultSubpictureLanguageExt` propriété récupère l’extension du langage de sous-image de DVD par défaut.</span><span class="sxs-lookup"><span data-stu-id="06010-106">The `DefaultSubpictureLanguageExt` property retrieves the default DVD subpicture language extension.</span></span>

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a><span data-ttu-id="06010-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="06010-107">Return Value</span></span>

<span data-ttu-id="06010-108">Retourne une valeur entière indiquant l’extension du langage de sous-image de DVD par défaut.</span><span class="sxs-lookup"><span data-stu-id="06010-108">Returns an Integer value indicating the default DVD subpicture language extension.</span></span>

## <a name="remarks"></a><span data-ttu-id="06010-109">Notes</span><span class="sxs-lookup"><span data-stu-id="06010-109">Remarks</span></span>

<span data-ttu-id="06010-110">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="06010-110">This property is read-only with no default value.</span></span> <span data-ttu-id="06010-111">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="06010-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="06010-112">Value</span><span class="sxs-lookup"><span data-stu-id="06010-112">Value</span></span> | <span data-ttu-id="06010-113">Description</span><span class="sxs-lookup"><span data-stu-id="06010-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="06010-114">0</span><span class="sxs-lookup"><span data-stu-id="06010-114">0</span></span>     | <span data-ttu-id="06010-115">Extension non spécifiée</span><span class="sxs-lookup"><span data-stu-id="06010-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="06010-116">1</span><span class="sxs-lookup"><span data-stu-id="06010-116">1</span></span>     | <span data-ttu-id="06010-117">Légendes normales</span><span class="sxs-lookup"><span data-stu-id="06010-117">Normal Captions</span></span>                |
| <span data-ttu-id="06010-118">2</span><span class="sxs-lookup"><span data-stu-id="06010-118">2</span></span>     | <span data-ttu-id="06010-119">Grandes légendes</span><span class="sxs-lookup"><span data-stu-id="06010-119">Big Captions</span></span>                   |
| <span data-ttu-id="06010-120">3</span><span class="sxs-lookup"><span data-stu-id="06010-120">3</span></span>     | <span data-ttu-id="06010-121">Légendes des enfants</span><span class="sxs-lookup"><span data-stu-id="06010-121">Children's Captions</span></span>            |
| <span data-ttu-id="06010-122">5</span><span class="sxs-lookup"><span data-stu-id="06010-122">5</span></span>     | <span data-ttu-id="06010-123">Sous-titres normaux</span><span class="sxs-lookup"><span data-stu-id="06010-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="06010-124">6</span><span class="sxs-lookup"><span data-stu-id="06010-124">6</span></span>     | <span data-ttu-id="06010-125">Légendes volumineuses fermées</span><span class="sxs-lookup"><span data-stu-id="06010-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="06010-126">7</span><span class="sxs-lookup"><span data-stu-id="06010-126">7</span></span>     | <span data-ttu-id="06010-127">Sous-titres des enfants fermés</span><span class="sxs-lookup"><span data-stu-id="06010-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="06010-128">9</span><span class="sxs-lookup"><span data-stu-id="06010-128">9</span></span>     | <span data-ttu-id="06010-129">Forcé</span><span class="sxs-lookup"><span data-stu-id="06010-129">Forced</span></span>                         |
| <span data-ttu-id="06010-130">13</span><span class="sxs-lookup"><span data-stu-id="06010-130">13</span></span>    | <span data-ttu-id="06010-131">Commentaires du directeur normal</span><span class="sxs-lookup"><span data-stu-id="06010-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="06010-132">14</span><span class="sxs-lookup"><span data-stu-id="06010-132">14</span></span>    | <span data-ttu-id="06010-133">Commentaires du grand directeur</span><span class="sxs-lookup"><span data-stu-id="06010-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="06010-134">15</span><span class="sxs-lookup"><span data-stu-id="06010-134">15</span></span>    | <span data-ttu-id="06010-135">Commentaires Director’s des enfants</span><span class="sxs-lookup"><span data-stu-id="06010-135">Children's Director's Comments</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="06010-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06010-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06010-137">**SelectDefaultSubpictureLanguage**</span><span class="sxs-lookup"><span data-stu-id="06010-137">**SelectDefaultSubpictureLanguage**</span></span>](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



