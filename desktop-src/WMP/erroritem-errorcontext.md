---
title: ErrorItem.errorContext
description: La propriété errorContext récupère une valeur indiquant le contexte de l’erreur.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- Lecteur Windows Media ErrorItem. errorContext
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532517"
---
# <a name="erroritemerrorcontext"></a><span data-ttu-id="f2258-104">ErrorItem.errorContext</span><span class="sxs-lookup"><span data-stu-id="f2258-104">ErrorItem.errorContext</span></span>

<span data-ttu-id="f2258-105">La propriété **errorContext** récupère une valeur indiquant le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f2258-105">The **errorContext** property retrieves a value indicating the context of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a><span data-ttu-id="f2258-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="f2258-106">Possible Values</span></span>

<span data-ttu-id="f2258-107">Cette propriété est une **chaîne** en lecture seule qui représente le code de contexte d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f2258-107">This property is a read-only **String** that represents the error context code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2258-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f2258-108">Remarks</span></span>

<span data-ttu-id="f2258-109">Le contexte d’erreur est une information utilisée par Microsoft pour fournir des informations supplémentaires au personnel du support technique.</span><span class="sxs-lookup"><span data-stu-id="f2258-109">The error context is information that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="f2258-110">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="f2258-110">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2258-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2258-111">Requirements</span></span>



| <span data-ttu-id="f2258-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2258-112">Requirement</span></span> | <span data-ttu-id="f2258-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2258-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2258-114">Version</span><span class="sxs-lookup"><span data-stu-id="f2258-114">Version</span></span><br/> | <span data-ttu-id="f2258-115">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="f2258-115">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="f2258-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f2258-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="f2258-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2258-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2258-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2258-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2258-119">**Objet ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="f2258-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





