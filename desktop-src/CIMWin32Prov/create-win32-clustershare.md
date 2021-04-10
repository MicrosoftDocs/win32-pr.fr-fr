---
description: Crée une instance de \_ ClusterShare Win32.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111534"
---
# <a name="create-method-of-the-win32_clustershare-class"></a><span data-ttu-id="a2725-103">Créer une méthode de la \_ classe ClusterShare Win32</span><span class="sxs-lookup"><span data-stu-id="a2725-103">Create method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="a2725-104">Crée une instance [**de \_ ClusterShare Win32**](win32-clustershare.md) .</span><span class="sxs-lookup"><span data-stu-id="a2725-104">Creates a new [**Win32\_ClusterShare**](win32-clustershare.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2725-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2725-105">Syntax</span></span>


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="a2725-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2725-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2725-107">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2725-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2725-108">Chemin d’accès local du partage Windows.</span><span class="sxs-lookup"><span data-stu-id="a2725-108">Local path of the Windows share.</span></span>

<span data-ttu-id="a2725-109">Par exemple, « C : \\ Program Files ».</span><span class="sxs-lookup"><span data-stu-id="a2725-109">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="a2725-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2725-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2725-111">Alias d’un chemin d’accès configuré en tant que partage sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="a2725-111">The alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="a2725-112">Exemple : « public ».</span><span class="sxs-lookup"><span data-stu-id="a2725-112">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="a2725-113">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2725-113">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2725-114">Type de ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="a2725-114">Type of resource being shared.</span></span> <span data-ttu-id="a2725-115">Les types sont les suivants : lecteurs de disque, files d’attente à l’impression, communications interprocessus (IPC) et périphériques généraux.</span><span class="sxs-lookup"><span data-stu-id="a2725-115">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span data-ttu-id="a2725-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="a2725-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="a2725-117">Lecteur de disque</span><span class="sxs-lookup"><span data-stu-id="a2725-117">Disk Drive</span></span>

</dd> <dt>

<span data-ttu-id="a2725-118">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a2725-118">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="a2725-119">File d'attente d'impression</span><span class="sxs-lookup"><span data-stu-id="a2725-119">Print Queue</span></span>

</dd> <dt>

<span data-ttu-id="a2725-120">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="a2725-120">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="a2725-121">Appareil</span><span class="sxs-lookup"><span data-stu-id="a2725-121">Device</span></span>

</dd> <dt>

<span data-ttu-id="a2725-122">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="a2725-122">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="a2725-123">IPC</span><span class="sxs-lookup"><span data-stu-id="a2725-123">IPC</span></span>

</dd> <dt>

<span data-ttu-id="a2725-124">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="a2725-124">2147483648 (0x80000000)</span></span>
</dt> <dd>

<span data-ttu-id="a2725-125">Administrateur du lecteur de disque</span><span class="sxs-lookup"><span data-stu-id="a2725-125">Disk Drive Admin</span></span>

</dd> <dt>

<span data-ttu-id="a2725-126">2147483649 (0x80000001)</span><span class="sxs-lookup"><span data-stu-id="a2725-126">2147483649 (0x80000001)</span></span>
</dt> <dd>

<span data-ttu-id="a2725-127">Administrateur de file d’attente à l’impression</span><span class="sxs-lookup"><span data-stu-id="a2725-127">Print Queue Admin</span></span>

</dd> <dt>

<span data-ttu-id="a2725-128">2147483650 (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="a2725-128">2147483650 (0x80000002)</span></span>
</dt> <dd>

<span data-ttu-id="a2725-129">Administrateur de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a2725-129">Device Admin</span></span>

</dd> <dt>

<span data-ttu-id="a2725-130">2147483651 (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="a2725-130">2147483651 (0x80000003)</span></span>
</dt> <dd>

<span data-ttu-id="a2725-131">Administrateur IPC</span><span class="sxs-lookup"><span data-stu-id="a2725-131">IPC Admin</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a2725-132">*MaximumAllowed* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a2725-132">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2725-133">Limite du nombre maximal d’utilisateurs autorisés à utiliser cette ressource simultanément.</span><span class="sxs-lookup"><span data-stu-id="a2725-133">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="a2725-134">*Description* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a2725-134">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2725-135">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a2725-135">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a2725-136">*Mot de passe* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a2725-136">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2725-137">TBD</span><span class="sxs-lookup"><span data-stu-id="a2725-137">TBD</span></span>

</dd> <dt>

<span data-ttu-id="a2725-138">*Accès* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a2725-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2725-139">Instance incorporée facultative d’une classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) qui contient le descripteur de sécurité pour le nouveau partage.</span><span class="sxs-lookup"><span data-stu-id="a2725-139">Optional embedded instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class that contains the security descriptor for the new share.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2725-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2725-140">Requirements</span></span>



| <span data-ttu-id="a2725-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2725-141">Requirement</span></span> | <span data-ttu-id="a2725-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2725-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2725-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2725-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a2725-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2725-144">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="a2725-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2725-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a2725-146">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2725-146">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a2725-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a2725-147">Namespace</span></span><br/>                | <span data-ttu-id="a2725-148">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a2725-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2725-149">MOF</span><span class="sxs-lookup"><span data-stu-id="a2725-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2725-150"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2725-150"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2725-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a2725-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2725-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2725-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2725-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2725-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2725-154">**\_ClusterShare Win32**</span><span class="sxs-lookup"><span data-stu-id="a2725-154">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

