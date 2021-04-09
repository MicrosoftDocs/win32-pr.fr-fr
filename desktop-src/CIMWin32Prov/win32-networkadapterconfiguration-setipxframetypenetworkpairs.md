---
description: Définit le numéro de réseau ou les paires de trames IPX pour cette carte réseau.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Méthode SetIPXFrameTypeNetworkPairs de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111355"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="4350a-103">Méthode SetIPXFrameTypeNetworkPairs de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="4350a-103">SetIPXFrameTypeNetworkPairs method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="4350a-104">Définit le numéro de réseau ou les paires de trames IPX pour cette carte réseau.</span><span class="sxs-lookup"><span data-stu-id="4350a-104">Sets the Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span>

<span data-ttu-id="4350a-105">Windows 2000 et Windows NT 3,51 et versions ultérieures utilisent un numéro de réseau IPX à des fins de routage.</span><span class="sxs-lookup"><span data-stu-id="4350a-105">Windows 2000 and Windows NT 3.51 and higher use an IPX network number for routing purposes.</span></span> <span data-ttu-id="4350a-106">Elle est affectée à chaque combinaison de type de trame/carte réseau configurée sur votre système informatique.</span><span class="sxs-lookup"><span data-stu-id="4350a-106">It is assigned to each configured frame type/network adapter combination on your computer system.</span></span> <span data-ttu-id="4350a-107">Ce nombre est parfois appelé « numéro de réseau externe ».</span><span class="sxs-lookup"><span data-stu-id="4350a-107">This number is sometimes referred to as the "external network number."</span></span> <span data-ttu-id="4350a-108">Elle doit être unique pour chaque segment de réseau.</span><span class="sxs-lookup"><span data-stu-id="4350a-108">It must be unique for each network segment.</span></span> <span data-ttu-id="4350a-109">Si le type de trame est défini sur AUTO, le numéro de réseau doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4350a-109">If the frame type is set to AUTO, the network number should to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="4350a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4350a-110">Syntax</span></span>


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a><span data-ttu-id="4350a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4350a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4350a-112">*IPXNetworkNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4350a-112">*IPXNetworkNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4350a-113">Tableau de caractères qui identifient de façon unique un adaptateur sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="4350a-113">An array of characters that uniquely identify an adapter on the computer system.</span></span> <span data-ttu-id="4350a-114">Le transport compatible IPX/SPX NetWare Link (NWLink) dans Windows 2000 et Windows NT 3,51 ou version ultérieure utilise deux types de numéros de réseau différents.</span><span class="sxs-lookup"><span data-stu-id="4350a-114">The NetWare Link (NWLink) IPX/SPX-compatible transport in Windows 2000 and Windows NT 3.51 or higher, uses two different types of network numbers.</span></span> <span data-ttu-id="4350a-115">Ce nombre est parfois appelé numéro de réseau externe.</span><span class="sxs-lookup"><span data-stu-id="4350a-115">This number is sometimes referred to as the External Network Number.</span></span> <span data-ttu-id="4350a-116">Elle doit être unique pour chaque segment de réseau.</span><span class="sxs-lookup"><span data-stu-id="4350a-116">It must be unique for each network segment.</span></span> <span data-ttu-id="4350a-117">Les valeurs de cette liste de chaînes doivent avoir une valeur correspondante dans le paramètre IPXFrameType identifiant le type de trame de paquet utilisé pour ce réseau.</span><span class="sxs-lookup"><span data-stu-id="4350a-117">The values in this string list must have a corresponding value in the IPXFrameType parameter identifying the packet frame type used for this network.</span></span>

</dd> <dt>

<span data-ttu-id="4350a-118">*IPXFrameType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4350a-118">*IPXFrameType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4350a-119">Tableau d’entiers des identificateurs de type de frame.</span><span class="sxs-lookup"><span data-stu-id="4350a-119">An integer array of frame type identifiers.</span></span> <span data-ttu-id="4350a-120">Les valeurs de ce tableau correspondent aux éléments dans le paramètre *IPXNetworkNumber* .</span><span class="sxs-lookup"><span data-stu-id="4350a-120">The values in this array correspond to the elements in the *IPXNetworkNumber* parameter.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="4350a-121">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="4350a-121">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="4350a-122">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="4350a-122">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="4350a-123">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="4350a-123">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="4350a-124">**Snap Ethernet** (3)</span><span class="sxs-lookup"><span data-stu-id="4350a-124">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="4350a-125">**Automatique** (255)</span><span class="sxs-lookup"><span data-stu-id="4350a-125">**AUTO** (255)</span></span>


<span data-ttu-id="4350a-126"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4350a-126"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="4350a-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4350a-127">Return value</span></span>

<dl> <dt>

