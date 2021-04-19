---
title: IWMPControls3 propriété audioLanguageCount
description: La propriété audioLanguageCount obtient le nombre de langues audio prises en charge.
ms.assetid: 92e2093f-435b-4427-9f85-8c8ae76e0e2d
keywords:
- propriété audioLanguageCount lecteur Windows Media
- propriété audioLanguageCount lecteur Windows Media, interface IWMPControls3
- Interface IWMPControls3 lecteur Windows Media, propriété audioLanguageCount
topic_type:
- apiref
api_name:
- IWMPControls3.audioLanguageCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd397dec80a5ccb5f2085e3231782555efde8e39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540050"
---
# <a name="iwmpcontrols3audiolanguagecount-property"></a><span data-ttu-id="7cb6d-106">IWMPControls3 :: audioLanguageCount, propriété</span><span class="sxs-lookup"><span data-stu-id="7cb6d-106">IWMPControls3::audioLanguageCount property</span></span>

<span data-ttu-id="7cb6d-107">La propriété **audioLanguageCount** obtient le nombre de langues audio prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-107">The **audioLanguageCount** property gets the count of supported audio languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb6d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cb6d-108">Syntax</span></span>


```CSharp
public System.Int32 audioLanguageCount {get; set;}
```


```VB

Public ReadOnly Property audioLanguageCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="7cb6d-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7cb6d-109">Property value</span></span>

<span data-ttu-id="7cb6d-110">**System. Int32** qui est le nombre de langues audio prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-110">A **System.Int32** that is the count of supported audio languages.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb6d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7cb6d-111">Remarks</span></span>

<span data-ttu-id="7cb6d-112">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-112">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb6d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cb6d-113">Requirements</span></span>



| <span data-ttu-id="7cb6d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cb6d-114">Requirement</span></span> | <span data-ttu-id="7cb6d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb6d-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb6d-116">Version</span><span class="sxs-lookup"><span data-stu-id="7cb6d-116">Version</span></span><br/>   | <span data-ttu-id="7cb6d-117">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7cb6d-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7cb6d-118">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7cb6d-118">Namespace</span></span><br/> | <span data-ttu-id="7cb6d-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7cb6d-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7cb6d-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="7cb6d-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7cb6d-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7cb6d-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cb6d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cb6d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb6d-123">**Interface IWMPControls3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7cb6d-123">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7cb6d-124">**IWMPControls3. currentAudioLanguage (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7cb6d-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7cb6d-125">**IWMPControls3. currentAudioLanguageIndex (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7cb6d-125">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7cb6d-126">**IWMPControls3. getAudioLanguageDescription (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7cb6d-126">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7cb6d-127">**IWMPControls3. getAudioLanguageID (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7cb6d-127">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7cb6d-128">**IWMPControls3. getLanguageName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7cb6d-128">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





