---
title: IWMPClosedCaption propriété SAMIStyle
description: La propriété SAMIStyle obtient ou définit le style de sous-titrage.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Propriété SAMIStyle lecteur Windows Media
- Propriété SAMIStyle lecteur Windows Media, interface IWMPClosedCaption
- Interface IWMPClosedCaption lecteur Windows Media, propriété SAMIStyle
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526856"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a><span data-ttu-id="b50ad-106">IWMPClosedCaption :: SAMIStyle, propriété</span><span class="sxs-lookup"><span data-stu-id="b50ad-106">IWMPClosedCaption::SAMIStyle property</span></span>

<span data-ttu-id="b50ad-107">La propriété **SAMIStyle** obtient ou définit le style de sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="b50ad-107">The **SAMIStyle** property gets or sets the closed captioning style.</span></span>

## <a name="syntax"></a><span data-ttu-id="b50ad-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b50ad-108">Syntax</span></span>


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a><span data-ttu-id="b50ad-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b50ad-109">Property value</span></span>

<span data-ttu-id="b50ad-110">**System. String** qui est le nom spécifié dans l’identificateur de style d’un fichier sami.</span><span class="sxs-lookup"><span data-stu-id="b50ad-110">The **System.String** that is the name specified in the style identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="b50ad-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b50ad-111">Remarks</span></span>

<span data-ttu-id="b50ad-112">Un fichier SAMI peut contenir plusieurs définitions de style de format.</span><span class="sxs-lookup"><span data-stu-id="b50ad-112">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="b50ad-113">Les styles SAMI sont définis entre les balises <STYLE> et </STYLE> dans le fichier sami.</span><span class="sxs-lookup"><span data-stu-id="b50ad-113">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="b50ad-114">Un style est défini avec une chaîne de texte précédée d’un \# caractère.</span><span class="sxs-lookup"><span data-stu-id="b50ad-114">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="b50ad-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b50ad-115">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



<span data-ttu-id="b50ad-116">Cela spécifie un style qui produit une police particulière.</span><span class="sxs-lookup"><span data-stu-id="b50ad-116">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="b50ad-117">Si aucun style SAMI n’est spécifié, le premier style défini dans le fichier SAMI est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="b50ad-117">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="b50ad-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b50ad-118">Requirements</span></span>



| <span data-ttu-id="b50ad-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b50ad-119">Requirement</span></span> | <span data-ttu-id="b50ad-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b50ad-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b50ad-121">Version</span><span class="sxs-lookup"><span data-stu-id="b50ad-121">Version</span></span><br/>   | <span data-ttu-id="b50ad-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b50ad-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b50ad-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b50ad-123">Namespace</span></span><br/> | <span data-ttu-id="b50ad-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b50ad-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b50ad-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="b50ad-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b50ad-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b50ad-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b50ad-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b50ad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b50ad-128">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="b50ad-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="b50ad-129">**Interface IWMPClosedCaption (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b50ad-129">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b50ad-130">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b50ad-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





