---
description: La propriété Name d’un objet SWbemPrivilege est une chaîne qui décrit de façon unique un privilège.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: Propriété SWbemPrivilege.Name (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210541"
---
# <a name="swbemprivilegename-property"></a><span data-ttu-id="411db-103">Propriété SWbemPrivilege.Name</span><span class="sxs-lookup"><span data-stu-id="411db-103">SWbemPrivilege.Name property</span></span>

<span data-ttu-id="411db-104">La propriété **Name** d’un objet [**SWbemPrivilege**](swbemprivilege.md) est une chaîne qui décrit de façon unique un privilège.</span><span class="sxs-lookup"><span data-stu-id="411db-104">The **Name** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that uniquely describes a privilege.</span></span> <span data-ttu-id="411db-105">Par exemple, le privilège qui contrôle si un utilisateur peut exécuter la méthode Shutdown d’un objet possède la chaîne « SeShutdownPrivilege » dans la propriété **SWbemPrivilege.Name** .</span><span class="sxs-lookup"><span data-stu-id="411db-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "SeShutdownPrivilege" string in the **SWbemPrivilege.Name** property.</span></span> <span data-ttu-id="411db-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="411db-106">This property is read-only.</span></span>

<span data-ttu-id="411db-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="411db-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="411db-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="411db-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="411db-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="411db-109">Syntax</span></span>


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a><span data-ttu-id="411db-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="411db-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="411db-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="411db-111">Requirements</span></span>



| <span data-ttu-id="411db-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="411db-112">Requirement</span></span> | <span data-ttu-id="411db-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="411db-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="411db-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="411db-114">Minimum supported client</span></span><br/> | <span data-ttu-id="411db-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="411db-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="411db-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="411db-116">Minimum supported server</span></span><br/> | <span data-ttu-id="411db-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="411db-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="411db-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="411db-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="411db-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="411db-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="411db-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="411db-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="411db-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="411db-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="411db-122">DLL</span><span class="sxs-lookup"><span data-stu-id="411db-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="411db-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="411db-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="411db-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="411db-124">CLSID</span></span><br/>                    | <span data-ttu-id="411db-125">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="411db-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="411db-126">IID</span><span class="sxs-lookup"><span data-stu-id="411db-126">IID</span></span><br/>                      | <span data-ttu-id="411db-127">IID \_ ISWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="411db-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




