---
title: Interface ITsSbTargetEx
description: Expose les propriétés qui stockent les informations de configuration et d’état d’une cible.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface ITsSbTargetEx
- Services Bureau à distance de l’interface ITsSbTargetEx, Description
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942789"
---
# <a name="itssbtargetex-interface"></a><span data-ttu-id="b4008-105">Interface ITsSbTargetEx</span><span class="sxs-lookup"><span data-stu-id="b4008-105">ITsSbTargetEx interface</span></span>

<span data-ttu-id="b4008-106">Expose les propriétés qui stockent les informations de configuration et d’état d’une cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-106">Exposes properties that store configuration and state information about a target.</span></span>

<span data-ttu-id="b4008-107">Cette interface est uniquement disponible sur Windows Server 2012 R2 avec [KB3091411](https://support.microsoft.com/kb/3091411) installé.</span><span class="sxs-lookup"><span data-stu-id="b4008-107">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="b4008-108">La propriété [**TargetLoad**](itssbtarget-targetload.md) de l’interface [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) est disponible à partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b4008-108">The [**TargetLoad**](itssbtarget-targetload.md) property of the [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) interface is available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="b4008-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b4008-109">Members</span></span>

<span data-ttu-id="b4008-110">L’interface **ITsSbTargetEx** hérite de [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span><span class="sxs-lookup"><span data-stu-id="b4008-110">The **ITsSbTargetEx** interface inherits from [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span></span> <span data-ttu-id="b4008-111">**ITsSbTargetEx** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b4008-111">**ITsSbTargetEx** also has these types of members:</span></span>

-   [<span data-ttu-id="b4008-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4008-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4008-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4008-113">Properties</span></span>

<span data-ttu-id="b4008-114">L’interface **ITsSbTargetEx** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4008-114">The **ITsSbTargetEx** interface has these properties.</span></span>



| <span data-ttu-id="b4008-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="b4008-115">Property</span></span>                                                                      | <span data-ttu-id="b4008-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b4008-116">Access type</span></span>           | <span data-ttu-id="b4008-117">Description</span><span class="sxs-lookup"><span data-stu-id="b4008-117">Description</span></span>                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4008-118">**EnvironmentName**</span><span class="sxs-lookup"><span data-stu-id="b4008-118">**EnvironmentName**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | <span data-ttu-id="b4008-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b4008-119">Read/write</span></span><br/> | <span data-ttu-id="b4008-120">Récupère ou spécifie le nom de l’environnement associé à la cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-120">Retrieves or specifies the name of the environment associated with the target.</span></span><br/> |
| [<span data-ttu-id="b4008-121">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="b4008-121">**FarmName**</span></span>](itssbtarget-farmname.md)<br/>                           | <span data-ttu-id="b4008-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b4008-122">Read/write</span></span><br/> | <span data-ttu-id="b4008-123">Spécifie ou récupère le nom de la batterie de serveurs à laquelle cette cible est jointe.</span><span class="sxs-lookup"><span data-stu-id="b4008-123">Specifies or retrieves the name of the farm to which this target is joined.</span></span><br/>    |
| [<span data-ttu-id="b4008-124">**AdressesIP**</span><span class="sxs-lookup"><span data-stu-id="b4008-124">**IpAddresses**</span></span>](itssbtarget-ipaddresses.md)<br/>                     | <span data-ttu-id="b4008-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b4008-125">Read/write</span></span><br/> | <span data-ttu-id="b4008-126">Récupère ou spécifie les adresses IP externes de la cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-126">Retrieves or specifies the external IP addresses of the target.</span></span><br/>                |
| [<span data-ttu-id="b4008-127">**NumPendingConnections**</span><span class="sxs-lookup"><span data-stu-id="b4008-127">**NumPendingConnections**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | <span data-ttu-id="b4008-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4008-128">Read-only</span></span><br/>  | <span data-ttu-id="b4008-129">Récupère le nombre de connexions utilisateur en attente pour la cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-129">Retrieves the number of pending user connections for the target.</span></span><br/>               |
| [<span data-ttu-id="b4008-130">**NumSessions**</span><span class="sxs-lookup"><span data-stu-id="b4008-130">**NumSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | <span data-ttu-id="b4008-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4008-131">Read-only</span></span><br/>  | <span data-ttu-id="b4008-132">Récupère le nombre de sessions gérées par le répartiteur pour la cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-132">Retrieves the number of sessions maintained by broker for the target.</span></span><br/>          |
| [<span data-ttu-id="b4008-133">**TargetFQDN**</span><span class="sxs-lookup"><span data-stu-id="b4008-133">**TargetFQDN**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | <span data-ttu-id="b4008-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b4008-134">Read/write</span></span><br/> | <span data-ttu-id="b4008-135">Spécifie ou récupère le nom de domaine complet de la cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-135">Specifies or retrieves the fully qualified domain name of the target.</span></span><br/>          |
| <span data-ttu-id="b4008-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b4008-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span></span><br/>                     | <span data-ttu-id="b4008-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4008-137">Read-only</span></span><br/>  | <span data-ttu-id="b4008-138">Récupère le chargement relatif sur une cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-138">Retrieves the relative load on a target.</span></span><br/>                                       |
| [<span data-ttu-id="b4008-139">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="b4008-139">**TargetName**</span></span>](itssbtarget-targetname.md)<br/>                       | <span data-ttu-id="b4008-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b4008-140">Read/write</span></span><br/> | <span data-ttu-id="b4008-141">Spécifie ou récupère le nom de la cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-141">Specifies or retrieves the name of the target.</span></span><br/>                                 |
| [<span data-ttu-id="b4008-142">**TargetNetbios**</span><span class="sxs-lookup"><span data-stu-id="b4008-142">**TargetNetbios**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | <span data-ttu-id="b4008-143">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b4008-143">Read/write</span></span><br/> | <span data-ttu-id="b4008-144">Spécifie ou récupère le nom NetBIOS de la cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-144">Specifies or retrieves the NetBIOS name of the target.</span></span><br/>                         |
| [<span data-ttu-id="b4008-145">**TargetPropertySet**</span><span class="sxs-lookup"><span data-stu-id="b4008-145">**TargetPropertySet**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | <span data-ttu-id="b4008-146">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b4008-146">Read/write</span></span><br/> | <span data-ttu-id="b4008-147">Spécifie ou récupère le jeu de propriétés pour la cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-147">Specifies or retrieves the property set for the target.</span></span><br/>                        |
| [<span data-ttu-id="b4008-148">**TargetState**</span><span class="sxs-lookup"><span data-stu-id="b4008-148">**TargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | <span data-ttu-id="b4008-149">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b4008-149">Read/write</span></span><br/> | <span data-ttu-id="b4008-150">Spécifie ou récupère l’État cible.</span><span class="sxs-lookup"><span data-stu-id="b4008-150">Specifies or retrieves the target state.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="b4008-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4008-151">Requirements</span></span>



| <span data-ttu-id="b4008-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4008-152">Requirement</span></span> | <span data-ttu-id="b4008-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4008-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b4008-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4008-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b4008-155">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4008-155">None supported</span></span><br/>                                                        |
| <span data-ttu-id="b4008-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4008-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b4008-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b4008-157">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="b4008-158">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b4008-158">End of server support</span></span><br/>    | <span data-ttu-id="b4008-159">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b4008-159">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="b4008-160">IID</span><span class="sxs-lookup"><span data-stu-id="b4008-160">IID</span></span><br/>                      | <span data-ttu-id="b4008-161">IID \_ ITsSbTargetEx est défini en tant que 74f99987-625d-11e5-BEA1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="b4008-161">IID\_ITsSbTargetEx is defined as 74f99987-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4008-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4008-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4008-163">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="b4008-163">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="b4008-164">Bureau à distance les interfaces de virtualisation</span><span class="sxs-lookup"><span data-stu-id="b4008-164">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