<span data-ttu-id="4350a-128">**Exécution réussie, aucun redémarrage requis** (0)</span><span class="sxs-lookup"><span data-stu-id="4350a-128">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-129">**Achèvement réussi, redémarrage requis** (1)</span><span class="sxs-lookup"><span data-stu-id="4350a-129">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-130">**Méthode non prise en charge sur cette plateforme** (64)</span><span class="sxs-lookup"><span data-stu-id="4350a-130">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-131">**Échec inconnu** (65)</span><span class="sxs-lookup"><span data-stu-id="4350a-131">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-132">**Masque de sous-réseau non valide** (66)</span><span class="sxs-lookup"><span data-stu-id="4350a-132">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-133">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée** (67)</span><span class="sxs-lookup"><span data-stu-id="4350a-133">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-134">**Paramètre d’entrée non valide** (68)</span><span class="sxs-lookup"><span data-stu-id="4350a-134">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-135">**Plus de 5 passerelles spécifiées** (69)</span><span class="sxs-lookup"><span data-stu-id="4350a-135">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-136">**Adresse IP non valide** (70)</span><span class="sxs-lookup"><span data-stu-id="4350a-136">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-137">**Adresse IP de passerelle non valide** (71)</span><span class="sxs-lookup"><span data-stu-id="4350a-137">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-138">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées** (72)</span><span class="sxs-lookup"><span data-stu-id="4350a-138">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-139">**Nom de domaine non valide** (73)</span><span class="sxs-lookup"><span data-stu-id="4350a-139">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-140">**Nom d’hôte non valide** (74)</span><span class="sxs-lookup"><span data-stu-id="4350a-140">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-141">**Aucun serveur WINS principal/secondaire défini** (75)</span><span class="sxs-lookup"><span data-stu-id="4350a-141">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-142">**Fichier non valide** (76)</span><span class="sxs-lookup"><span data-stu-id="4350a-142">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-143">**Chemin système non valide** (77)</span><span class="sxs-lookup"><span data-stu-id="4350a-143">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-144">**Échec** de la copie du fichier (78)</span><span class="sxs-lookup"><span data-stu-id="4350a-144">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-145">**Paramètre de sécurité non valide** (79)</span><span class="sxs-lookup"><span data-stu-id="4350a-145">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-146">**Impossible de configurer le service TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="4350a-146">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-147">**Impossible de configurer le service DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="4350a-147">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-148">**Impossible de renouveler le bail DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="4350a-148">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-149">**Impossible de libérer le bail DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="4350a-149">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-150">**IP non activé sur l’adaptateur** (84)</span><span class="sxs-lookup"><span data-stu-id="4350a-150">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-151">**IPX non activé sur l’adaptateur** (85)</span><span class="sxs-lookup"><span data-stu-id="4350a-151">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-152">**Erreur liée à un nombre de trames/réseau** (86)</span><span class="sxs-lookup"><span data-stu-id="4350a-152">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-153">**Type de trame non valide** (87)</span><span class="sxs-lookup"><span data-stu-id="4350a-153">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-154">**Numéro de réseau non valide** (88)</span><span class="sxs-lookup"><span data-stu-id="4350a-154">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-155">**Numéro de réseau en double** (89)</span><span class="sxs-lookup"><span data-stu-id="4350a-155">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-156">**Paramètre hors limites** (90)</span><span class="sxs-lookup"><span data-stu-id="4350a-156">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-157">**Accès refusé** (91)</span><span class="sxs-lookup"><span data-stu-id="4350a-157">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-158">**Mémoire insuffisante** (92)</span><span class="sxs-lookup"><span data-stu-id="4350a-158">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-159">**Existe déjà** (93)</span><span class="sxs-lookup"><span data-stu-id="4350a-159">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-160">**Chemin d’accès, fichier ou objet introuvable** (94)</span><span class="sxs-lookup"><span data-stu-id="4350a-160">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-161">**Impossible de notifier le service** (95)</span><span class="sxs-lookup"><span data-stu-id="4350a-161">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-162">**Impossible d’informer le service DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="4350a-162">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-163">**Interface non configurable** (97)</span><span class="sxs-lookup"><span data-stu-id="4350a-163">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-164">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés** (98)</span><span class="sxs-lookup"><span data-stu-id="4350a-164">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-165">**DHCP n’est pas activé sur la carte** (100)</span><span class="sxs-lookup"><span data-stu-id="4350a-165">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="4350a-166">**Autre** (101 à 4294967295)</span><span class="sxs-lookup"><span data-stu-id="4350a-166">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4350a-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4350a-167">Requirements</span></span>



| <span data-ttu-id="4350a-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4350a-168">Requirement</span></span> | <span data-ttu-id="4350a-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="4350a-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4350a-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4350a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4350a-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4350a-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4350a-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4350a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4350a-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4350a-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4350a-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4350a-174">Namespace</span></span><br/>                | <span data-ttu-id="4350a-175">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4350a-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4350a-176">MOF</span><span class="sxs-lookup"><span data-stu-id="4350a-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4350a-177"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4350a-177"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4350a-178">DLL</span><span class="sxs-lookup"><span data-stu-id="4350a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4350a-179"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4350a-179"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4350a-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4350a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4350a-181">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="4350a-181">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




