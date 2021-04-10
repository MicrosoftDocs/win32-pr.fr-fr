---
description: Une infrastructure de clé publique (PKI) Windows enregistre des certificats sur le serveur qui héberge l’autorité de certification (CA) et sur l’ordinateur ou l’appareil local.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Répertoire de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210914"
---
# <a name="certificate-directory"></a><span data-ttu-id="4c59e-103">Répertoire de certificat</span><span class="sxs-lookup"><span data-stu-id="4c59e-103">Certificate Directory</span></span>

<span data-ttu-id="4c59e-104">Une infrastructure de clé publique (PKI) Windows enregistre des certificats sur le serveur qui héberge l’autorité de certification (CA) et sur l’ordinateur ou l’appareil local.</span><span class="sxs-lookup"><span data-stu-id="4c59e-104">A Windows public key infrastructure (PKI) saves certificates on the server that hosts the certification authority (CA) and on the local computer or device.</span></span> <span data-ttu-id="4c59e-105">Le stockage de l’autorité de certification est généralement désigné sous le nom de base de données de certificats, et le stockage local est appelé magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="4c59e-105">CA storage is typically referred to as the certificate database, and local storage is known as the certificate store.</span></span>

## <a name="certificate-database"></a><span data-ttu-id="4c59e-106">Base de données de certificats</span><span class="sxs-lookup"><span data-stu-id="4c59e-106">Certificate Database</span></span>

<span data-ttu-id="4c59e-107">Lorsque vous ajoutez des services de certificats sur un serveur Windows et configurez une autorité de certification, une base de données de certificats est créée.</span><span class="sxs-lookup"><span data-stu-id="4c59e-107">When you add Certificate Services on a Windows server and configure a CA, a certificate database is created.</span></span> <span data-ttu-id="4c59e-108">Par défaut, la base de données est contenue dans le dossier *% systemroot%* \\ system32 \\ Certlog, et le nom est basé sur le nom de l’autorité de certification avec une extension. edb.</span><span class="sxs-lookup"><span data-stu-id="4c59e-108">By default, the database is contained in the *%SystemRoot%*\\System32\\Certlog folder, and the name is based on the CA name with an .edb extension.</span></span> <span data-ttu-id="4c59e-109">La base de données peut contenir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4c59e-109">The database can contain:</span></span>

-   <span data-ttu-id="4c59e-110">Certificats émis</span><span class="sxs-lookup"><span data-stu-id="4c59e-110">Issued certificates</span></span>
-   <span data-ttu-id="4c59e-111">Certificats révoqués</span><span class="sxs-lookup"><span data-stu-id="4c59e-111">Revoked certificates</span></span>
-   <span data-ttu-id="4c59e-112">Clés privées archivées</span><span class="sxs-lookup"><span data-stu-id="4c59e-112">Archived private keys</span></span>
-   <span data-ttu-id="4c59e-113">Demandes de certificat</span><span class="sxs-lookup"><span data-stu-id="4c59e-113">Certificate requests</span></span>

<span data-ttu-id="4c59e-114">Vous ne pouvez pas utiliser l’API d’inscription de certificats pour manipuler la base de données.</span><span class="sxs-lookup"><span data-stu-id="4c59e-114">You cannot use the Certificate Enrollment API to manipulate the database.</span></span> <span data-ttu-id="4c59e-115">Le processus d’inscription crée automatiquement les entrées nécessaires.</span><span class="sxs-lookup"><span data-stu-id="4c59e-115">The enrollment process automatically creates the necessary entries.</span></span>

## <a name="certificate-stores"></a><span data-ttu-id="4c59e-116">Magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="4c59e-116">Certificate Stores</span></span>

<span data-ttu-id="4c59e-117">Les services de certificats Microsoft copient les certificats émis et les demandes en attente ou rejetées pour les ordinateurs et les appareils locaux.</span><span class="sxs-lookup"><span data-stu-id="4c59e-117">Microsoft Certificate Services copies issued certificates and pending or rejected requests to local computers and devices.</span></span> <span data-ttu-id="4c59e-118">L’emplacement de stockage est appelé magasin de certificats et se compose des magasins logiques suivants.</span><span class="sxs-lookup"><span data-stu-id="4c59e-118">The storage location is called the certificate store and consists of the following logical stores.</span></span>

