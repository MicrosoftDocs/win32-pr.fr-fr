---
description: La propriété Value de l’objet SWbemNamedValue retourne la valeur de type variant d’un élément SWbemNamedValue.
ms.assetid: f9609bd2-893a-48c3-9faa-93cd033c4109
ms.tgt_platform: multiple
title: SWbemNamedValue. Value, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue.Value
- ISWbemNamedValue.Value
- ISWbemNamedValue.get_Value
- ISWbemNamedValue.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bf63b15a27c1149341200f29e938bdba6cd7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114871"
---
# <a name="swbemnamedvaluevalue-property"></a><span data-ttu-id="cc530-103">SWbemNamedValue. Value (propriété)</span><span class="sxs-lookup"><span data-stu-id="cc530-103">SWbemNamedValue.Value property</span></span>

<span data-ttu-id="cc530-104">La propriété **value** de l’objet [**SWbemNamedValue**](swbemnamedvalue.md) retourne la valeur de type variant d’un élément **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="cc530-104">The **Value** property of the [**SWbemNamedValue**](swbemnamedvalue.md) object returns the variant value of an **SWbemNamedValue** item.</span></span> <span data-ttu-id="cc530-105">Il s’agit de la propriété par défaut pour les objets **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="cc530-105">This is the default property for **SWbemNamedValue** objects.</span></span> <span data-ttu-id="cc530-106">Les modifications apportées à la propriété value sont répercutées automatiquement dans la collection [**SWbemNamedValueSet**](swbemnamedvalueset.md) à laquelle appartient l’objet **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="cc530-106">Changes made to the value property are reflected automatically in the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection to which the **SWbemNamedValue** object belongs.</span></span>

<span data-ttu-id="cc530-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="cc530-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="cc530-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cc530-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc530-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc530-109">Syntax</span></span>


```VB
SWbemNamedValue.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="cc530-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cc530-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="cc530-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc530-111">Requirements</span></span>



| <span data-ttu-id="cc530-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc530-112">Requirement</span></span> | <span data-ttu-id="cc530-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc530-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc530-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc530-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cc530-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc530-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc530-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc530-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cc530-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc530-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc530-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc530-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc530-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc530-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc530-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cc530-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="cc530-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cc530-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cc530-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cc530-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc530-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc530-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cc530-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="cc530-124">CLSID</span></span><br/>                    | <span data-ttu-id="cc530-125">CLSID \_ SWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="cc530-125">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="cc530-126">IID</span><span class="sxs-lookup"><span data-stu-id="cc530-126">IID</span></span><br/>                      | <span data-ttu-id="cc530-127">IID \_ ISWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="cc530-127">IID\_ISWbemNamedValue</span></span><br/>                                                        |



 

 




