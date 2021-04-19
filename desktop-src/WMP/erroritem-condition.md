---
title: ErrorItem. condition
description: La propriété condition récupère une valeur indiquant la condition de l’erreur.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- Lecteur Windows Media ErrorItem. condition
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537834"
---
# <a name="erroritemcondition"></a><span data-ttu-id="ae030-104">ErrorItem. condition</span><span class="sxs-lookup"><span data-stu-id="ae030-104">ErrorItem.condition</span></span>

<span data-ttu-id="ae030-105">La propriété **condition** récupère une valeur indiquant la condition de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ae030-105">The **condition** property retrieves a value indicating the condition for the error.</span></span>

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a><span data-ttu-id="ae030-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ae030-106">Possible Values</span></span>

<span data-ttu-id="ae030-107">Cette propriété est un **nombre** en lecture seule (**long**) qui représente le code de condition.</span><span class="sxs-lookup"><span data-stu-id="ae030-107">This property is a read-only **Number** (**long**) that represents the condition code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae030-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ae030-108">Remarks</span></span>

<span data-ttu-id="ae030-109">Le code de condition est une valeur utilisée par Microsoft pour fournir des informations supplémentaires au personnel du support technique.</span><span class="sxs-lookup"><span data-stu-id="ae030-109">The condition code is a value that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="ae030-110">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours 0.</span><span class="sxs-lookup"><span data-stu-id="ae030-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae030-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae030-111">Requirements</span></span>



| <span data-ttu-id="ae030-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae030-112">Requirement</span></span> | <span data-ttu-id="ae030-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae030-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae030-114">Version</span><span class="sxs-lookup"><span data-stu-id="ae030-114">Version</span></span><br/> | <span data-ttu-id="ae030-115">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ae030-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="ae030-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ae030-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="ae030-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae030-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae030-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae030-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae030-119">**Objet ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="ae030-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





