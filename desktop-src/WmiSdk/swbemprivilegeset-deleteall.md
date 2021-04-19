---
description: La méthode DeleteAll de l’objet SWbemPrivilegeSet supprime tous les privilèges de la collection, ce qui la vide.
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: SWbemPrivilegeSet. DeleteAll, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544307"
---
# <a name="swbemprivilegesetdeleteall-method"></a><span data-ttu-id="5efd2-103">SWbemPrivilegeSet. DeleteAll, méthode</span><span class="sxs-lookup"><span data-stu-id="5efd2-103">SWbemPrivilegeSet.DeleteAll method</span></span>

<span data-ttu-id="5efd2-104">La méthode **DeleteAll** de l’objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) supprime tous les privilèges de la collection, ce qui la vide.</span><span class="sxs-lookup"><span data-stu-id="5efd2-104">The **DeleteAll** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object removes all privileges from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="5efd2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5efd2-105">Syntax</span></span>


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="5efd2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5efd2-106">Parameters</span></span>

<span data-ttu-id="5efd2-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5efd2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5efd2-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5efd2-108">Return value</span></span>

<span data-ttu-id="5efd2-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5efd2-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5efd2-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5efd2-110">Error codes</span></span>

<span data-ttu-id="5efd2-111">À la fin de la méthode **DeleteAll** , l’objet **Err** peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5efd2-111">Upon the completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="5efd2-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5efd2-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5efd2-113">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5efd2-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5efd2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5efd2-114">Requirements</span></span>



| <span data-ttu-id="5efd2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5efd2-115">Requirement</span></span> | <span data-ttu-id="5efd2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5efd2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5efd2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5efd2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5efd2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5efd2-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5efd2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5efd2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5efd2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5efd2-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5efd2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5efd2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5efd2-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5efd2-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5efd2-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5efd2-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="5efd2-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5efd2-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5efd2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5efd2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5efd2-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5efd2-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5efd2-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="5efd2-127">CLSID</span></span><br/>                    | <span data-ttu-id="5efd2-128">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="5efd2-128">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="5efd2-129">IID</span><span class="sxs-lookup"><span data-stu-id="5efd2-129">IID</span></span><br/>                      | <span data-ttu-id="5efd2-130">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="5efd2-130">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="5efd2-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5efd2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5efd2-132">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="5efd2-132">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="5efd2-133">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="5efd2-133">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="5efd2-134">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="5efd2-134">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




