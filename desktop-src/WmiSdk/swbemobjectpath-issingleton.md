---
description: La propriété IsSingleton de l’objet SWbemObjectPath est une valeur booléenne qui indique si ce chemin représente une instance singleton. Une instance singleton est une instance d’une classe qui ne peut jamais avoir plus d’une instance. Cette propriété est en lecture seule.
ms.assetid: 0d0533be-89fe-4ab6-bafa-2da6195ff02c
ms.tgt_platform: multiple
title: SWbemObjectPath. IsSingleton, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.IsSingleton
- ISWbemObjectPath.IsSingleton
- ISWbemObjectPath.get_IsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bd267c3d8ad36459a04b835cb2f130c3e98420a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210546"
---
# <a name="swbemobjectpathissingleton-property"></a><span data-ttu-id="16b71-105">SWbemObjectPath. IsSingleton, propriété</span><span class="sxs-lookup"><span data-stu-id="16b71-105">SWbemObjectPath.IsSingleton property</span></span>

<span data-ttu-id="16b71-106">La propriété **IsSingleton** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) est une valeur booléenne qui indique si ce chemin représente une instance singleton.</span><span class="sxs-lookup"><span data-stu-id="16b71-106">The **IsSingleton** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is a Boolean value that indicates if this path represents a singleton instance.</span></span> <span data-ttu-id="16b71-107">Une instance singleton est une instance d’une classe qui ne peut jamais avoir plus d’une instance.</span><span class="sxs-lookup"><span data-stu-id="16b71-107">A singleton instance is an instance of a class that can never have more than one instance.</span></span> <span data-ttu-id="16b71-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="16b71-108">This property is read-only.</span></span>

<span data-ttu-id="16b71-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="16b71-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="16b71-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="16b71-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b71-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16b71-111">Syntax</span></span>


```VB
SWbemObjectPath.IsSingleton As Boolean
```



## <a name="property-value"></a><span data-ttu-id="16b71-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="16b71-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="16b71-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16b71-113">Requirements</span></span>



| <span data-ttu-id="16b71-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16b71-114">Requirement</span></span> | <span data-ttu-id="16b71-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="16b71-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16b71-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16b71-116">Minimum supported client</span></span><br/> | <span data-ttu-id="16b71-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16b71-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16b71-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16b71-118">Minimum supported server</span></span><br/> | <span data-ttu-id="16b71-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16b71-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16b71-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="16b71-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="16b71-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b71-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="16b71-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="16b71-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="16b71-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="16b71-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="16b71-124">DLL</span><span class="sxs-lookup"><span data-stu-id="16b71-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16b71-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16b71-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="16b71-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="16b71-126">CLSID</span></span><br/>                    | <span data-ttu-id="16b71-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="16b71-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="16b71-128">IID</span><span class="sxs-lookup"><span data-stu-id="16b71-128">IID</span></span><br/>                      | <span data-ttu-id="16b71-129">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="16b71-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




