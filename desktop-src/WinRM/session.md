---
title: Objet session (WSManDisp. h)
description: Définit des opérations et des paramètres de session.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Windows Remote Management d’objet de session
- Windows Remote Management d’objet de session, Description
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942880"
---
# <a name="session-object-wsmandisph"></a><span data-ttu-id="b5376-105">Objet session (WSManDisp. h)</span><span class="sxs-lookup"><span data-stu-id="b5376-105">Session object (WSManDisp.h)</span></span>

<span data-ttu-id="b5376-106">Définit des opérations et des paramètres de session.</span><span class="sxs-lookup"><span data-stu-id="b5376-106">Defines operations and session settings.</span></span> <span data-ttu-id="b5376-107">Toute opération de Windows Remote Management nécessite la création d’une **session** qui se connecte à un ordinateur distant, à un [*contrôleur de gestion de base*](windows-remote-management-glossary.md) (BMC) ou à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b5376-107">Any Windows Remote Management operations require creation of a **Session** that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="b5376-108">Les opérations de réseau WinRM incluent l’obtention, l’écriture ou l’énumération de données, ou l’appel de méthodes.</span><span class="sxs-lookup"><span data-stu-id="b5376-108">WinRM network operations include getting, writing, or enumerating data, or invoking methods.</span></span> <span data-ttu-id="b5376-109">Les méthodes de l’objet de **session** reflètent les opérations de base définies dans le protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="b5376-109">The methods of the **Session** object mirror the basic operations defined in the WS-Management protocol.</span></span>

## <a name="members"></a><span data-ttu-id="b5376-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b5376-110">Members</span></span>

<span data-ttu-id="b5376-111">L’objet **session** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b5376-111">The **Session** object has these types of members:</span></span>

-   [<span data-ttu-id="b5376-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b5376-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b5376-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5376-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b5376-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b5376-114">Methods</span></span>

<span data-ttu-id="b5376-115">L’objet **session** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b5376-115">The **Session** object has these methods.</span></span>



| <span data-ttu-id="b5376-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="b5376-116">Method</span></span>                                 | <span data-ttu-id="b5376-117">Description</span><span class="sxs-lookup"><span data-stu-id="b5376-117">Description</span></span>                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5376-118">**Créés**</span><span class="sxs-lookup"><span data-stu-id="b5376-118">**Create**</span></span>](session-create.md)       | <span data-ttu-id="b5376-119">Crée une nouvelle instance d’une ressource et retourne l’URI du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="b5376-119">Creates a new instance of a resource and returns the URI of the new object.</span></span><br/>                                      |
| [<span data-ttu-id="b5376-120">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="b5376-120">**Delete**</span></span>](session-delete.md)       | <span data-ttu-id="b5376-121">Supprime la ressource spécifiée dans l’URI de ressource.</span><span class="sxs-lookup"><span data-stu-id="b5376-121">Deletes the resource specified in the resource URI.</span></span><br/>                                                              |
| [<span data-ttu-id="b5376-122">**Énumérer**</span><span class="sxs-lookup"><span data-stu-id="b5376-122">**Enumerate**</span></span>](session-enumerate.md) | <span data-ttu-id="b5376-123">Énumère les ressources d’une collection, d’une table ou d’un journal des messages.</span><span class="sxs-lookup"><span data-stu-id="b5376-123">Enumerates a collection, table, or message log resource.</span></span><br/>                                                         |
| [<span data-ttu-id="b5376-124">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="b5376-124">**Get**</span></span>](session-get.md)             | <span data-ttu-id="b5376-125">Récupère une ressource du service et retourne une représentation XML de l’instance actuelle de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b5376-125">Retrieves a resource from the service and returns an XML representation of the current instance of the resource.</span></span><br/> |
| [<span data-ttu-id="b5376-126">**Repérer**</span><span class="sxs-lookup"><span data-stu-id="b5376-126">**Identify**</span></span>](session-identify.md)   | <span data-ttu-id="b5376-127">Interroge un ordinateur distant pour déterminer s’il prend en charge le protocole WS-Management</span><span class="sxs-lookup"><span data-stu-id="b5376-127">Queries a remote computer to determine if it supports the WS-Management protocol</span></span><br/>                                 |
| [<span data-ttu-id="b5376-128">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="b5376-128">**Invoke**</span></span>](session-invoke.md)       | <span data-ttu-id="b5376-129">Appelle une méthode qui retourne les résultats de l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="b5376-129">Invokes a method that returns the results of the method call.</span></span><br/>                                                    |
| [<span data-ttu-id="b5376-130">**Posé**</span><span class="sxs-lookup"><span data-stu-id="b5376-130">**Put**</span></span>](session-put.md)             | <span data-ttu-id="b5376-131">Met à jour une ressource.</span><span class="sxs-lookup"><span data-stu-id="b5376-131">Updates a resource.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="b5376-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5376-132">Properties</span></span>

