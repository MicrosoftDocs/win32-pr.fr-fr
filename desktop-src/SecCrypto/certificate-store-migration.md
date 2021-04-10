---
description: Lors de la mise à niveau d’un ordinateur ou d’une migration d’ordinateur à ordinateur, les certificats de certains magasins de certificats seront migrés.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migration du magasin de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035005"
---
# <a name="certificate-store-migration"></a><span data-ttu-id="afd88-103">Migration du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="afd88-103">Certificate Store Migration</span></span>

<span data-ttu-id="afd88-104">Lors de la mise à niveau d’un ordinateur ou d’une migration d’ordinateur à ordinateur, les certificats de certains magasins de certificats seront migrés.</span><span class="sxs-lookup"><span data-stu-id="afd88-104">During a computer upgrade or a computer-to-computer migration, the certificates in certain certificate stores will be migrated.</span></span> <span data-ttu-id="afd88-105">Le tableau suivant répertorie les magasins de certificats qui sont migrés par défaut.</span><span class="sxs-lookup"><span data-stu-id="afd88-105">The following table lists the certificate stores that are migrated by default.</span></span> <span data-ttu-id="afd88-106">Pour le magasin de demandes de certificat automatique du système (ACRS), seules les [*listes de certificats de confiance*](../secgloss/c-gly.md) (CTL) sont migrées.</span><span class="sxs-lookup"><span data-stu-id="afd88-106">For the system Automatic Certificate Request Settings (ACRS) store, only the [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) are migrated.</span></span> <span data-ttu-id="afd88-107">Pour tous les autres magasins répertoriés ci-dessous, seuls les certificats sont migrés.</span><span class="sxs-lookup"><span data-stu-id="afd88-107">For all other stores listed below, only the certificates are migrated.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="afd88-108">Système/utilisateur</span><span class="sxs-lookup"><span data-stu-id="afd88-108">System/user</span></span></th>
<th><span data-ttu-id="afd88-109">Magasin</span><span class="sxs-lookup"><span data-stu-id="afd88-109">Store</span></span></th>
<th><span data-ttu-id="afd88-110">Emplacement de stockage</span><span class="sxs-lookup"><span data-stu-id="afd88-110">Storage location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="afd88-111">$ {ROWSPAN8} $System $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="afd88-111">${ROWSPAN8}$System${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="afd88-112">ROOT</span><span class="sxs-lookup"><span data-stu-id="afd88-112">ROOT</span></span></td>
<td><span data-ttu-id="afd88-113"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Racine</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-113"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afd88-114">MY</span><span class="sxs-lookup"><span data-stu-id="afd88-114">MY</span></span></td>
<td><span data-ttu-id="afd88-115"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Mes</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-115"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>My</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="afd88-116">DEMANDE</span><span class="sxs-lookup"><span data-stu-id="afd88-116">REQUEST</span></span></td>
<td><span data-ttu-id="afd88-117"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Demande</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-117"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Request</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="afd88-118">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="afd88-118">TrustedPublisher</span></span></td>
<td><span data-ttu-id="afd88-119"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-119"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="afd88-120">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="afd88-120">TrustedPeople</span></span></td>
<td><span data-ttu-id="afd88-121"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-121"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="afd88-122">Interdit</span><span class="sxs-lookup"><span data-stu-id="afd88-122">Disallowed</span></span></td>
<td><span data-ttu-id="afd88-123"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Non <strong>autorisé</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-123"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="afd88-124">CA</span><span class="sxs-lookup"><span data-stu-id="afd88-124">CA</span></span></td>
<td><span data-ttu-id="afd88-125"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Autorité de certification</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-125"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="afd88-126">ENREGISTREMENTS</span><span class="sxs-lookup"><span data-stu-id="afd88-126">ACRS</span></span></td>
<td><span data-ttu-id="afd88-127"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>Listes CTL</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-127"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>ACRS</strong>\<strong>CTLs</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td rowspan="7"><span data-ttu-id="afd88-128">Utilisateur $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="afd88-128">User${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="afd88-129">ROOT</span><span class="sxs-lookup"><span data-stu-id="afd88-129">ROOT</span></span></td>
<td><span data-ttu-id="afd88-130"><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Racine</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-130"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afd88-131">MY</span><span class="sxs-lookup"><span data-stu-id="afd88-131">MY</span></span></td>
<td><span data-ttu-id="afd88-132">fichier : \\ %AppData%\Microsoft\SystemCertificates\My\Certificates</span><span class="sxs-lookup"><span data-stu-id="afd88-132">file:\\%APPDATA%\Microsoft\SystemCertificates\My\Certificates</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="afd88-133">DEMANDE</span><span class="sxs-lookup"><span data-stu-id="afd88-133">REQUEST</span></span></td>
<td><span data-ttu-id="afd88-134">fichier : \\ %AppData%\Microsoft\SystemCertificates\Request\Certificates</span><span class="sxs-lookup"><span data-stu-id="afd88-134">file:\\%APPDATA%\Microsoft\SystemCertificates\Request\Certificates</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="afd88-135">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="afd88-135">TrustedPublisher</span></span></td>
<td><span data-ttu-id="afd88-136"><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-136"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="afd88-137">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="afd88-137">TrustedPeople</span></span></td>
<td><span data-ttu-id="afd88-138"><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-138"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="afd88-139">Interdit</span><span class="sxs-lookup"><span data-stu-id="afd88-139">Disallowed</span></span></td>
<td><span data-ttu-id="afd88-140"><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Non <strong>autorisé</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-140"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="afd88-141">CA</span><span class="sxs-lookup"><span data-stu-id="afd88-141">CA</span></span></td>
<td><span data-ttu-id="afd88-142"><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Autorité de certification</strong> \ <strong>Certificats</strong></span><span class="sxs-lookup"><span data-stu-id="afd88-142"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="afd88-143">Les autres magasins de certificats créés par les applications ne sont pas migrés par défaut.</span><span class="sxs-lookup"><span data-stu-id="afd88-143">Other certificate stores created by applications are not migrated by default.</span></span> <span data-ttu-id="afd88-144">Les applications qui créent leurs propres magasins sont responsables de la migration des magasins qu’ils créent.</span><span class="sxs-lookup"><span data-stu-id="afd88-144">Applications that create their own stores are responsible for migration of the stores that they create.</span></span> <span data-ttu-id="afd88-145">Pour créer des magasins, nous vous recommandons de définir une clé de Registre dans les paramètres de l’application et de créer un magasin dans les paramètres du Registre à l’aide du fournisseur de magasin **CERT \_ Store \_ Prov \_** .</span><span class="sxs-lookup"><span data-stu-id="afd88-145">To create stores, we recommend that you define a registry key in the application settings and create a store within the registry settings by using the **CERT\_STORE\_PROV\_REG** store provider.</span></span> <span data-ttu-id="afd88-146">Pour plus d’informations sur la migration des paramètres d’application, consultez la rubrique *How to Create a Custom. XML file* dans le guide *using USMT 3,0* à l’adresse [outil de migration utilisateur 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span><span class="sxs-lookup"><span data-stu-id="afd88-146">For more information about migrating application settings, see the *How To Create a Custom .xml File* topic in the *Using USMT 3.0* guide at [User State Migration Tool 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span></span> <span data-ttu-id="afd88-147">(Cette ressource n’est peut-être pas disponible dans certaines langues et pays ou régions.)</span><span class="sxs-lookup"><span data-stu-id="afd88-147">(This resource may not be available in some languages and countries or regions.)</span></span>

 

 
