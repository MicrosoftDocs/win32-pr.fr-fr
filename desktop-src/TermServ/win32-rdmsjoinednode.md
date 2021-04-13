---
title: Classe Win32_RDMSJoinedNode
description: Représente un nœud de serveur géré par Bureau à distance Management Services (RDMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Win32_RDMSJoinedNode de la classe Services Bureau à distance
- Win32_RDMSJoinedNode de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383963"
---
# <a name="win32_rdmsjoinednode-class"></a><span data-ttu-id="e0247-105">\_Classe RDMSJoinedNode Win32</span><span class="sxs-lookup"><span data-stu-id="e0247-105">Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="e0247-106">Représente un nœud de serveur géré par Bureau à distance Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="e0247-106">Represents a server node that is managed by Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="e0247-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e0247-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0247-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0247-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a><span data-ttu-id="e0247-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e0247-109">Members</span></span>

<span data-ttu-id="e0247-110">La classe **Win32 \_ RDMSJoinedNode** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e0247-110">The **Win32\_RDMSJoinedNode** class has these types of members:</span></span>

-   [<span data-ttu-id="e0247-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e0247-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e0247-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0247-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e0247-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e0247-113">Methods</span></span>

<span data-ttu-id="e0247-114">La classe **Win32 \_ RDMSJoinedNode** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e0247-114">The **Win32\_RDMSJoinedNode** class has these methods.</span></span>



| <span data-ttu-id="e0247-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="e0247-115">Method</span></span>                                                                | <span data-ttu-id="e0247-116">Description</span><span class="sxs-lookup"><span data-stu-id="e0247-116">Description</span></span>                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0247-117">**GetJoinedNodeCount**</span><span class="sxs-lookup"><span data-stu-id="e0247-117">**GetJoinedNodeCount**</span></span>](win32-rdmsjoinednode-getjoinednodecount.md) | <span data-ttu-id="e0247-118">**Windows server 2012 R2 et Windows server 2012 :** Cette méthode n’est pas disponible avant Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e0247-118">**Windows Server 2012 R2 and Windows Server 2012:** This method is unavailable prior to Windows Server 2016.</span></span><br/> <span data-ttu-id="e0247-119">Obtient le nombre de serveurs sur lesquels le rôle spécifié est installé.</span><span class="sxs-lookup"><span data-stu-id="e0247-119">Gets the number of servers that have the specified role installed.</span></span><br/> |
| [<span data-ttu-id="e0247-120">**Joindre**</span><span class="sxs-lookup"><span data-stu-id="e0247-120">**Join**</span></span>](join-win32-rdmsjoinednode.md)                             | <span data-ttu-id="e0247-121">Ajoute un nœud à RDMS.</span><span class="sxs-lookup"><span data-stu-id="e0247-121">Adds a node to RDMS.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="e0247-122">**Disjoindre**</span><span class="sxs-lookup"><span data-stu-id="e0247-122">**Unjoin**</span></span>](unjoin-win32-rdmsjoinednode.md)                         | <span data-ttu-id="e0247-123">Supprime un nœud de RDMS.</span><span class="sxs-lookup"><span data-stu-id="e0247-123">Removes a node from RDMS.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="e0247-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0247-124">Properties</span></span>

