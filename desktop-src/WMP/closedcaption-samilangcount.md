---
title: ClosedCaption.SAMILangCount
description: La propriété SAMILangCount récupère le nombre de langues prises en charge par le fichier SAMI actuel.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- Lecteur Windows Media ClosedCaption. SAMILangCount
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528693"
---
# <a name="closedcaptionsamilangcount"></a><span data-ttu-id="33dbc-104">ClosedCaption.SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="33dbc-104">ClosedCaption.SAMILangCount</span></span>

<span data-ttu-id="33dbc-105">La propriété **SAMILangCount** récupère le nombre de langues prises en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="33dbc-105">The **SAMILangCount** property retrieves the number of languages supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a><span data-ttu-id="33dbc-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="33dbc-106">Possible Values</span></span>

<span data-ttu-id="33dbc-107">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="33dbc-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="33dbc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="33dbc-108">Remarks</span></span>

<span data-ttu-id="33dbc-109">Cette méthode ne peut pas être utilisée tant qu’un fichier multimédia numérique n’est pas ouvert (*lecteur*.**openState** est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="33dbc-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="33dbc-110">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours 0.</span><span class="sxs-lookup"><span data-stu-id="33dbc-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="33dbc-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33dbc-111">Requirements</span></span>



| <span data-ttu-id="33dbc-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33dbc-112">Requirement</span></span> | <span data-ttu-id="33dbc-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="33dbc-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33dbc-114">Version</span><span class="sxs-lookup"><span data-stu-id="33dbc-114">Version</span></span><br/> | <span data-ttu-id="33dbc-115">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="33dbc-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="33dbc-116">DLL</span><span class="sxs-lookup"><span data-stu-id="33dbc-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="33dbc-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33dbc-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33dbc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33dbc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33dbc-119">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="33dbc-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="33dbc-120">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="33dbc-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="33dbc-121">**ClosedCaption.getSAMILangName**</span><span class="sxs-lookup"><span data-stu-id="33dbc-121">**ClosedCaption.getSAMILangName**</span></span>](closedcaption-getsamilangname.md)
</dt> <dt>

[<span data-ttu-id="33dbc-122">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="33dbc-122">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





