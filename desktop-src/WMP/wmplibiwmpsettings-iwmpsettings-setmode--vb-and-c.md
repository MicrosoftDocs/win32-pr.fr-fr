---
title: Méthode IWMPSettings setMode
description: La méthode setMode définit le mode de boucle ou le mode de lecture aléatoire sur actif ou inactif.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- méthode setMode lecteur Windows Media
- méthode setMode lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, méthode setMode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528379"
---
# <a name="iwmpsettingssetmode-method"></a><span data-ttu-id="ce5d0-106">IWMPSettings :: setMode, méthode</span><span class="sxs-lookup"><span data-stu-id="ce5d0-106">IWMPSettings::setMode method</span></span>

<span data-ttu-id="ce5d0-107">La méthode **setMode** définit le mode de boucle ou le mode de lecture aléatoire sur actif ou inactif.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-107">The **setMode** method sets the loop mode or shuffle mode to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce5d0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce5d0-108">Syntax</span></span>


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a><span data-ttu-id="ce5d0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce5d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce5d0-110">*bstrMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce5d0-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5d0-111">**System. String** qui est le nom du mode en cours de modification, contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-111">A **System.String** that is the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="ce5d0-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce5d0-112">Value</span></span>      | <span data-ttu-id="ce5d0-113">Description</span><span class="sxs-lookup"><span data-stu-id="ce5d0-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5d0-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="ce5d0-114">autoRewind</span></span> | <span data-ttu-id="ce5d0-115">Les suivis sont redémarrés à partir du début après avoir été lus jusqu’à la fin.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="ce5d0-116">loop</span><span class="sxs-lookup"><span data-stu-id="ce5d0-116">loop</span></span>       | <span data-ttu-id="ce5d0-117">La séquence de suivi se répète lui-même.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="ce5d0-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="ce5d0-118">showFrame</span></span>  | <span data-ttu-id="ce5d0-119">L’image clé la plus proche s’affiche lorsque l’image n’est pas lue.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="ce5d0-120">Ce mode n’est pas pertinent pour les pistes audio.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="ce5d0-121">lecture aléatoire</span><span class="sxs-lookup"><span data-stu-id="ce5d0-121">shuffle</span></span>    | <span data-ttu-id="ce5d0-122">Les pistes sont lues dans un ordre aléatoire.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> <dt>

<span data-ttu-id="ce5d0-123">*varfMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce5d0-123">*varfMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5d0-124">Valeur **System. Boolean** spécifiant si le nouveau mode spécifié est actif.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-124">A **System.Boolean** value specifying whether the new specified mode is active.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce5d0-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce5d0-125">Return value</span></span>

<span data-ttu-id="ce5d0-126">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce5d0-127">Notes</span><span class="sxs-lookup"><span data-stu-id="ce5d0-127">Remarks</span></span>

<span data-ttu-id="ce5d0-128">Lorsque le mode showFrame est actif, le lecteur Windows Media doit accéder au contenu Track pour récupérer la trame vidéo.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-128">When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="ce5d0-129">Utilisez ce mode avec précaution lors de la diffusion de contenu qui n’est pas local.</span><span class="sxs-lookup"><span data-stu-id="ce5d0-129">Use this mode cautiously when playing content that is not local.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce5d0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce5d0-130">Requirements</span></span>



| <span data-ttu-id="ce5d0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce5d0-131">Requirement</span></span> | <span data-ttu-id="ce5d0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce5d0-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5d0-133">Version</span><span class="sxs-lookup"><span data-stu-id="ce5d0-133">Version</span></span><br/>   | <span data-ttu-id="ce5d0-134">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ce5d0-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ce5d0-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ce5d0-135">Namespace</span></span><br/> | <span data-ttu-id="ce5d0-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ce5d0-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ce5d0-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="ce5d0-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ce5d0-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ce5d0-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce5d0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce5d0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5d0-140">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ce5d0-140">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce5d0-141">**IWMPSettings. getMode (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ce5d0-141">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