<span data-ttu-id="e0247-125">La classe **Win32 \_ RDMSJoinedNode** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e0247-125">The **Win32\_RDMSJoinedNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0247-126">**FQDN**</span><span class="sxs-lookup"><span data-stu-id="e0247-126">**FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0247-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0247-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0247-129">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e0247-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e0247-130">Obtient le nom de domaine complet du nœud.</span><span class="sxs-lookup"><span data-stu-id="e0247-130">Gets the fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-131">**IsGatewayCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="e0247-131">**IsGatewayCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-132">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-134">Obtient et définit une valeur qui indique si le serveur a un certificat pour effectuer l’authentification pour les connexions Bureau à distance passerelle.</span><span class="sxs-lookup"><span data-stu-id="e0247-134">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop gateway connections.</span></span> <span data-ttu-id="e0247-135">**True** si le certificat est installé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-135">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-136">**IsPublishingCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="e0247-136">**IsPublishingCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-137">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-139">Obtient et définit une valeur qui indique si le serveur dispose d’un certificat pour signer protocole RDP (Remote Desktop Protocol) fichiers de publication.</span><span class="sxs-lookup"><span data-stu-id="e0247-139">Gets and sets a value that indicates whether the server has a certificate to sign Remote Desktop Protocol publishing files.</span></span> <span data-ttu-id="e0247-140">**True** si le certificat est installé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-140">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-141">**IsRdcb**</span><span class="sxs-lookup"><span data-stu-id="e0247-141">**IsRdcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-144">Obtient et définit une valeur qui indique si le serveur est Connexion Bureau à distance Broker.</span><span class="sxs-lookup"><span data-stu-id="e0247-144">Gets and sets a value that indicates whether the server is Remote Desktop Connection Broker.</span></span> <span data-ttu-id="e0247-145">**True** si le serveur est un connexion Bureau à distance Broker ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-145">**TRUE** if the server is a Remote Desktop Connection Broker; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-146">**IsRdg**</span><span class="sxs-lookup"><span data-stu-id="e0247-146">**IsRdg**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-147">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-149">Obtient et définit une valeur qui indique si le serveur est Bureau à distance serveur de passerelle.</span><span class="sxs-lookup"><span data-stu-id="e0247-149">Gets and sets a value that indicates whether the server is Remote Desktop gateway server.</span></span> <span data-ttu-id="e0247-150">**True** si le serveur est un serveur de passerelle Bureau à distance ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-150">**TRUE** if the server is a Remote Desktop gateway server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-151">**IsRdls**</span><span class="sxs-lookup"><span data-stu-id="e0247-151">**IsRdls**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-152">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-154">Obtient et définit une valeur qui indique si le serveur est Bureau à distance serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="e0247-154">Gets and sets a value that indicates whether the server is Remote Desktop license server.</span></span> <span data-ttu-id="e0247-155">**True** si le serveur est un serveur de licences bureau à distance ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-155">**TRUE** if the server is a Remote Desktop license server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-156">**IsRdsh**</span><span class="sxs-lookup"><span data-stu-id="e0247-156">**IsRdsh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-157">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-159">Obtient et définit une valeur qui indique si le serveur est Bureau à distance serveur hôte de session.</span><span class="sxs-lookup"><span data-stu-id="e0247-159">Gets and sets a value that indicates whether the server is Remote Desktop session host server.</span></span> <span data-ttu-id="e0247-160">**True** si le serveur est un serveur hôte de session Bureau à distance ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-160">**TRUE** if the server is a Remote Desktop session host server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-161">**IsRdvh**</span><span class="sxs-lookup"><span data-stu-id="e0247-161">**IsRdvh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-162">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-164">Obtient et définit une valeur qui indique si le serveur est Bureau à distance ordinateur hôte de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="e0247-164">Gets and sets a value that indicates whether the server is Remote Desktop virtualization host.</span></span> <span data-ttu-id="e0247-165">**True** si le serveur est un hôte de virtualisation Bureau à distance ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-165">**TRUE** if the server is a Remote Desktop virtualization host; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-166">**IsRdwa**</span><span class="sxs-lookup"><span data-stu-id="e0247-166">**IsRdwa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-167">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-167">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-168">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-168">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-169">Obtient et définit une valeur qui indique si le serveur est Bureau à distance serveur d’accès Web.</span><span class="sxs-lookup"><span data-stu-id="e0247-169">Gets and sets a value that indicates whether the server is Remote Desktop web access server.</span></span> <span data-ttu-id="e0247-170">**True** si le serveur est un serveur Bureau à distance accès Web ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-170">**TRUE** if the server is a Remote Desktop Web Access server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-171">**IsRedirectorCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="e0247-171">**IsRedirectorCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-172">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-174">Obtient et définit une valeur qui indique si le serveur a un certificat pour effectuer l’authentification pour le déploiement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e0247-174">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Services deployment.</span></span> <span data-ttu-id="e0247-175">**True** si le certificat est installé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-175">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-176">**IsWebAccessCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="e0247-176">**IsWebAccessCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-177">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0247-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0247-179">Obtient et définit une valeur qui indique si le serveur a un certificat pour effectuer l’authentification pour Bureau à distance Accès web.</span><span class="sxs-lookup"><span data-stu-id="e0247-179">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Web Access.</span></span> <span data-ttu-id="e0247-180">**True** si le certificat est installé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e0247-180">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-181">**OSVersion**</span><span class="sxs-lookup"><span data-stu-id="e0247-181">**OSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0247-182">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-183">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0247-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e0247-184">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e0247-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e0247-185">Obtient et définit la version des systèmes d’exploitation sur le nœud.</span><span class="sxs-lookup"><span data-stu-id="e0247-185">Gets and sets the version of the operating systems on the node.</span></span>

</dd> <dt>

<span data-ttu-id="e0247-186">**SID**</span><span class="sxs-lookup"><span data-stu-id="e0247-186">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0247-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0247-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0247-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0247-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0247-189">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e0247-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e0247-190">Obtient l’identificateur de sécurité (SID) du nœud.</span><span class="sxs-lookup"><span data-stu-id="e0247-190">Gets the security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0247-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0247-191">Requirements</span></span>



| <span data-ttu-id="e0247-192">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0247-192">Requirement</span></span> | <span data-ttu-id="e0247-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0247-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0247-194">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0247-194">Minimum supported client</span></span><br/> | <span data-ttu-id="e0247-195">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0247-195">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e0247-196">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0247-196">Minimum supported server</span></span><br/> | <span data-ttu-id="e0247-197">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0247-197">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e0247-198">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e0247-198">Namespace</span></span><br/>                | <span data-ttu-id="e0247-199">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="e0247-199">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e0247-200">MOF</span><span class="sxs-lookup"><span data-stu-id="e0247-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0247-201"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0247-201"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0247-202">DLL</span><span class="sxs-lookup"><span data-stu-id="e0247-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0247-203"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0247-203"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e0247-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0247-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0247-205">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e0247-205">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

