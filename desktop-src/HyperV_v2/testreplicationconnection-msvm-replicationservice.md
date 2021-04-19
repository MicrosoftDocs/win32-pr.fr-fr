---
description: Vérifie si la réplication peut être activée à partir du système hôte actuel vers le système de récupération spécifié.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Méthode TestReplicationConnection de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544618"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="c1857-103">Méthode TestReplicationConnection de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="c1857-103">TestReplicationConnection method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="c1857-104">Vérifie si la réplication peut être activée à partir du système hôte actuel vers le système de récupération spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1857-104">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1857-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1857-105">Syntax</span></span>


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c1857-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1857-107">*RecoveryConnectionPoint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1857-107">*RecoveryConnectionPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1857-108">Nom du point de connexion.</span><span class="sxs-lookup"><span data-stu-id="c1857-108">The name of the connection point.</span></span> <span data-ttu-id="c1857-109">Pour un cluster de récupération, il s’agit du nom de l’extrémité de service Broker.</span><span class="sxs-lookup"><span data-stu-id="c1857-109">For a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="c1857-110">Pour un serveur de récupération autonome, il s’agit du nom du système hôte.</span><span class="sxs-lookup"><span data-stu-id="c1857-110">For a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="c1857-111">*RecoveryServerPortNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1857-111">*RecoveryServerPortNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1857-112">Numéro de port du point de connexion de récupération.</span><span class="sxs-lookup"><span data-stu-id="c1857-112">The recovery connection point port number.</span></span>

</dd> <dt>

<span data-ttu-id="c1857-113">*AuthenticationType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1857-113">*AuthenticationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1857-114">Schéma d’authentification de récupération.</span><span class="sxs-lookup"><span data-stu-id="c1857-114">The recovery authentication scheme.</span></span> <span data-ttu-id="c1857-115">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c1857-115">This must be one of the following values.</span></span>

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span data-ttu-id="c1857-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Authentification intégrée** (1)</span><span class="sxs-lookup"><span data-stu-id="c1857-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrated authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c1857-117">Authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c1857-117">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="c1857-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Authentification basée sur les certificats** (2)</span><span class="sxs-lookup"><span data-stu-id="c1857-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c1857-119">Authentification basée sur les certificats.</span><span class="sxs-lookup"><span data-stu-id="c1857-119">Certificate based authentication.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c1857-120">*CertificateThumbPrint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1857-120">*CertificateThumbPrint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1857-121">Empreinte numérique du certificat à utiliser lorsque le paramètre *AuthenticationType* est l’authentification basée sur les certificats.</span><span class="sxs-lookup"><span data-stu-id="c1857-121">Certificate thumbprint to use when the *AuthenticationType* parameter is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="c1857-122">*BypassProxyServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1857-122">*BypassProxyServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1857-123">Contournez le serveur proxy lors de la connexion au serveur de réplication.</span><span class="sxs-lookup"><span data-stu-id="c1857-123">Bypass the proxy server when connecting to the replica server.</span></span>

</dd> <dt>

<span data-ttu-id="c1857-124">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c1857-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1857-125">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c1857-125">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1857-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1857-126">Return value</span></span>

<span data-ttu-id="c1857-127">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c1857-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c1857-128">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c1857-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-129">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c1857-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-130">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="c1857-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-131">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="c1857-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-132">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="c1857-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-133">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="c1857-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-134">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="c1857-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-135">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="c1857-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-136">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="c1857-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-137">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="c1857-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-138">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="c1857-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-139">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c1857-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-140">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="c1857-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c1857-141">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="c1857-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c1857-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1857-142">Requirements</span></span>



| <span data-ttu-id="c1857-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1857-143">Requirement</span></span> | <span data-ttu-id="c1857-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1857-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1857-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1857-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c1857-146">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1857-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c1857-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1857-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c1857-148">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1857-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1857-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c1857-149">Namespace</span></span><br/>                | <span data-ttu-id="c1857-150">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c1857-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c1857-151">MOF</span><span class="sxs-lookup"><span data-stu-id="c1857-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1857-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1857-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1857-153">DLL</span><span class="sxs-lookup"><span data-stu-id="c1857-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1857-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1857-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1857-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1857-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1857-156">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="c1857-156">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

