---
title: Événement DomainChange de l’objet AxWindowsMediaPlayer
description: L’événement DomainChange se produit lorsque le domaine DVD change. | Événement DomainChange de l’objet AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Événement DomainChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533414"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="20c6d-105">Événement DomainChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="20c6d-105">DomainChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="20c6d-106">L’événement DomainChange se produit lorsque le domaine DVD change.</span><span class="sxs-lookup"><span data-stu-id="20c6d-106">The DomainChange event occurs when the DVD domain changes.</span></span>

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a><span data-ttu-id="20c6d-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="20c6d-107">Event Data</span></span>

<span data-ttu-id="20c6d-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="20c6d-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEventHandler**.</span></span> <span data-ttu-id="20c6d-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="20c6d-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="20c6d-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="20c6d-110">Property</span></span>  | <span data-ttu-id="20c6d-111">Description</span><span class="sxs-lookup"><span data-stu-id="20c6d-111">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c6d-112">strDomain</span><span class="sxs-lookup"><span data-stu-id="20c6d-112">strDomain</span></span> | <span data-ttu-id="20c6d-113">System. StringIndicates le nouveau domaine.</span><span class="sxs-lookup"><span data-stu-id="20c6d-113">System.StringIndicates the new domain.</span></span> <span data-ttu-id="20c6d-114">Pour connaître les valeurs possibles, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="20c6d-114">For possible values, see the Remarks section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20c6d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="20c6d-115">Remarks</span></span>

<span data-ttu-id="20c6d-116">Le tableau suivant indique les valeurs possibles pour la propriété strDomain.</span><span class="sxs-lookup"><span data-stu-id="20c6d-116">The following table shows the possible values for the strDomain property.</span></span>



| <span data-ttu-id="20c6d-117">String</span><span class="sxs-lookup"><span data-stu-id="20c6d-117">String</span></span>            | <span data-ttu-id="20c6d-118">Description</span><span class="sxs-lookup"><span data-stu-id="20c6d-118">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="20c6d-119">firstPlay</span><span class="sxs-lookup"><span data-stu-id="20c6d-119">firstPlay</span></span>         | <span data-ttu-id="20c6d-120">Exécution de l’initialisation par défaut d’un disque DVD.</span><span class="sxs-lookup"><span data-stu-id="20c6d-120">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="20c6d-121">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="20c6d-121">videoManagerMenu</span></span>  | <span data-ttu-id="20c6d-122">Affichage des menus pour la totalité du disque. Également appelé menu racine ou menu principal.</span><span class="sxs-lookup"><span data-stu-id="20c6d-122">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="20c6d-123">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="20c6d-123">videoTitleSetMenu</span></span> | <span data-ttu-id="20c6d-124">Affichage des menus pour le jeu de titres actuel.</span><span class="sxs-lookup"><span data-stu-id="20c6d-124">Displaying menus for current title set.</span></span> <span data-ttu-id="20c6d-125">Également appelé titleMenu.</span><span class="sxs-lookup"><span data-stu-id="20c6d-125">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="20c6d-126">title</span><span class="sxs-lookup"><span data-stu-id="20c6d-126">title</span></span>             | <span data-ttu-id="20c6d-127">Affichage du titre actuel.</span><span class="sxs-lookup"><span data-stu-id="20c6d-127">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="20c6d-128">stop</span><span class="sxs-lookup"><span data-stu-id="20c6d-128">stop</span></span>              | <span data-ttu-id="20c6d-129">Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.</span><span class="sxs-lookup"><span data-stu-id="20c6d-129">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

## <a name="requirements"></a><span data-ttu-id="20c6d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20c6d-130">Requirements</span></span>



| <span data-ttu-id="20c6d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20c6d-131">Requirement</span></span> | <span data-ttu-id="20c6d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="20c6d-132">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c6d-133">Version</span><span class="sxs-lookup"><span data-stu-id="20c6d-133">Version</span></span><br/>   | <span data-ttu-id="20c6d-134">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="20c6d-134">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="20c6d-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="20c6d-135">Namespace</span></span><br/> | <span data-ttu-id="20c6d-136">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="20c6d-136">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="20c6d-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="20c6d-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="20c6d-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="20c6d-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20c6d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20c6d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c6d-140">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="20c6d-140">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="20c6d-141">**Interface IWMPDVD (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="20c6d-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