| <span data-ttu-id="4c59e-119">Magasin logique</span><span class="sxs-lookup"><span data-stu-id="4c59e-119">Logical store</span></span>                                         | <span data-ttu-id="4c59e-120">Description</span><span class="sxs-lookup"><span data-stu-id="4c59e-120">Description</span></span>                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c59e-121">Personnel</span><span class="sxs-lookup"><span data-stu-id="4c59e-121">Personal</span></span><br/>                                   | <span data-ttu-id="4c59e-122">Contient des certificats associés à une clé privée contrôlée par l’utilisateur ou l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4c59e-122">Contains certificates associated with a private key controlled by the user or computer.</span></span><br/>                     |
| <span data-ttu-id="4c59e-123">Autorités de certification racine de confiance</span><span class="sxs-lookup"><span data-stu-id="4c59e-123">Trusted Root Certification Authorities</span></span><br/>     | <span data-ttu-id="4c59e-124">Contient des certificats provenant d’autorités de certification (ca) approuvées de manière implicite.</span><span class="sxs-lookup"><span data-stu-id="4c59e-124">Contains certificates from implicitly trusted certification authorities (CAs).</span></span><br/>                              |
| <span data-ttu-id="4c59e-125">Enterprise Trust</span><span class="sxs-lookup"><span data-stu-id="4c59e-125">Enterprise Trust</span></span><br/>                           | <span data-ttu-id="4c59e-126">Contient les listes de certificats de confiance généralement utilisées pour approuver des certificats auto-signés d’autres organisations.</span><span class="sxs-lookup"><span data-stu-id="4c59e-126">Contains certificate trust lists typically used to trust self-signed certificates from other organizations.</span></span><br/> |
| <span data-ttu-id="4c59e-127">Autorités de certification intermédiaires</span><span class="sxs-lookup"><span data-stu-id="4c59e-127">Intermediate Certification Authorities</span></span><br/>     | <span data-ttu-id="4c59e-128">Contient les certificats émis pour des AC secondaires dans la hiérarchie de certification.</span><span class="sxs-lookup"><span data-stu-id="4c59e-128">Contains certificates issued to subordinate CAs in the certification hierarchy.</span></span><br/>                             |
| <span data-ttu-id="4c59e-129">Objet utilisateur Active Directory</span><span class="sxs-lookup"><span data-stu-id="4c59e-129">Active Directory User Object</span></span><br/>               | <span data-ttu-id="4c59e-130">Contient le ou les certificats de l’objet utilisateur publiés dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4c59e-130">Contains the user object certificate or certificates published in Active Directory.</span></span><br/>                         |
| <span data-ttu-id="4c59e-131">Éditeurs approuvés</span><span class="sxs-lookup"><span data-stu-id="4c59e-131">Trusted Publishers</span></span><br/>                         | <span data-ttu-id="4c59e-132">Contient des certificats provenant d’autorités de certification approuvées.</span><span class="sxs-lookup"><span data-stu-id="4c59e-132">Contains certificates from trusted CAs.</span></span><br/>                                                                     |
| <span data-ttu-id="4c59e-133">Certificats non autorisés</span><span class="sxs-lookup"><span data-stu-id="4c59e-133">Untrusted Certificates</span></span><br/>                     | <span data-ttu-id="4c59e-134">Contient des certificats qui ont été identifiés explicitement comme non approuvés.</span><span class="sxs-lookup"><span data-stu-id="4c59e-134">Contains certificates that have been explicitly identified as untrusted.</span></span><br/>                                    |
| <span data-ttu-id="4c59e-135">Autorités de certification racine tierce partie</span><span class="sxs-lookup"><span data-stu-id="4c59e-135">Third-Party Root Certification Authorities</span></span><br/> | <span data-ttu-id="4c59e-136">Contient des certificats racines approuvés provenant d’autorités de certification en dehors de la hiérarchie de certificats interne.</span><span class="sxs-lookup"><span data-stu-id="4c59e-136">Contains trusted root certificates from CAs outside the internal certificate hierarchy.</span></span><br/>                     |
| <span data-ttu-id="4c59e-137">Personnes autorisées</span><span class="sxs-lookup"><span data-stu-id="4c59e-137">Trusted People</span></span><br/>                             | <span data-ttu-id="4c59e-138">Contient des certificats délivrés aux utilisateurs ou entités qui ont été explicitement approuvés.</span><span class="sxs-lookup"><span data-stu-id="4c59e-138">Contains certificates issued to users or entities that have been explicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="4c59e-139">Autres personnes</span><span class="sxs-lookup"><span data-stu-id="4c59e-139">Other People</span></span><br/>                               | <span data-ttu-id="4c59e-140">Contient des certificats délivrés aux utilisateurs ou entités qui ont été approuvés implicitement.</span><span class="sxs-lookup"><span data-stu-id="4c59e-140">Contains certificates issued to users or entities that have been implicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="4c59e-141">Demandes d'inscription de certificat</span><span class="sxs-lookup"><span data-stu-id="4c59e-141">Certificate Enrollment Requests</span></span><br/>            | <span data-ttu-id="4c59e-142">Contient des demandes de certificat en attente ou rejetées.</span><span class="sxs-lookup"><span data-stu-id="4c59e-142">Contains pending or rejected certificate requests.</span></span><br/>                                                          |



 

<span data-ttu-id="4c59e-143">Vous ne pouvez pas utiliser l’API d’inscription de certificats pour spécifier ou récupérer des propriétés de stockage ou copier des certificats dans des magasins spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4c59e-143">You cannot use the Certificate Enrollment API to specify or retrieve store properties or copy certificates to specific stores.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c59e-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c59e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c59e-145">Éléments PKI</span><span class="sxs-lookup"><span data-stu-id="4c59e-145">PKI Elements</span></span>](about-pki-components.md)
</dt> </dl>

 

 




