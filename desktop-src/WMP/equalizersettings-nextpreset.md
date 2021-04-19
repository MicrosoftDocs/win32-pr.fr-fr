---
title: EQUALIZERSETTINGS.nextPreset
description: La méthode nextPreset applique la présélection d’égaliseur suivante.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- Lecteur Windows Media EQUALIZERSETTINGS. nextPreset
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545661"
---
# <a name="equalizersettingsnextpreset"></a><span data-ttu-id="7536b-104">EQUALIZERSETTINGS.nextPreset</span><span class="sxs-lookup"><span data-stu-id="7536b-104">EQUALIZERSETTINGS.nextPreset</span></span>

<span data-ttu-id="7536b-105">La méthode **nextPreset** applique la présélection d’égaliseur suivante.</span><span class="sxs-lookup"><span data-stu-id="7536b-105">The **nextPreset** method applies the next equalizer preset.</span></span>

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a><span data-ttu-id="7536b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7536b-106">Parameters</span></span>

<span data-ttu-id="7536b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7536b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7536b-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7536b-108">Return Value</span></span>

<span data-ttu-id="7536b-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7536b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7536b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7536b-110">Remarks</span></span>

<span data-ttu-id="7536b-111">Si la présélection actuelle est la dernière disponible, la première présélection est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7536b-111">If the current preset is the last one available, the first preset is made current.</span></span>

## <a name="examples"></a><span data-ttu-id="7536b-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="7536b-112">Examples</span></span>


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a><span data-ttu-id="7536b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7536b-113">Requirements</span></span>



| <span data-ttu-id="7536b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7536b-114">Requirement</span></span> | <span data-ttu-id="7536b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7536b-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7536b-116">Version</span><span class="sxs-lookup"><span data-stu-id="7536b-116">Version</span></span><br/> | <span data-ttu-id="7536b-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="7536b-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7536b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7536b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7536b-119">**Élément EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="7536b-119">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="7536b-120">**EQUALIZERSETTINGS.previousPreset**</span><span class="sxs-lookup"><span data-stu-id="7536b-120">**EQUALIZERSETTINGS.previousPreset**</span></span>](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





