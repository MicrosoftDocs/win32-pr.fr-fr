---
description: La propriété Path de l’objet SWbemObjectPath contient le chemin d’accès absolu. Il est identique à la \_ \_ propriété Path de l’API com. Il s’agit de la propriété par défaut de cet objet.
ms.assetid: cc0d2c56-bb69-4008-8688-0166714ea5fd
ms.tgt_platform: multiple
title: SWbemObjectPath. Path, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Path
- ISWbemObjectPath.Path
- ISWbemObjectPath.get_Path
- ISWbemObjectPath.put_Path
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02a3dfbf6dbc24434ad4d9807ab5e39dbc121043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534587"
---
# <a name="swbemobjectpathpath-property"></a><span data-ttu-id="9e14a-105">SWbemObjectPath. Path, propriété</span><span class="sxs-lookup"><span data-stu-id="9e14a-105">SWbemObjectPath.Path property</span></span>

<span data-ttu-id="9e14a-106">La propriété **path** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) contient le chemin d’accès absolu.</span><span class="sxs-lookup"><span data-stu-id="9e14a-106">The **Path** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the absolute path.</span></span> <span data-ttu-id="9e14a-107">Il est identique à la propriété [ \_ \_ path](wmi-system-properties.md) de l’API com.</span><span class="sxs-lookup"><span data-stu-id="9e14a-107">This is the same as the [\_\_Path](wmi-system-properties.md) property in the COM API.</span></span> <span data-ttu-id="9e14a-108">Il s’agit de la propriété par défaut de cet objet.</span><span class="sxs-lookup"><span data-stu-id="9e14a-108">This is the default property of this object.</span></span>

<span data-ttu-id="9e14a-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9e14a-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="9e14a-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9e14a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e14a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e14a-111">Syntax</span></span>


```VB
SWbemObjectPath.Path As String
```



## <a name="property-value"></a><span data-ttu-id="9e14a-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9e14a-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="9e14a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e14a-113">Requirements</span></span>



| <span data-ttu-id="9e14a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e14a-114">Requirement</span></span> | <span data-ttu-id="9e14a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e14a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e14a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e14a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9e14a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e14a-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e14a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e14a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9e14a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e14a-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e14a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e14a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e14a-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e14a-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e14a-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9e14a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e14a-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9e14a-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9e14a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9e14a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e14a-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e14a-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e14a-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="9e14a-126">CLSID</span></span><br/>                    | <span data-ttu-id="9e14a-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="9e14a-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="9e14a-128">IID</span><span class="sxs-lookup"><span data-stu-id="9e14a-128">IID</span></span><br/>                      | <span data-ttu-id="9e14a-129">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="9e14a-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




