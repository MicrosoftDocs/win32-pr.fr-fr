---
title: Événement OpenStateChange de l’objet AxWindowsMediaPlayer
description: L’événement OpenStateChange se produit lorsque la propriété openState change de valeur. | Événement OpenStateChange de l’objet AxWindowsMediaPlayer
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- Événement OpenStateChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538075"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="11944-105">Événement OpenStateChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="11944-105">OpenStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="11944-106">L’événement OpenStateChange se produit lorsque la propriété **openState** change de valeur.</span><span class="sxs-lookup"><span data-stu-id="11944-106">The OpenStateChange event occurs when the **openState** property changes value.</span></span>

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a><span data-ttu-id="11944-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="11944-107">Event Data</span></span>

<span data-ttu-id="11944-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="11944-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEventHandler**.</span></span> <span data-ttu-id="11944-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="11944-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="11944-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="11944-110">Property</span></span> | <span data-ttu-id="11944-111">Description</span><span class="sxs-lookup"><span data-stu-id="11944-111">Description</span></span>                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11944-112">NewState</span><span class="sxs-lookup"><span data-stu-id="11944-112">NewState</span></span> | <span data-ttu-id="11944-113">System. Int32Specifies : nouvel état ouvert.</span><span class="sxs-lookup"><span data-stu-id="11944-113">System.Int32Specifies the new open state.</span></span> <span data-ttu-id="11944-114">Pour obtenir une table de valeurs, consultez [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="11944-114">For a table of values, see [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11944-115">Notes</span><span class="sxs-lookup"><span data-stu-id="11944-115">Remarks</span></span>

<span data-ttu-id="11944-116">Le lecteur Windows Media peut passer par plusieurs États ouverts pendant qu’il tente d’ouvrir un fichier réseau, par exemple Rechercher le serveur, se connecter au serveur et enfin ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="11944-116">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="11944-117">Cet événement est déclenché chaque fois que l’état ouvert change.</span><span class="sxs-lookup"><span data-stu-id="11944-117">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="11944-118">Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="11944-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="11944-119">En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="11944-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="11944-120">Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.</span><span class="sxs-lookup"><span data-stu-id="11944-120">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="11944-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11944-121">Requirements</span></span>



| <span data-ttu-id="11944-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11944-122">Requirement</span></span> | <span data-ttu-id="11944-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="11944-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11944-124">Version</span><span class="sxs-lookup"><span data-stu-id="11944-124">Version</span></span><br/>   | <span data-ttu-id="11944-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="11944-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="11944-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="11944-126">Namespace</span></span><br/> | <span data-ttu-id="11944-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="11944-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="11944-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="11944-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="11944-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="11944-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11944-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11944-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11944-131">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="11944-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="11944-132">**AxWindowsMediaPlayer. openState (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="11944-132">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





