---
description: La propriété DisplayName d’un objet SWbemPrivilege est une chaîne qui affiche une description d’un objet SWbemPrivilege.
ms.assetid: 9ed91a6a-e513-4a72-b8a9-3180e42b811f
ms.tgt_platform: multiple
title: Propriété SWbemPrivilege. DisplayName (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.DisplayName
- ISWbemPrivilege.DisplayName
- ISWbemPrivilege.get_DisplayName
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bb45bdce52b1930f1893f7716d573033627e0cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524124"
---
# <a name="swbemprivilegedisplayname-property"></a><span data-ttu-id="25f11-103">SWbemPrivilege. DisplayName, propriété</span><span class="sxs-lookup"><span data-stu-id="25f11-103">SWbemPrivilege.DisplayName property</span></span>

<span data-ttu-id="25f11-104">La propriété **DisplayName** d’un objet [**SWbemPrivilege**](swbemprivilege.md) est une chaîne qui affiche une description d’un objet **SWbemPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="25f11-104">The **DisplayName** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that displays a description of an **SWbemPrivilege** object.</span></span> <span data-ttu-id="25f11-105">Par exemple, le privilège qui contrôle si un utilisateur peut exécuter la méthode Shutdown d’un objet a la chaîne « arrêter le système » dans la propriété **SWbemPrivilege. DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="25f11-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "Shut down the system" string in the **SWbemPrivilege.DisplayName** property.</span></span> <span data-ttu-id="25f11-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="25f11-106">This property is read-only.</span></span>

<span data-ttu-id="25f11-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="25f11-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="25f11-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="25f11-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f11-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25f11-109">Syntax</span></span>


```VB
SWbemPrivilege.DisplayName As 
```



## <a name="property-value"></a><span data-ttu-id="25f11-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="25f11-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="25f11-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25f11-111">Requirements</span></span>



| <span data-ttu-id="25f11-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25f11-112">Requirement</span></span> | <span data-ttu-id="25f11-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="25f11-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25f11-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25f11-114">Minimum supported client</span></span><br/> | <span data-ttu-id="25f11-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25f11-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25f11-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25f11-116">Minimum supported server</span></span><br/> | <span data-ttu-id="25f11-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25f11-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25f11-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="25f11-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f11-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="25f11-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="25f11-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="25f11-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="25f11-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="25f11-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="25f11-122">DLL</span><span class="sxs-lookup"><span data-stu-id="25f11-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25f11-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25f11-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="25f11-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="25f11-124">CLSID</span></span><br/>                    | <span data-ttu-id="25f11-125">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="25f11-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="25f11-126">IID</span><span class="sxs-lookup"><span data-stu-id="25f11-126">IID</span></span><br/>                      | <span data-ttu-id="25f11-127">IID \_ ISWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="25f11-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