<span data-ttu-id="b5376-133">L’objet **session** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b5376-133">The **Session** object has these properties.</span></span>



| <span data-ttu-id="b5376-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="b5376-134">Property</span></span>                                            | <span data-ttu-id="b5376-135">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b5376-135">Access type</span></span>           | <span data-ttu-id="b5376-136">Description</span><span class="sxs-lookup"><span data-stu-id="b5376-136">Description</span></span>                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5376-137">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="b5376-137">**BatchItems**</span></span>](session-batchitems.md)<br/> | <span data-ttu-id="b5376-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5376-138">Read/write</span></span><br/> | <span data-ttu-id="b5376-139">Définit et obtient le nombre d’éléments dans chaque lot d’énumération.</span><span class="sxs-lookup"><span data-stu-id="b5376-139">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="b5376-140">Cette valeur ne peut pas être modifiée pendant une énumération.</span><span class="sxs-lookup"><span data-stu-id="b5376-140">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="b5376-141">Par défaut, la valeur par défaut est un nombre illimité d’éléments.</span><span class="sxs-lookup"><span data-stu-id="b5376-141">By default, the default is an unlimited number of items.</span></span> <span data-ttu-id="b5376-142">Le fournisseur de ressources peut définir une limite.</span><span class="sxs-lookup"><span data-stu-id="b5376-142">The resource provider may set a limit.</span></span><br/> |
| [<span data-ttu-id="b5376-143">**Error**</span><span class="sxs-lookup"><span data-stu-id="b5376-143">**Error**</span></span>](session-error.md)<br/>           | <span data-ttu-id="b5376-144">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5376-144">Read-only</span></span><br/>  | <span data-ttu-id="b5376-145">Obtient des informations supplémentaires sur l’erreur dans un flux XML.</span><span class="sxs-lookup"><span data-stu-id="b5376-145">Gets additional error information in an XML stream.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="b5376-146">**Délai d'expiration**</span><span class="sxs-lookup"><span data-stu-id="b5376-146">**Timeout**</span></span>](session-timeout.md)<br/>       | <span data-ttu-id="b5376-147">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5376-147">Read/write</span></span><br/> | <span data-ttu-id="b5376-148">Définit et obtient la durée maximale (en millisecondes) d’attente de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="b5376-148">Sets and gets the maximum amount of time (in milliseconds) for the client application to wait.</span></span><br/>                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="b5376-149">Notes</span><span class="sxs-lookup"><span data-stu-id="b5376-149">Remarks</span></span>

<span data-ttu-id="b5376-150">L’objet **session** correspond à l’interface [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) .</span><span class="sxs-lookup"><span data-stu-id="b5376-150">The **Session** object corresponds to the [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="b5376-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="b5376-151">Examples</span></span>

<span data-ttu-id="b5376-152">L’exemple de code VBScript suivant montre comment créer un objet de **session** .</span><span class="sxs-lookup"><span data-stu-id="b5376-152">The following VBScript code example shows how to create a **Session** object.</span></span>


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a><span data-ttu-id="b5376-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5376-153">Requirements</span></span>



| <span data-ttu-id="b5376-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5376-154">Requirement</span></span> | <span data-ttu-id="b5376-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5376-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5376-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5376-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b5376-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5376-157">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b5376-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5376-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b5376-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5376-159">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b5376-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5376-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5376-161"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5376-161"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5376-162">MIDL</span><span class="sxs-lookup"><span data-stu-id="b5376-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5376-163"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5376-163"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b5376-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5376-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5376-165"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5376-165"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5376-166">DLL</span><span class="sxs-lookup"><span data-stu-id="b5376-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5376-167"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5376-167"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5376-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5376-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5376-169">API de script WinRM</span><span class="sxs-lookup"><span data-stu-id="b5376-169">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="b5376-170">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="b5376-170">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b5376-171">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="b5376-171">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b5376-172">Scripts dans Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="b5376-172">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b5376-173">Obtention de données à partir de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="b5376-173">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="b5376-174">Obtention de données à partir d’un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="b5376-174">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





