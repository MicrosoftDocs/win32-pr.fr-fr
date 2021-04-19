---
title: IWMPClosedCaption propriété SAMILang
description: La propriété SAMILang obtient ou définit la langue affichée pour le sous-titrage.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Propriété SAMILang lecteur Windows Media
- Propriété SAMILang lecteur Windows Media, interface IWMPClosedCaption
- Interface IWMPClosedCaption lecteur Windows Media, propriété SAMILang
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521730"
---
# <a name="iwmpclosedcaptionsamilang-property"></a><span data-ttu-id="de3e3-106">IWMPClosedCaption :: SAMILang, propriété</span><span class="sxs-lookup"><span data-stu-id="de3e3-106">IWMPClosedCaption::SAMILang property</span></span>

<span data-ttu-id="de3e3-107">La propriété **SAMILang** obtient ou définit la langue affichée pour le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="de3e3-107">The **SAMILang** property gets or sets the language displayed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3e3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de3e3-108">Syntax</span></span>


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a><span data-ttu-id="de3e3-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="de3e3-109">Property value</span></span>

<span data-ttu-id="de3e3-110">**System. String** qui est le nom spécifié dans l’identificateur de langue d’un fichier sami.</span><span class="sxs-lookup"><span data-stu-id="de3e3-110">The **System.String** that is the name specified in the language identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="de3e3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="de3e3-111">Remarks</span></span>

<span data-ttu-id="de3e3-112">Un fichier SAMI peut contenir du texte pour une ou plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="de3e3-112">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="de3e3-113">Les langues disponibles pour le sous-titrage sont définies entre les balises <STYLE> et </STYLE> dans le fichier sami.</span><span class="sxs-lookup"><span data-stu-id="de3e3-113">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="de3e3-114">Un identificateur de langue est spécifié avec une chaîne alphanumérique unique précédée d’un point (.).</span><span class="sxs-lookup"><span data-stu-id="de3e3-114">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="de3e3-115">Le nom spécifié pour une langue peut être n’importe quelle chaîne.</span><span class="sxs-lookup"><span data-stu-id="de3e3-115">The name specified for a language can be any string.</span></span> <span data-ttu-id="de3e3-116">Par exemple, les éléments suivants peuvent être utilisés pour définir l’anglais des États-Unis :</span><span class="sxs-lookup"><span data-stu-id="de3e3-116">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



<span data-ttu-id="de3e3-117">Si aucune langue SAMI n’est spécifiée, la première langue définie dans le fichier SAMI est utilisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="de3e3-117">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="de3e3-118">La chaîne que vous définissez à l’aide de **SAMILang** doit correspondre à l’attribut **Name** dans le spécificateur de langage.</span><span class="sxs-lookup"><span data-stu-id="de3e3-118">The string you set using **SAMILang** must match the **Name** attribute in the language specifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="de3e3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de3e3-119">Requirements</span></span>



| <span data-ttu-id="de3e3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de3e3-120">Requirement</span></span> | <span data-ttu-id="de3e3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="de3e3-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3e3-122">Version</span><span class="sxs-lookup"><span data-stu-id="de3e3-122">Version</span></span><br/>   | <span data-ttu-id="de3e3-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="de3e3-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="de3e3-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="de3e3-124">Namespace</span></span><br/> | <span data-ttu-id="de3e3-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="de3e3-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="de3e3-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="de3e3-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="de3e3-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="de3e3-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3e3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de3e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3e3-129">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="de3e3-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="de3e3-130">**Interface IWMPClosedCaption (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="de3e3-130">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="de3e3-131">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="de3e3-131">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





