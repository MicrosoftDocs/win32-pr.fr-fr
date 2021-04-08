---
description: La propriété ParentNamespace de l’objet SWbemObjectPath contient le nom de l’espace de noms parent qui fait partie du chemin d’accès de l’objet. Cette propriété est en lecture seule.
ms.assetid: 506cf172-2c8b-48fe-bcdd-572bdca754a8
ms.tgt_platform: multiple
title: SWbemObjectPath. ParentNamespace, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.ParentNamespace
- ISWbemObjectPath.ParentNamespace
- ISWbemObjectPath.get_ParentNamespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e157b920f9c500fc4024da6facbe9781a7fa1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754989"
---
# <a name="swbemobjectpathparentnamespace-property"></a><span data-ttu-id="6b031-104">SWbemObjectPath. ParentNamespace, propriété</span><span class="sxs-lookup"><span data-stu-id="6b031-104">SWbemObjectPath.ParentNamespace property</span></span>

<span data-ttu-id="6b031-105">La propriété **ParentNamespace** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) contient le nom de l’espace de noms parent qui fait partie du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b031-105">The **ParentNamespace** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the name of the parent namespace that is part of the object path.</span></span> <span data-ttu-id="6b031-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6b031-106">This property is read-only.</span></span>

<span data-ttu-id="6b031-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6b031-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6b031-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6b031-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b031-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b031-109">Syntax</span></span>


```VB
SWbemObjectPath.ParentNamespace As String
```



## <a name="property-value"></a><span data-ttu-id="6b031-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6b031-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="6b031-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b031-111">Requirements</span></span>



| <span data-ttu-id="6b031-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b031-112">Requirement</span></span> | <span data-ttu-id="6b031-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b031-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b031-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b031-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6b031-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b031-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b031-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b031-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6b031-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b031-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b031-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b031-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b031-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b031-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b031-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6b031-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b031-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b031-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b031-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6b031-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b031-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b031-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6b031-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="6b031-124">CLSID</span></span><br/>                    | <span data-ttu-id="6b031-125">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="6b031-125">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="6b031-126">IID</span><span class="sxs-lookup"><span data-stu-id="6b031-126">IID</span></span><br/>                      | <span data-ttu-id="6b031-127">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="6b031-127">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




