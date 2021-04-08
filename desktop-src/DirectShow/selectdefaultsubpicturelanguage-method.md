---
description: La méthode SelectDefaultSubpictureLanguage définit la langue de sous-image par défaut actuelle dans l’objet MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Méthode SelectDefaultSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746245"
---
# <a name="selectdefaultsubpicturelanguage-method"></a><span data-ttu-id="9d7ab-103">Méthode SelectDefaultSubpictureLanguage</span><span class="sxs-lookup"><span data-stu-id="9d7ab-103">SelectDefaultSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="9d7ab-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9d7ab-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9d7ab-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9d7ab-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9d7ab-106">La `SelectDefaultSubpictureLanguage` méthode définit la langue de sous-image par défaut actuelle dans l’objet **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="9d7ab-106">The `SelectDefaultSubpictureLanguage` method sets the current default subpicture language in the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a><span data-ttu-id="9d7ab-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d7ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d7ab-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="9d7ab-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="9d7ab-109">Spécifie la langue sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="9d7ab-109">Specifies the language as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="9d7ab-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="9d7ab-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="9d7ab-111">Spécifie l’extension de langage de sous-image sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="9d7ab-111">Specifies the subpicture language extension as an Integer.</span></span>



| <span data-ttu-id="9d7ab-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d7ab-112">Value</span></span> | <span data-ttu-id="9d7ab-113">Description</span><span class="sxs-lookup"><span data-stu-id="9d7ab-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="9d7ab-114">0</span><span class="sxs-lookup"><span data-stu-id="9d7ab-114">0</span></span>     | <span data-ttu-id="9d7ab-115">Extension non spécifiée</span><span class="sxs-lookup"><span data-stu-id="9d7ab-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="9d7ab-116">1</span><span class="sxs-lookup"><span data-stu-id="9d7ab-116">1</span></span>     | <span data-ttu-id="9d7ab-117">Légendes normales</span><span class="sxs-lookup"><span data-stu-id="9d7ab-117">Normal Captions</span></span>                |
| <span data-ttu-id="9d7ab-118">2</span><span class="sxs-lookup"><span data-stu-id="9d7ab-118">2</span></span>     | <span data-ttu-id="9d7ab-119">Grandes légendes</span><span class="sxs-lookup"><span data-stu-id="9d7ab-119">Big Captions</span></span>                   |
| <span data-ttu-id="9d7ab-120">3</span><span class="sxs-lookup"><span data-stu-id="9d7ab-120">3</span></span>     | <span data-ttu-id="9d7ab-121">Légendes des enfants</span><span class="sxs-lookup"><span data-stu-id="9d7ab-121">Children's Captions</span></span>            |
| <span data-ttu-id="9d7ab-122">5</span><span class="sxs-lookup"><span data-stu-id="9d7ab-122">5</span></span>     | <span data-ttu-id="9d7ab-123">Sous-titres normaux</span><span class="sxs-lookup"><span data-stu-id="9d7ab-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="9d7ab-124">6</span><span class="sxs-lookup"><span data-stu-id="9d7ab-124">6</span></span>     | <span data-ttu-id="9d7ab-125">Légendes volumineuses fermées</span><span class="sxs-lookup"><span data-stu-id="9d7ab-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="9d7ab-126">7</span><span class="sxs-lookup"><span data-stu-id="9d7ab-126">7</span></span>     | <span data-ttu-id="9d7ab-127">Sous-titres des enfants fermés</span><span class="sxs-lookup"><span data-stu-id="9d7ab-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="9d7ab-128">9</span><span class="sxs-lookup"><span data-stu-id="9d7ab-128">9</span></span>     | <span data-ttu-id="9d7ab-129">Forcé</span><span class="sxs-lookup"><span data-stu-id="9d7ab-129">Forced</span></span>                         |
| <span data-ttu-id="9d7ab-130">13</span><span class="sxs-lookup"><span data-stu-id="9d7ab-130">13</span></span>    | <span data-ttu-id="9d7ab-131">Commentaires du directeur normal</span><span class="sxs-lookup"><span data-stu-id="9d7ab-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="9d7ab-132">14</span><span class="sxs-lookup"><span data-stu-id="9d7ab-132">14</span></span>    | <span data-ttu-id="9d7ab-133">Commentaires du grand directeur</span><span class="sxs-lookup"><span data-stu-id="9d7ab-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="9d7ab-134">15</span><span class="sxs-lookup"><span data-stu-id="9d7ab-134">15</span></span>    | <span data-ttu-id="9d7ab-135">Commentaires Director’s des enfants</span><span class="sxs-lookup"><span data-stu-id="9d7ab-135">Children's Director's Comments</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d7ab-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9d7ab-136">Return Value</span></span>

<span data-ttu-id="9d7ab-137">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9d7ab-137">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d7ab-138">Notes</span><span class="sxs-lookup"><span data-stu-id="9d7ab-138">Remarks</span></span>

<span data-ttu-id="9d7ab-139">L’extension du langage de sous-image fournit des informations supplémentaires sur la sous-image.</span><span class="sxs-lookup"><span data-stu-id="9d7ab-139">The subpicture language extension provides further information about the subpicture.</span></span>

 

 



