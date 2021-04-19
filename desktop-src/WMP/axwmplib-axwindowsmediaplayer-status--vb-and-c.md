---
title: AxWindowsMediaPlayer. Status, propriété
description: La propriété Status obtient une valeur indiquant l’état du lecteur Windows Media.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- propriété d’État lecteur Windows Media
- propriété d’État lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété Status
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525262"
---
# <a name="axwindowsmediaplayerstatus-property"></a><span data-ttu-id="312d0-106">AxWindowsMediaPlayer. Status, propriété</span><span class="sxs-lookup"><span data-stu-id="312d0-106">AxWindowsMediaPlayer.status property</span></span>

<span data-ttu-id="312d0-107">La propriété Status obtient une valeur indiquant l’état du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="312d0-107">The status property gets a value indicating the status of Windows Media Player.</span></span>

<span data-ttu-id="312d0-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="312d0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="312d0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="312d0-109">Syntax</span></span>


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a><span data-ttu-id="312d0-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="312d0-110">Property value</span></span>

<span data-ttu-id="312d0-111">System. String qui est l’État.</span><span class="sxs-lookup"><span data-stu-id="312d0-111">The System.String that is the status.</span></span>

## <a name="remarks"></a><span data-ttu-id="312d0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="312d0-112">Remarks</span></span>

<span data-ttu-id="312d0-113">Les valeurs contenues dans cette propriété sont sujettes à modification à tout moment et doivent être utilisées à des fins d’affichage uniquement.</span><span class="sxs-lookup"><span data-stu-id="312d0-113">The values contained in this property are subject to change at any time, and should be used for display purposes only.</span></span>

<span data-ttu-id="312d0-114">AxWindowsMediaPlayer. L’événement **statuschange** est déclenché à chaque modification de la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="312d0-114">The AxWindowsMediaPlayer.**StatusChange** event is fired whenever this property changes value.</span></span>

## <a name="requirements"></a><span data-ttu-id="312d0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="312d0-115">Requirements</span></span>



| <span data-ttu-id="312d0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="312d0-116">Requirement</span></span> | <span data-ttu-id="312d0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="312d0-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="312d0-118">Version</span><span class="sxs-lookup"><span data-stu-id="312d0-118">Version</span></span><br/>   | <span data-ttu-id="312d0-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="312d0-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="312d0-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="312d0-120">Namespace</span></span><br/> | <span data-ttu-id="312d0-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="312d0-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="312d0-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="312d0-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="312d0-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="312d0-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="312d0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="312d0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="312d0-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="312d0-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="312d0-126">**Événement AxWindowsMediaPlayer. StatusChange (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="312d0-126">**AxWindowsMediaPlayer.StatusChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





