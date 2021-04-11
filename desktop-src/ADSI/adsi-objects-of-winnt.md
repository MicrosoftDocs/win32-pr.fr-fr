---
title: Objets ADSI de Winnt
description: Le fournisseur Winnt ADSI implémente les objets COM suivants pour prendre en charge les fonctionnalités et les services de différentes interfaces ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- ADSI, fournisseur de service WinNT, objets ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d0c9e5c486d07e1e392a9f307ecd9af4509ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100581"
---
# <a name="adsi-objects-of-winnt"></a><span data-ttu-id="9c0ed-104">Objets ADSI de Winnt</span><span class="sxs-lookup"><span data-stu-id="9c0ed-104">ADSI Objects of WinNT</span></span>

<span data-ttu-id="9c0ed-105">Le fournisseur Winnt ADSI implémente les objets COM suivants pour prendre en charge les fonctionnalités et les services de différentes interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-105">The ADSI WinNT provider implement the following COM objects to support features and services of various ADSI interfaces.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c0ed-106">Objet ADSI</span><span class="sxs-lookup"><span data-stu-id="9c0ed-106">ADSI Object</span></span></th>
<th><span data-ttu-id="9c0ed-107">Description</span><span class="sxs-lookup"><span data-stu-id="9c0ed-107">Description</span></span></th>
<th><span data-ttu-id="9c0ed-108">Interfaces prises en charge</span><span class="sxs-lookup"><span data-stu-id="9c0ed-108">Supported Interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c0ed-109"><strong>Classe</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-109"><strong>Class</strong></span></span></td>
<td><span data-ttu-id="9c0ed-110">Objet ADSI qui représente une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-110">An ADSI object that represents a class definition.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>IADsClass</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-112"><strong>Ordinateur</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-112"><strong>Computer</strong></span></span></td>
<td><span data-ttu-id="9c0ed-113">Objet ADSI qui représente un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-113">An ADSI object that represents a computer.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-115"><strong>Domaine</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-115"><strong>Domain</strong></span></span></td>
<td><span data-ttu-id="9c0ed-116">Objet ADSI qui représente un domaine sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-116">An ADSI object that represents a domain over the network.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-118"><strong>FileService</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-118"><strong>FileService</strong></span></span></td>
<td><span data-ttu-id="9c0ed-119">Objet ADSI qui représente un service de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-119">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-121"><strong>FileShare</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-121"><strong>FileShare</strong></span></span></td>
<td><span data-ttu-id="9c0ed-122">Objet ADSI qui représente un partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-122">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-124"><strong>FPNWFileService</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-124"><strong>FPNWFileService</strong></span></span></td>
<td><span data-ttu-id="9c0ed-125">Objet ADSI qui représente un service de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-125">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-127"><strong>FPNWFileShare</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-127"><strong>FPNWFileShare</strong></span></span></td>
<td><span data-ttu-id="9c0ed-128">Objet ADSI qui représente un partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-128">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-130"><strong>FPNWResource</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-130"><strong>FPNWResource</strong></span></span></td>
<td><span data-ttu-id="9c0ed-131">Objet ADSI qui représente une ressource.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-131">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-133"><strong>FPNWResourcesCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-133"><strong>FPNWResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="9c0ed-134">Objet ADSI qui représente une collection de ressources.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-134">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="9c0ed-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9c0ed-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-136"><strong>FPNWSession</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-136"><strong>FPNWSession</strong></span></span></td>
<td><span data-ttu-id="9c0ed-137">Objet ADSI qui représente une session.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-137">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-139"><strong>FPNWSessionsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-139"><strong>FPNWSessionsCollection</strong></span></span></td>
<td><span data-ttu-id="9c0ed-140">Objet ADSI qui représente une collection de sessions.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-140">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="9c0ed-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9c0ed-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-142"><strong>Groupe</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-142"><strong>Group</strong></span></span></td>
<td><span data-ttu-id="9c0ed-143">Objet ADSI qui représente un groupe.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-143">An ADSI object that represents a group.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c0ed-145">GetInfo ne peut pas être utilisé pour les groupes qui contiennent des membres qui sont des principaux de sécurité wellKnown dans l’étendue Winnt.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-145">GetInfo cannot be used for groups that contain members that are wellKnown security principals in the WinNT scope.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-146"><strong>GroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-146"><strong>GroupCollection</strong></span></span></td>
<td><span data-ttu-id="9c0ed-147">Objet ADSI qui représente une collection de groupes.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-147">An ADSI object that represents a collection of groups.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-149"><strong>LocalGroup</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-149"><strong>LocalGroup</strong></span></span></td>
<td><span data-ttu-id="9c0ed-150">Objet ADSI qui représente un groupe local.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-150">An ADSI object that represents a local group.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-152"><strong>LocalgroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-152"><strong>LocalgroupCollection</strong></span></span></td>
<td><span data-ttu-id="9c0ed-153">Objet ADSI qui représente une collection de groupes locaux.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-153">An ADSI object that represents a collection of local groups.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-155"><strong>Espace de noms</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-155"><strong>Namespace</strong></span></span></td>
<td><span data-ttu-id="9c0ed-156">Objet ADSI qui représente l’espace de noms Winnt.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-156">An ADSI object that represents the WinNT namespace.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-158"><strong>PrintJob</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-158"><strong>PrintJob</strong></span></span></td>
<td><span data-ttu-id="9c0ed-159">Objet ADSI qui représente un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-159">An ADSI object that represents a print job.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-161"><strong>PrintJobsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-161"><strong>PrintJobsCollection</strong></span></span></td>
<td><span data-ttu-id="9c0ed-162">Objet ADSI qui représente une collection de travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-162">An ADSI object that represents a collection of print jobs.</span></span></td>
<td><span data-ttu-id="9c0ed-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9c0ed-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-164"><strong>PrintQueue</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-164"><strong>PrintQueue</strong></span></span></td>
<td><span data-ttu-id="9c0ed-165">Objet ADSI qui représente une file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-165">An ADSI object that represents a print queue.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-167"><strong>Propriété</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-167"><strong>Property</strong></span></span></td>
<td><span data-ttu-id="9c0ed-168">Objet ADSI qui représente une définition d’attribut.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-168">An ADSI object that represents an attribute definition.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>IADsProperty</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-170"><strong>Ressource</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-170"><strong>Resource</strong></span></span></td>
<td><span data-ttu-id="9c0ed-171">Objet ADSI qui représente une ressource.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-171">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-173"><strong>ResourcesCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-173"><strong>ResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="9c0ed-174">Objet ADSI qui représente une collection de ressources.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-174">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="9c0ed-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9c0ed-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-176"><strong>Schéma</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-176"><strong>Schema</strong></span></span></td>
<td><span data-ttu-id="9c0ed-177">Objet ADSI qui représente le conteneur de schéma.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-177">An ADSI object that represents the schema container.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-179"><strong>Service</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-179"><strong>Service</strong></span></span></td>
<td><span data-ttu-id="9c0ed-180">Objet ADSI qui représente un service.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-180">An ADSI object that represents a service.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-182"><strong>Session</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-182"><strong>Session</strong></span></span></td>
<td><span data-ttu-id="9c0ed-183">Objet ADSI qui représente une session.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-183">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-185"><strong>SessionsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-185"><strong>SessionsCollection</strong></span></span></td>
<td><span data-ttu-id="9c0ed-186">Objet ADSI qui représente une collection de sessions.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-186">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="9c0ed-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9c0ed-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-188"><strong>Syntaxe</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-188"><strong>Syntax</strong></span></span></td>
<td><span data-ttu-id="9c0ed-189">Objet ADSI qui représente la syntaxe d’un attribut.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-189">An ADSI object that represents the syntax of an attribute.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>IADsSyntax</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-191"><strong>Utilisateur</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-191"><strong>User</strong></span></span></td>
<td><span data-ttu-id="9c0ed-192">Objet ADSI qui représente un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-192">An ADSI object that represents a user account.</span></span></td>
<td><dl> <span data-ttu-id="9c0ed-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9c0ed-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-194"><strong>UserGroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9c0ed-194"><strong>UserGroupCollection</strong></span></span></td>
<td><span data-ttu-id="9c0ed-195">Objet ADSI qui représente une collection de groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-195">An ADSI object that represents a collection of user groups.</span></span></td>
<td><span data-ttu-id="9c0ed-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span><span class="sxs-lookup"><span data-stu-id="9c0ed-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





