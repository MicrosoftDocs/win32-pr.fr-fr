---
description: La propriété IsEnabled d’un objet SWbemPrivilege est une valeur booléenne que vous utilisez pour activer ou désactiver ce privilège. Pour plus d’informations sur les conséquences de l’activation de privilèges spécifiques, consultez exécution avec des privilèges spéciaux.
ms.assetid: 282c8865-ba0d-4e82-be05-96a940036590
ms.tgt_platform: multiple
title: Propriété SWbemPrivilege. IsEnabled (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.IsEnabled
- ISWbemPrivilege.IsEnabled
- ISWbemPrivilege.get_IsEnabled
- ISWbemPrivilege.put_IsEnabled
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ec27b2344c42dca56ac629144f6edc402f81ea4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517766"
---
# <a name="swbemprivilegeisenabled-property"></a><span data-ttu-id="fe06d-104">SWbemPrivilege. IsEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="fe06d-104">SWbemPrivilege.IsEnabled property</span></span>

<span data-ttu-id="fe06d-105">La propriété **IsEnabled** d’un objet [**SWbemPrivilege**](swbemprivilege.md) est une valeur booléenne que vous utilisez pour activer ou désactiver ce privilège.</span><span class="sxs-lookup"><span data-stu-id="fe06d-105">The **IsEnabled** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a Boolean value that you use to enable or disable this privilege.</span></span> <span data-ttu-id="fe06d-106">Pour plus d’informations sur les conséquences de l’activation de privilèges spécifiques, consultez [**exécution avec des privilèges spéciaux**](swbemsecurity-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="fe06d-106">For more information about the consequences of enabling specific privileges, see [**Running with Special Privileges**](swbemsecurity-privileges.md).</span></span>

<span data-ttu-id="fe06d-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fe06d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="fe06d-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fe06d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe06d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe06d-109">Syntax</span></span>


```VB
SWbemPrivilege.IsEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="fe06d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fe06d-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="fe06d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe06d-111">Requirements</span></span>



| <span data-ttu-id="fe06d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe06d-112">Requirement</span></span> | <span data-ttu-id="fe06d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe06d-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe06d-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe06d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fe06d-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe06d-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe06d-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe06d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fe06d-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe06d-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe06d-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe06d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe06d-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe06d-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe06d-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fe06d-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="fe06d-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fe06d-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fe06d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fe06d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe06d-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe06d-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fe06d-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="fe06d-124">CLSID</span></span><br/>                    | <span data-ttu-id="fe06d-125">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="fe06d-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="fe06d-126">IID</span><span class="sxs-lookup"><span data-stu-id="fe06d-126">IID</span></span><br/>                      | <span data-ttu-id="fe06d-127">IID \_ ISWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="fe06d-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




