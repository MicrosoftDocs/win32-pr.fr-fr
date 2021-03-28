---
description: Étend l’objet IShellDispatch avec diverses nouvelles fonctionnalités.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Objet IShellDispatch2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972387"
---
# <a name="ishelldispatch2-object"></a><span data-ttu-id="1b94c-103">Objet IShellDispatch2</span><span class="sxs-lookup"><span data-stu-id="1b94c-103">IShellDispatch2 object</span></span>

<span data-ttu-id="1b94c-104">Étend l’objet [**IShellDispatch**](ishelldispatch.md) avec diverses nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="1b94c-104">Extends the [**IShellDispatch**](ishelldispatch.md) object with a variety of new functionality.</span></span>

> [!Note]  
> <span data-ttu-id="1b94c-105">**IShellDispatch2** est implémenté et accessible via l’objet [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="1b94c-105">**IShellDispatch2** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="1b94c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1b94c-106">Members</span></span>

<span data-ttu-id="1b94c-107">L’objet **IShellDispatch2** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1b94c-107">The **IShellDispatch2** object has these types of members:</span></span>

-   [<span data-ttu-id="1b94c-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b94c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1b94c-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b94c-109">Methods</span></span>

<span data-ttu-id="1b94c-110">L’objet **IShellDispatch2** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1b94c-110">The **IShellDispatch2** object has these methods.</span></span>



| <span data-ttu-id="1b94c-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="1b94c-111">Method</span></span>                                                               | <span data-ttu-id="1b94c-112">Description</span><span class="sxs-lookup"><span data-stu-id="1b94c-112">Description</span></span>                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="1b94c-113">**CanStartStopService**</span><span class="sxs-lookup"><span data-stu-id="1b94c-113">**CanStartStopService**</span></span>](ishelldispatch2-canstartstopservice.md)   | <span data-ttu-id="1b94c-114">Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.</span><span class="sxs-lookup"><span data-stu-id="1b94c-114">Determines if the current user can start and stop the named service.</span></span><br/>    |
| [<span data-ttu-id="1b94c-115">**FindPrinter**</span><span class="sxs-lookup"><span data-stu-id="1b94c-115">**FindPrinter**</span></span>](ishelldispatch2-findprinter.md)                   | <span data-ttu-id="1b94c-116">Affiche la boîte de dialogue **Rechercher l’imprimante** .</span><span class="sxs-lookup"><span data-stu-id="1b94c-116">Displays the **Find Printer** dialog box.</span></span><br/>                               |
| [<span data-ttu-id="1b94c-117">**GetSystemInformation**</span><span class="sxs-lookup"><span data-stu-id="1b94c-117">**GetSystemInformation**</span></span>](ishelldispatch2-getsysteminformation.md) | <span data-ttu-id="1b94c-118">Récupère des informations système.</span><span class="sxs-lookup"><span data-stu-id="1b94c-118">Retrieves system information.</span></span><br/>                                           |
| [<span data-ttu-id="1b94c-119">**IsRestricted**</span><span class="sxs-lookup"><span data-stu-id="1b94c-119">**IsRestricted**</span></span>](ishelldispatch2-isrestricted.md)                 | <span data-ttu-id="1b94c-120">Récupère le paramètre de restriction d’un groupe à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="1b94c-120">Retrieves a group's restriction setting from the registry.</span></span><br/>              |
| [<span data-ttu-id="1b94c-121">**IsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="1b94c-121">**IsServiceRunning**</span></span>](ishelldispatch2-isservicerunning.md)         | <span data-ttu-id="1b94c-122">Retourne une valeur qui indique si un service particulier est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1b94c-122">Returns a value that indicates whether a particular service is running.</span></span><br/> |
| [<span data-ttu-id="1b94c-123">**ServiceStart**</span><span class="sxs-lookup"><span data-stu-id="1b94c-123">**ServiceStart**</span></span>](ishelldispatch2-servicestart.md)                 | <span data-ttu-id="1b94c-124">Démarre un service nommé.</span><span class="sxs-lookup"><span data-stu-id="1b94c-124">Starts a named service.</span></span><br/>                                                 |
| [<span data-ttu-id="1b94c-125">**ServiceStop**</span><span class="sxs-lookup"><span data-stu-id="1b94c-125">**ServiceStop**</span></span>](ishelldispatch2-servicestop.md)                   | <span data-ttu-id="1b94c-126">Arrête un service nommé.</span><span class="sxs-lookup"><span data-stu-id="1b94c-126">Stops a named service.</span></span><br/>                                                  |
| [<span data-ttu-id="1b94c-127">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="1b94c-127">**ShellExecute**</span></span>](ishelldispatch2-shellexecute.md)                 | <span data-ttu-id="1b94c-128">Exécute une opération spécifiée sur un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1b94c-128">Performs a specified operation on a specified file.</span></span><br/>                     |
| [<span data-ttu-id="1b94c-129">**ShowBrowserBar**</span><span class="sxs-lookup"><span data-stu-id="1b94c-129">**ShowBrowserBar**</span></span>](ishelldispatch2-showbrowserbar.md)             | <span data-ttu-id="1b94c-130">Affiche une barre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="1b94c-130">Displays a browser bar.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="1b94c-131">Notes</span><span class="sxs-lookup"><span data-stu-id="1b94c-131">Remarks</span></span>

<span data-ttu-id="1b94c-132">Pour plus d’informations sur les services Windows, consultez la documentation relative aux [services](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="1b94c-132">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b94c-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1b94c-133">Requirements</span></span>



| <span data-ttu-id="1b94c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b94c-134">Requirement</span></span> | <span data-ttu-id="1b94c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b94c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b94c-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b94c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1b94c-137">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b94c-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b94c-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b94c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1b94c-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b94c-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1b94c-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b94c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b94c-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b94c-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1b94c-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="1b94c-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b94c-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b94c-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1b94c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1b94c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b94c-145"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1b94c-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b94c-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b94c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b94c-147">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1b94c-147">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="1b94c-148">**Objet Shell**</span><span class="sxs-lookup"><span data-stu-id="1b94c-148">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="1b94c-149">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="1b94c-149">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> </dl>

 

 
