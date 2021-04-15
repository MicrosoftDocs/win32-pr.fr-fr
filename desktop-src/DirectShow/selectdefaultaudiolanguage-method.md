---
description: La méthode SelectDefaultAudioLanguage définit la langue audio par défaut actuelle dans l’objet MSWebDVD.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Méthode SelectDefaultAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521276"
---
# <a name="selectdefaultaudiolanguage-method"></a><span data-ttu-id="e1ad5-103">Méthode SelectDefaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="e1ad5-103">SelectDefaultAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="e1ad5-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e1ad5-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e1ad5-106">La `SelectDefaultAudioLanguage` méthode définit la langue audio par défaut actuelle dans l’objet mswebdvd.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-106">The `SelectDefaultAudioLanguage` method sets the current default audio language in the MSWebDVD object.</span></span>

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a><span data-ttu-id="e1ad5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1ad5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1ad5-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="e1ad5-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="e1ad5-109">Spécifie la langue sous la forme d’une valeur LCID entière.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-109">Specifies the language as an Integer LCID value.</span></span>

</dd> <dt>

<span data-ttu-id="e1ad5-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="e1ad5-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="e1ad5-111">Spécifie l’extension de langage audio DVD en tant que valeur entière.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-111">Specifies the DVD audio language extension as an integer value.</span></span>



| <span data-ttu-id="e1ad5-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1ad5-112">Value</span></span> | <span data-ttu-id="e1ad5-113">Description</span><span class="sxs-lookup"><span data-stu-id="e1ad5-113">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="e1ad5-114">0</span><span class="sxs-lookup"><span data-stu-id="e1ad5-114">0</span></span>     | <span data-ttu-id="e1ad5-115">NotSpecified</span><span class="sxs-lookup"><span data-stu-id="e1ad5-115">NotSpecified</span></span>      |
| <span data-ttu-id="e1ad5-116">1</span><span class="sxs-lookup"><span data-stu-id="e1ad5-116">1</span></span>     | <span data-ttu-id="e1ad5-117">Sous-titres</span><span class="sxs-lookup"><span data-stu-id="e1ad5-117">Captions</span></span>          |
| <span data-ttu-id="e1ad5-118">2</span><span class="sxs-lookup"><span data-stu-id="e1ad5-118">2</span></span>     | <span data-ttu-id="e1ad5-119">VisuallyImpaired</span><span class="sxs-lookup"><span data-stu-id="e1ad5-119">VisuallyImpaired</span></span>  |
| <span data-ttu-id="e1ad5-120">3</span><span class="sxs-lookup"><span data-stu-id="e1ad5-120">3</span></span>     | <span data-ttu-id="e1ad5-121">DirectorComments1</span><span class="sxs-lookup"><span data-stu-id="e1ad5-121">DirectorComments1</span></span> |
| <span data-ttu-id="e1ad5-122">4</span><span class="sxs-lookup"><span data-stu-id="e1ad5-122">4</span></span>     | <span data-ttu-id="e1ad5-123">DirectorComments2</span><span class="sxs-lookup"><span data-stu-id="e1ad5-123">DirectorComments2</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1ad5-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e1ad5-124">Return Value</span></span>

<span data-ttu-id="e1ad5-125">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-125">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1ad5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1ad5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ad5-127">Objet MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="e1ad5-127">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



