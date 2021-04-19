---
title: ClosedCaption.SAMIStyleCount
description: La propriété SAMIStyleCount récupère le nombre de styles pris en charge par le fichier SAMI actuel.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- Lecteur Windows Media ClosedCaption. SAMIStyleCount
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528624"
---
# <a name="closedcaptionsamistylecount"></a><span data-ttu-id="154be-104">ClosedCaption.SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="154be-104">ClosedCaption.SAMIStyleCount</span></span>

<span data-ttu-id="154be-105">La propriété **SAMIStyleCount** récupère le nombre de styles pris en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="154be-105">The **SAMIStyleCount** property retrieves the number of styles supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a><span data-ttu-id="154be-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="154be-106">Possible Values</span></span>

<span data-ttu-id="154be-107">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="154be-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="154be-108">Notes</span><span class="sxs-lookup"><span data-stu-id="154be-108">Remarks</span></span>

<span data-ttu-id="154be-109">Cette méthode ne peut pas être utilisée tant qu’un fichier multimédia numérique n’est pas ouvert (*lecteur*.**openState** est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="154be-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="154be-110">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours 0.</span><span class="sxs-lookup"><span data-stu-id="154be-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="154be-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="154be-111">Requirements</span></span>



| <span data-ttu-id="154be-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="154be-112">Requirement</span></span> | <span data-ttu-id="154be-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="154be-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="154be-114">Version</span><span class="sxs-lookup"><span data-stu-id="154be-114">Version</span></span><br/> | <span data-ttu-id="154be-115">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="154be-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="154be-116">DLL</span><span class="sxs-lookup"><span data-stu-id="154be-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="154be-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="154be-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="154be-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="154be-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="154be-119">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="154be-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="154be-120">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="154be-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="154be-121">**ClosedCaption.getSAMIStyleName**</span><span class="sxs-lookup"><span data-stu-id="154be-121">**ClosedCaption.getSAMIStyleName**</span></span>](closedcaption-getsamistylename.md)
</dt> <dt>

[<span data-ttu-id="154be-122">**ClosedCaption.SAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="154be-122">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





