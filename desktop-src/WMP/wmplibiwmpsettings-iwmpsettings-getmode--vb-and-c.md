---
title: Méthode IWMPSettings getMode
description: La méthode getMode retourne une valeur indiquant si le mode de boucle ou le mode de lecture aléatoire est actif.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- méthode getMode lecteur Windows Media
- méthode getMode lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, méthode getMode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542337"
---
# <a name="iwmpsettingsgetmode-method"></a><span data-ttu-id="03345-106">IWMPSettings :: getMode, méthode</span><span class="sxs-lookup"><span data-stu-id="03345-106">IWMPSettings::getMode method</span></span>

<span data-ttu-id="03345-107">La méthode **getMode** retourne une valeur indiquant si le mode de boucle ou le mode de lecture aléatoire est actif.</span><span class="sxs-lookup"><span data-stu-id="03345-107">The **getMode** method returns a value indicating whether loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="03345-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03345-108">Syntax</span></span>


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a><span data-ttu-id="03345-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03345-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03345-110">*bstrMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="03345-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03345-111">**System. String** qui est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="03345-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="03345-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="03345-112">Value</span></span>      | <span data-ttu-id="03345-113">Description</span><span class="sxs-lookup"><span data-stu-id="03345-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03345-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="03345-114">autoRewind</span></span> | <span data-ttu-id="03345-115">Les suivis sont redémarrés à partir du début après avoir été lus jusqu’à la fin.</span><span class="sxs-lookup"><span data-stu-id="03345-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="03345-116">loop</span><span class="sxs-lookup"><span data-stu-id="03345-116">loop</span></span>       | <span data-ttu-id="03345-117">La séquence de suivi se répète lui-même.</span><span class="sxs-lookup"><span data-stu-id="03345-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="03345-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="03345-118">showFrame</span></span>  | <span data-ttu-id="03345-119">L’image clé la plus proche s’affiche lorsque l’image n’est pas lue.</span><span class="sxs-lookup"><span data-stu-id="03345-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="03345-120">Ce mode n’est pas pertinent pour les pistes audio.</span><span class="sxs-lookup"><span data-stu-id="03345-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="03345-121">lecture aléatoire</span><span class="sxs-lookup"><span data-stu-id="03345-121">shuffle</span></span>    | <span data-ttu-id="03345-122">Les pistes sont lues dans un ordre aléatoire.</span><span class="sxs-lookup"><span data-stu-id="03345-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03345-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03345-123">Return value</span></span>

<span data-ttu-id="03345-124">Valeur **System. Boolean** indiquant si le mode spécifié est actif.</span><span class="sxs-lookup"><span data-stu-id="03345-124">A **System.Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="03345-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03345-125">Requirements</span></span>



| <span data-ttu-id="03345-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03345-126">Requirement</span></span> | <span data-ttu-id="03345-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="03345-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03345-128">Version</span><span class="sxs-lookup"><span data-stu-id="03345-128">Version</span></span><br/>   | <span data-ttu-id="03345-129">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="03345-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="03345-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="03345-130">Namespace</span></span><br/> | <span data-ttu-id="03345-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="03345-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="03345-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="03345-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="03345-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="03345-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03345-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03345-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03345-135">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="03345-135">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="03345-136">**IWMPSettings. setMode (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="03345-136">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





