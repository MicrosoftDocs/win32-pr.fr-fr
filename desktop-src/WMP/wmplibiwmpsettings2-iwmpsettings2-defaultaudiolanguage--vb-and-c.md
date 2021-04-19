---
title: IWMPSettings2 propriété defaultAudioLanguage
description: La propriété defaultAudioLanguage obtient l’identificateur de paramètres régionaux (LCID) de la langue audio par défaut spécifiée dans le lecteur Windows Media.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- propriété defaultAudioLanguage lecteur Windows Media
- propriété defaultAudioLanguage lecteur Windows Media, interface IWMPSettings2
- Interface IWMPSettings2 lecteur Windows Media, propriété defaultAudioLanguage
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537481"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a><span data-ttu-id="b6f2c-106">IWMPSettings2 ::d propriété efaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="b6f2c-106">IWMPSettings2::defaultAudioLanguage property</span></span>

<span data-ttu-id="b6f2c-107">La propriété **defaultAudioLanguage** obtient l’identificateur de paramètres régionaux (LCID) de la langue audio par défaut spécifiée dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b6f2c-107">The **defaultAudioLanguage** property gets the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>

<span data-ttu-id="b6f2c-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b6f2c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f2c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6f2c-109">Syntax</span></span>


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="b6f2c-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b6f2c-110">Property value</span></span>

<span data-ttu-id="b6f2c-111">**System. Int32** qui est le LCID.</span><span class="sxs-lookup"><span data-stu-id="b6f2c-111">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6f2c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b6f2c-112">Remarks</span></span>

<span data-ttu-id="b6f2c-113">Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="b6f2c-113">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6f2c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6f2c-114">Requirements</span></span>



| <span data-ttu-id="b6f2c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6f2c-115">Requirement</span></span> | <span data-ttu-id="b6f2c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6f2c-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f2c-117">Version</span><span class="sxs-lookup"><span data-stu-id="b6f2c-117">Version</span></span><br/>   | <span data-ttu-id="b6f2c-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b6f2c-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b6f2c-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b6f2c-119">Namespace</span></span><br/> | <span data-ttu-id="b6f2c-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b6f2c-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b6f2c-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="b6f2c-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b6f2c-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b6f2c-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6f2c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6f2c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f2c-124">**IWMPControls3. currentAudioLanguage (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b6f2c-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6f2c-125">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b6f2c-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6f2c-126">**Interface IWMPSettings2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b6f2c-126">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





