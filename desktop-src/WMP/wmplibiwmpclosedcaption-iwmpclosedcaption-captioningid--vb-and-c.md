---
title: IWMPClosedCaption propriété captioningId
description: La propriété IWMPClosedCaption obtient ou définit le nom de l’élément HTML affichant le sous-titrage.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- propriété captioningId lecteur Windows Media
- propriété captioningId lecteur Windows Media, interface IWMPClosedCaption
- Interface IWMPClosedCaption lecteur Windows Media, propriété captioningId
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540516"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a><span data-ttu-id="63462-106">IWMPClosedCaption :: captioningId, propriété</span><span class="sxs-lookup"><span data-stu-id="63462-106">IWMPClosedCaption::captioningId property</span></span>

<span data-ttu-id="63462-107">La propriété **IWMPClosedCaption** obtient ou définit le nom de l’élément HTML affichant le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="63462-107">The **IWMPClosedCaption** property gets or sets the name of the HTML element displaying the captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="63462-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63462-108">Syntax</span></span>


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a><span data-ttu-id="63462-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="63462-109">Property value</span></span>

<span data-ttu-id="63462-110">**System. String** qui correspond à l’ID de l’élément HTML.</span><span class="sxs-lookup"><span data-stu-id="63462-110">The **System.String** that is the ID of the HTML element.</span></span>

## <a name="remarks"></a><span data-ttu-id="63462-111">Notes</span><span class="sxs-lookup"><span data-stu-id="63462-111">Remarks</span></span>

<span data-ttu-id="63462-112">Le nom d’élément spécifié peut être n’importe quel élément HTML dans la page Web, à condition qu’il prenne en charge l’attribut **InnerHtml** .</span><span class="sxs-lookup"><span data-stu-id="63462-112">The element name specified can be any HTML element in the webpage as long as it supports the **innerHTML** attribute.</span></span> <span data-ttu-id="63462-113">Si la page Web contient plusieurs frames, le nom de l’élément ne peut faire référence qu’à un élément dans le même frame que le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="63462-113">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="63462-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63462-114">Requirements</span></span>



| <span data-ttu-id="63462-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63462-115">Requirement</span></span> | <span data-ttu-id="63462-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="63462-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63462-117">Version</span><span class="sxs-lookup"><span data-stu-id="63462-117">Version</span></span><br/>   | <span data-ttu-id="63462-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="63462-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="63462-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63462-119">Namespace</span></span><br/> | <span data-ttu-id="63462-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="63462-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="63462-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="63462-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="63462-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="63462-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63462-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63462-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63462-124">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="63462-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="63462-125">**Interface IWMPClosedCaption (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="63462-125">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="63462-126">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="63462-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





