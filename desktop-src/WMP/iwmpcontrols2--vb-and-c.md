---
title: IWMPControls2 (VB et C), interface (Wmp.h)
description: Fournit une méthode qui complète l’interface IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB et C) interface Windows Media Player
- Interface IWMPControls2 (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538107"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a><span data-ttu-id="fbf4c-105">Interface IWMPControls2 (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="fbf4c-105">IWMPControls2 (VB and C#) interface</span></span>

<span data-ttu-id="fbf4c-106">Fournit une méthode qui complète l’interface [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) .</span><span class="sxs-lookup"><span data-stu-id="fbf4c-106">Provides a method that supplements the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) interface.</span></span>

## <a name="members"></a><span data-ttu-id="fbf4c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fbf4c-107">Members</span></span>

<span data-ttu-id="fbf4c-108">L’interface **IWMPControls2 (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fbf4c-108">The **IWMPControls2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="fbf4c-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fbf4c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fbf4c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fbf4c-110">Methods</span></span>

<span data-ttu-id="fbf4c-111">L’interface **IWMPControls2 (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-111">The **IWMPControls2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="fbf4c-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="fbf4c-112">Method</span></span>                                                           | <span data-ttu-id="fbf4c-113">Description</span><span class="sxs-lookup"><span data-stu-id="fbf4c-113">Description</span></span>                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbf4c-114">**première**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-114">**step**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | <span data-ttu-id="fbf4c-115">Déplace l’élément de média vidéo actuel vers le cadre suivant ou le frame précédent et gèle la lecture.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-115">Moves the current video media item to the next frame or the previous frame and freezes playback.</span></span><br/> |



 

<span data-ttu-id="fbf4c-116">L’exemple de code suivant montre comment accéder à une interface [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) .</span><span class="sxs-lookup"><span data-stu-id="fbf4c-116">The following example code shows how to access an [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) interface.</span></span> <span data-ttu-id="fbf4c-117">L’exemple de code convertit la valeur [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) que la propriété [**AxWindowsMediaPlayer. Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) retourne à une valeur **IWMPControls2** .</span><span class="sxs-lookup"><span data-stu-id="fbf4c-117">The example code casts the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) value that the [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) property returns to a **IWMPControls2** value.</span></span>

<span data-ttu-id="fbf4c-118">Pour **C#**:</span><span class="sxs-lookup"><span data-stu-id="fbf4c-118">For **C#**:</span></span>


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



<span data-ttu-id="fbf4c-119">Pour **VB**:</span><span class="sxs-lookup"><span data-stu-id="fbf4c-119">For **VB**:</span></span>


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a><span data-ttu-id="fbf4c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbf4c-120">Requirements</span></span>



| <span data-ttu-id="fbf4c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbf4c-121">Requirement</span></span> | <span data-ttu-id="fbf4c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbf4c-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fbf4c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbf4c-123">Header</span></span><br/> | <dl> <span data-ttu-id="fbf4c-124"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf4c-124"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf4c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf4c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf4c-126">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-126">**IWMPControls**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[<span data-ttu-id="fbf4c-127">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-127">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="fbf4c-128">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fbf4c-129">**Interface IWMPControls3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-129">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





