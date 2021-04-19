---
title: AxWindowsMediaPlayer. cdromCollection, propriété
description: La propriété cdromCollection obtient une interface IWMPCdromCollection qui fournit l’accès à une collection de lecteurs de CD ou DVD.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- propriété cdromCollection lecteur Windows Media
- propriété cdromCollection lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété cdromCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522408"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a><span data-ttu-id="62d27-106">AxWindowsMediaPlayer. cdromCollection, propriété</span><span class="sxs-lookup"><span data-stu-id="62d27-106">AxWindowsMediaPlayer.cdromCollection property</span></span>

<span data-ttu-id="62d27-107">La propriété cdromCollection obtient une interface **IWMPCdromCollection** qui fournit l’accès à une collection de lecteurs de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="62d27-107">The cdromCollection property gets an **IWMPCdromCollection** interface that provides access to a collection of CD or DVD drives.</span></span>

<span data-ttu-id="62d27-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="62d27-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="62d27-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62d27-109">Syntax</span></span>


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a><span data-ttu-id="62d27-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="62d27-110">Property value</span></span>

<span data-ttu-id="62d27-111">Interface WMPLib. IWMPCdromCollection.</span><span class="sxs-lookup"><span data-stu-id="62d27-111">A WMPLib.IWMPCdromCollection interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="62d27-112">Notes</span><span class="sxs-lookup"><span data-stu-id="62d27-112">Remarks</span></span>

<span data-ttu-id="62d27-113">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="62d27-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="62d27-114">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="62d27-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62d27-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62d27-115">Requirements</span></span>



| <span data-ttu-id="62d27-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62d27-116">Requirement</span></span> | <span data-ttu-id="62d27-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="62d27-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62d27-118">Version</span><span class="sxs-lookup"><span data-stu-id="62d27-118">Version</span></span><br/>   | <span data-ttu-id="62d27-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="62d27-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="62d27-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="62d27-120">Namespace</span></span><br/> | <span data-ttu-id="62d27-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="62d27-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="62d27-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="62d27-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="62d27-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="62d27-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62d27-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62d27-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62d27-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="62d27-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="62d27-126">**Interface IWMPCdromCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="62d27-126">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="62d27-127">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="62d27-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="62d27-128">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="62d27-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





