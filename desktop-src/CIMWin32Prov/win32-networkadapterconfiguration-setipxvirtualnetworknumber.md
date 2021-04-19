---
description: Définit le numéro de réseau virtuel IPX sur le système de l’ordinateur cible.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Méthode SetIPXVirtualNetworkNumber de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514545"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ba77e-103">Méthode SetIPXVirtualNetworkNumber de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba77e-103">SetIPXVirtualNetworkNumber method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ba77e-104">Définit le numéro de réseau virtuel IPX sur le système de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="ba77e-104">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span> <span data-ttu-id="ba77e-105">Windows 2000 et Windows NT 3,51 ou version ultérieure utilisent un numéro de réseau interne pour le routage interne.</span><span class="sxs-lookup"><span data-stu-id="ba77e-105">Windows 2000 and Windows NT 3.51 or greater uses an internal network number for internal routing.</span></span> <span data-ttu-id="ba77e-106">Le numéro de réseau interne est également appelé « numéro de réseau virtuel ».</span><span class="sxs-lookup"><span data-stu-id="ba77e-106">The internal network number is also known as a virtual network number.</span></span> <span data-ttu-id="ba77e-107">Il identifie de façon unique le système informatique sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="ba77e-107">It uniquely identifies the computer system on the network.</span></span> <span data-ttu-id="ba77e-108">La méthode retourne une valeur entière qui peut être interprétée comme suit :</span><span class="sxs-lookup"><span data-stu-id="ba77e-108">The method returns an integer value that can be interpretted as follows:</span></span>

## <a name="syntax"></a><span data-ttu-id="ba77e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba77e-109">Syntax</span></span>


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a><span data-ttu-id="ba77e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba77e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba77e-111">*IPXVirtualNetNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba77e-111">*IPXVirtualNetNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba77e-112">Numéro de réseau virtuel pour ce système.</span><span class="sxs-lookup"><span data-stu-id="ba77e-112">The virtual network number for this system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba77e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba77e-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="ba77e-114">**Exécution réussie, aucun redémarrage requis** (0)</span><span class="sxs-lookup"><span data-stu-id="ba77e-114">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-115">**Achèvement réussi, redémarrage requis** (1)</span><span class="sxs-lookup"><span data-stu-id="ba77e-115">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-116">**Méthode non prise en charge sur cette plateforme** (64)</span><span class="sxs-lookup"><span data-stu-id="ba77e-116">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-117">**Échec inconnu** (65)</span><span class="sxs-lookup"><span data-stu-id="ba77e-117">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-118">**Masque de sous-réseau non valide** (66)</span><span class="sxs-lookup"><span data-stu-id="ba77e-118">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-119">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée** (67)</span><span class="sxs-lookup"><span data-stu-id="ba77e-119">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-120">**Paramètre d’entrée non valide** (68)</span><span class="sxs-lookup"><span data-stu-id="ba77e-120">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-121">**Plus de 5 passerelles spécifiées** (69)</span><span class="sxs-lookup"><span data-stu-id="ba77e-121">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-122">**Adresse IP non valide** (70)</span><span class="sxs-lookup"><span data-stu-id="ba77e-122">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-123">**Adresse IP de passerelle non valide** (71)</span><span class="sxs-lookup"><span data-stu-id="ba77e-123">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-124">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées** (72)</span><span class="sxs-lookup"><span data-stu-id="ba77e-124">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-125">**Nom de domaine non valide** (73)</span><span class="sxs-lookup"><span data-stu-id="ba77e-125">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-126">**Nom d’hôte non valide** (74)</span><span class="sxs-lookup"><span data-stu-id="ba77e-126">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-127">**Aucun serveur WINS principal/secondaire défini** (75)</span><span class="sxs-lookup"><span data-stu-id="ba77e-127">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-128">**Fichier non valide** (76)</span><span class="sxs-lookup"><span data-stu-id="ba77e-128">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-129">**Chemin système non valide** (77)</span><span class="sxs-lookup"><span data-stu-id="ba77e-129">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-130">**Échec** de la copie du fichier (78)</span><span class="sxs-lookup"><span data-stu-id="ba77e-130">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-131">**Paramètre de sécurité non valide** (79)</span><span class="sxs-lookup"><span data-stu-id="ba77e-131">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-132">**Impossible de configurer le service TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="ba77e-132">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-133">**Impossible de configurer le service DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="ba77e-133">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-134">**Impossible de renouveler le bail DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="ba77e-134">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-135">**Impossible de libérer le bail DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="ba77e-135">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-136">**IP non activé sur l’adaptateur** (84)</span><span class="sxs-lookup"><span data-stu-id="ba77e-136">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-137">**IPX non activé sur l’adaptateur** (85)</span><span class="sxs-lookup"><span data-stu-id="ba77e-137">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-138">**Erreur liée à un nombre de trames/réseau** (86)</span><span class="sxs-lookup"><span data-stu-id="ba77e-138">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-139">**Type de trame non valide** (87)</span><span class="sxs-lookup"><span data-stu-id="ba77e-139">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-140">**Numéro de réseau non valide** (88)</span><span class="sxs-lookup"><span data-stu-id="ba77e-140">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-141">**Numéro de réseau en double** (89)</span><span class="sxs-lookup"><span data-stu-id="ba77e-141">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-142">**Paramètre hors limites** (90)</span><span class="sxs-lookup"><span data-stu-id="ba77e-142">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-143">**Accès refusé** (91)</span><span class="sxs-lookup"><span data-stu-id="ba77e-143">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-144">**Mémoire insuffisante** (92)</span><span class="sxs-lookup"><span data-stu-id="ba77e-144">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-145">**Existe déjà** (93)</span><span class="sxs-lookup"><span data-stu-id="ba77e-145">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-146">**Chemin d’accès, fichier ou objet introuvable** (94)</span><span class="sxs-lookup"><span data-stu-id="ba77e-146">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-147">**Impossible de notifier le service** (95)</span><span class="sxs-lookup"><span data-stu-id="ba77e-147">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-148">**Impossible d’informer le service DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="ba77e-148">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-149">**Interface non configurable** (97)</span><span class="sxs-lookup"><span data-stu-id="ba77e-149">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-150">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés** (98)</span><span class="sxs-lookup"><span data-stu-id="ba77e-150">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-151">**DHCP n’est pas activé sur la carte** (100)</span><span class="sxs-lookup"><span data-stu-id="ba77e-151">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="ba77e-152">**Autre** (101 à 4294967295)</span><span class="sxs-lookup"><span data-stu-id="ba77e-152">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ba77e-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba77e-153">Requirements</span></span>



| <span data-ttu-id="ba77e-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba77e-154">Requirement</span></span> | <span data-ttu-id="ba77e-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba77e-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba77e-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba77e-156">Minimum supported client</span></span><br/> | <span data-ttu-id="ba77e-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba77e-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba77e-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba77e-158">Minimum supported server</span></span><br/> | <span data-ttu-id="ba77e-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba77e-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba77e-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ba77e-160">Namespace</span></span><br/>                | <span data-ttu-id="ba77e-161">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ba77e-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ba77e-162">MOF</span><span class="sxs-lookup"><span data-stu-id="ba77e-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba77e-163"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba77e-163"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba77e-164">DLL</span><span class="sxs-lookup"><span data-stu-id="ba77e-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba77e-165"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba77e-165"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba77e-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba77e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba77e-167">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="ba77e-167">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




