---
description: L’objet SWbemPrivilege représente un privilège unique. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Objet SWbemPrivilege (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c3be448b4088011cd4d628a7d98b448af550b010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042760"
---
# <a name="swbemprivilege-object"></a><span data-ttu-id="3c2ed-104">Objet SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="3c2ed-104">SWbemPrivilege object</span></span>

<span data-ttu-id="3c2ed-105">L’objet **SWbemPrivilege** représente un privilège unique.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-105">The **SWbemPrivilege** object represents a single privilege.</span></span> <span data-ttu-id="3c2ed-106">Cet objet ne peut pas être créé par l’appel VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="3c2ed-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="3c2ed-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3c2ed-107">Members</span></span>

<span data-ttu-id="3c2ed-108">L’objet **SWbemPrivilege** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3c2ed-108">The **SWbemPrivilege** object has these types of members:</span></span>

-   [<span data-ttu-id="3c2ed-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c2ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c2ed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c2ed-110">Properties</span></span>

<span data-ttu-id="3c2ed-111">L’objet **SWbemPrivilege** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-111">The **SWbemPrivilege** object has these properties.</span></span>



| <span data-ttu-id="3c2ed-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="3c2ed-112">Property</span></span>                                                     | <span data-ttu-id="3c2ed-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="3c2ed-113">Access type</span></span>           | <span data-ttu-id="3c2ed-114">Description</span><span class="sxs-lookup"><span data-stu-id="3c2ed-114">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="3c2ed-115">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="3c2ed-115">**Displayname**</span></span>](swbemprivilege-displayname.md)<br/> | <span data-ttu-id="3c2ed-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ed-116">Read-only</span></span><br/>  | <span data-ttu-id="3c2ed-117">Nom complet de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-117">Display name of this privilege.</span></span><br/>                                       |
| [<span data-ttu-id="3c2ed-118">**Identificateur**</span><span class="sxs-lookup"><span data-stu-id="3c2ed-118">**Identifier**</span></span>](swbemprivilege-identifier.md)<br/>   | <span data-ttu-id="3c2ed-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c2ed-119">Read/write</span></span><br/> | <span data-ttu-id="3c2ed-120">Entier qui représente le privilège qui est défini ou récupéré.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-120">Integer that represents the privilege that is being set or retrieved.</span></span><br/> |
| [<span data-ttu-id="3c2ed-121">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="3c2ed-121">**IsEnabled**</span></span>](swbemprivilege-isenabled.md)<br/>     | <span data-ttu-id="3c2ed-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c2ed-122">Read/write</span></span><br/> | <span data-ttu-id="3c2ed-123">Valeur booléenne qui indique si ce privilège est activé.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-123">Boolean value that indicates if this privilege is enabled.</span></span><br/>            |
| [<span data-ttu-id="3c2ed-124">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3c2ed-124">**Name**</span></span>](swbemprivilege-name.md)<br/>               | <span data-ttu-id="3c2ed-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ed-125">Read-only</span></span><br/>  | <span data-ttu-id="3c2ed-126">Nom de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-126">Name of this privilege.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="3c2ed-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c2ed-127">Requirements</span></span>



| <span data-ttu-id="3c2ed-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c2ed-128">Requirement</span></span> | <span data-ttu-id="3c2ed-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c2ed-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2ed-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c2ed-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2ed-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c2ed-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c2ed-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c2ed-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2ed-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c2ed-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c2ed-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c2ed-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c2ed-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ed-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c2ed-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3c2ed-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="3c2ed-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ed-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3c2ed-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3c2ed-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c2ed-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ed-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3c2ed-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="3c2ed-140">CLSID</span></span><br/>                    | <span data-ttu-id="3c2ed-141">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="3c2ed-141">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="3c2ed-142">IID</span><span class="sxs-lookup"><span data-stu-id="3c2ed-142">IID</span></span><br/>                      | <span data-ttu-id="3c2ed-143">IID \_ ISWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="3c2ed-143">IID\_ISWbemPrivilege</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="3c2ed-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c2ed-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2ed-145">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="3c2ed-145">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="3c2ed-146">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="3c2ed-146">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




