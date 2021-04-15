---
description: Récupère les certificats système sur un système hôte.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Méthode GetSystemCertificates de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5464d420b7fc019a0829d7255dafb1716e5e9f5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525240"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="288e3-103">Méthode GetSystemCertificates de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="288e3-103">GetSystemCertificates method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="288e3-104">Récupère les certificats système sur un système hôte.</span><span class="sxs-lookup"><span data-stu-id="288e3-104">Retrieves the system certificates on a host system.</span></span>

## <a name="syntax"></a><span data-ttu-id="288e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="288e3-105">Syntax</span></span>


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a><span data-ttu-id="288e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="288e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="288e3-107">*EncodedCertificates* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="288e3-107">*EncodedCertificates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="288e3-108">En cas de réussite, reçoit les certificats disponibles dans le magasin personnel de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="288e3-108">If successful, receives the certificates available from the Personal store for the local machine.</span></span> <span data-ttu-id="288e3-109">Chaque entrée est une chaîne de certificat encodée 64 de base.</span><span class="sxs-lookup"><span data-stu-id="288e3-109">Each entry is a base 64 encoded certificate string.</span></span> <span data-ttu-id="288e3-110">Cette chaîne peut être convertie en un tableau d’octets en construisant un objet X509Certificate2.</span><span class="sxs-lookup"><span data-stu-id="288e3-110">This string can be converted to a byte array by constructing an X509Certificate2 object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="288e3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="288e3-111">Return value</span></span>

<span data-ttu-id="288e3-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="288e3-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="288e3-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="288e3-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="288e3-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="288e3-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="288e3-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="288e3-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="288e3-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="288e3-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="288e3-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="288e3-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="288e3-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="288e3-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="288e3-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="288e3-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="288e3-126">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="288e3-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="288e3-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="288e3-127">Requirements</span></span>



| <span data-ttu-id="288e3-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="288e3-128">Requirement</span></span> | <span data-ttu-id="288e3-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="288e3-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="288e3-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="288e3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="288e3-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="288e3-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="288e3-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="288e3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="288e3-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="288e3-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="288e3-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="288e3-134">Namespace</span></span><br/>                | <span data-ttu-id="288e3-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="288e3-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="288e3-136">MOF</span><span class="sxs-lookup"><span data-stu-id="288e3-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="288e3-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="288e3-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="288e3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="288e3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="288e3-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="288e3-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="288e3-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="288e3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="288e3-141">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="288e3-141">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

 




