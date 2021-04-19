---
title: Événement AudioLanguageChange de l’objet AxWindowsMediaPlayer
description: L’événement AudioLanguageChange se produit lorsque le langage audio actuel change. | Événement AudioLanguageChange de l’objet AxWindowsMediaPlayer
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Événement AudioLanguageChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525107"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3a6fa-105">Événement AudioLanguageChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="3a6fa-105">AudioLanguageChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3a6fa-106">L’événement AudioLanguageChange se produit lorsque le langage audio actuel change.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-106">The AudioLanguageChange event occurs when the current audio language changes.</span></span>

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a><span data-ttu-id="3a6fa-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="3a6fa-107">Event Data</span></span>

<span data-ttu-id="3a6fa-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEventHandler**.</span></span> <span data-ttu-id="3a6fa-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="3a6fa-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="3a6fa-110">Property</span></span>   | <span data-ttu-id="3a6fa-111">Description</span><span class="sxs-lookup"><span data-stu-id="3a6fa-111">Description</span></span>                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6fa-112">**langID**</span><span class="sxs-lookup"><span data-stu-id="3a6fa-112">**langID**</span></span> | <span data-ttu-id="3a6fa-113">**System. Int32** Identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-113">**System.Int32** Uniquely identifies a particular language dialect, called a locale.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a6fa-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3a6fa-114">Remarks</span></span>

<span data-ttu-id="3a6fa-115">Un identificateur de paramètres régionaux (LCID) identifie de manière unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-115">A locale identifier (LCID) uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a6fa-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a6fa-116">Requirements</span></span>



| <span data-ttu-id="3a6fa-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a6fa-117">Requirement</span></span> | <span data-ttu-id="3a6fa-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a6fa-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6fa-119">Version</span><span class="sxs-lookup"><span data-stu-id="3a6fa-119">Version</span></span><br/>   | <span data-ttu-id="3a6fa-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3a6fa-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3a6fa-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3a6fa-121">Namespace</span></span><br/> | <span data-ttu-id="3a6fa-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3a6fa-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3a6fa-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="3a6fa-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3a6fa-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3a6fa-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a6fa-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a6fa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a6fa-126">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3a6fa-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a6fa-127">**IWMPControls3. currentAudioLanguage (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3a6fa-127">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





