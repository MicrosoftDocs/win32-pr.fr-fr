---
description: EnableWINS &\# 32 ; La méthode statique de la classe WMI active les paramètres WINS (Windows Internet Service de nommage) spécifiques à TCP/IP, mais indépendamment de la carte réseau.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Méthode EnableWINS de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523388"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="345da-103">Méthode EnableWINS de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="345da-103">EnableWINS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="345da-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS** permet aux paramètres WINS (Windows Internet service de nommage) spécifiques à TCP/IP, mais indépendamment de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="345da-104">The **EnableWINS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables Windows Internet Naming Service (WINS) settings specific to TCP/IP, but independent of the network adapter.</span></span>

<span data-ttu-id="345da-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="345da-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="345da-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="345da-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="345da-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="345da-107">Syntax</span></span>


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a><span data-ttu-id="345da-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="345da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="345da-109">*DNSEnabledForWINSResolution* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="345da-109">*DNSEnabledForWINSResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="345da-110">Si la **valeur est true**, le système DNS (Domain Name System) est activé pour la résolution de noms sur la résolution WINS.</span><span class="sxs-lookup"><span data-stu-id="345da-110">If **true**, the Domain Name System (DNS) is enabled for name resolution over WINS resolution.</span></span>

</dd> <dt>

<span data-ttu-id="345da-111">*WINSEnableLMHostsLookup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="345da-111">*WINSEnableLMHostsLookup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="345da-112">Si la **valeur est true**, les fichiers de recherche locaux sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="345da-112">If **true**, local lookup files are used.</span></span> <span data-ttu-id="345da-113">Les fichiers de recherche contiendront des mappages d’adresses IP aux noms d’hôtes.</span><span class="sxs-lookup"><span data-stu-id="345da-113">Lookup files will contain mappings of IP addresses to host names.</span></span>

</dd> <dt>

<span data-ttu-id="345da-114">*WINSHostLookupFile* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="345da-114">*WINSHostLookupFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="345da-115">Fichiers de recherche qui contiennent des mappages d’adresses IP à des noms d’hôtes.</span><span class="sxs-lookup"><span data-stu-id="345da-115">Lookup files that contain mappings of IP addresses to host names.</span></span> <span data-ttu-id="345da-116">S’ils sont disponibles, les fichiers se trouvent dans% SystemRoot% \\ system32 \\ drivers \\ .</span><span class="sxs-lookup"><span data-stu-id="345da-116">If available, the files will be found in %SystemRoot%\\system32\\drivers\\ .</span></span>

</dd> <dt>

<span data-ttu-id="345da-117">*WINSScopeID* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="345da-117">*WINSScopeID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="345da-118">Valeur de l’identificateur d’étendue qui sera ajoutée à la fin du nom NetBIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="345da-118">Scope identifier value that will be appended to the end of the computer's NetBIOS name.</span></span> <span data-ttu-id="345da-119">Les systèmes qui utilisent le même identificateur d’étendue peuvent communiquer avec cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="345da-119">Systems that use the same scope identifier can communicate with this computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="345da-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="345da-120">Return value</span></span>

<span data-ttu-id="345da-121">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis ; 1 (un) pour une exécution réussie lorsqu’un redémarrage est nécessaire ; nombre différent en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="345da-121">Returns a value of 0 (zero) for a successful completion when no reboot is required; 1 (one) for a successful completion when a reboot is required; a different number if there is an error.</span></span> <span data-ttu-id="345da-122">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="345da-122">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="345da-123">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="345da-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="345da-124">**Exécution réussie, aucun redémarrage requis** (0)</span><span class="sxs-lookup"><span data-stu-id="345da-124">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="345da-125">**Achèvement réussi, redémarrage requis** (1)</span><span class="sxs-lookup"><span data-stu-id="345da-125">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="345da-126">**Méthode non prise en charge sur cette plateforme** (64)</span><span class="sxs-lookup"><span data-stu-id="345da-126">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="345da-127">**Échec inconnu** (65)</span><span class="sxs-lookup"><span data-stu-id="345da-127">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="345da-128">**Masque de sous-réseau non valide** (66)</span><span class="sxs-lookup"><span data-stu-id="345da-128">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="345da-129">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée** (67)</span><span class="sxs-lookup"><span data-stu-id="345da-129">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="345da-130">**Paramètre d’entrée non valide** (68)</span><span class="sxs-lookup"><span data-stu-id="345da-130">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="345da-131">**Plus de 5 passerelles spécifiées** (69)</span><span class="sxs-lookup"><span data-stu-id="345da-131">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="345da-132">**Adresse IP non valide** (70)</span><span class="sxs-lookup"><span data-stu-id="345da-132">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="345da-133">**Adresse IP de passerelle non valide** (71)</span><span class="sxs-lookup"><span data-stu-id="345da-133">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="345da-134">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées** (72)</span><span class="sxs-lookup"><span data-stu-id="345da-134">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="345da-135">**Nom de domaine non valide** (73)</span><span class="sxs-lookup"><span data-stu-id="345da-135">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="345da-136">**Nom d’hôte non valide** (74)</span><span class="sxs-lookup"><span data-stu-id="345da-136">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="345da-137">**Aucun serveur WINS principal/secondaire défini** (75)</span><span class="sxs-lookup"><span data-stu-id="345da-137">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="345da-138">**Fichier non valide** (76)</span><span class="sxs-lookup"><span data-stu-id="345da-138">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="345da-139">**Chemin système non valide** (77)</span><span class="sxs-lookup"><span data-stu-id="345da-139">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="345da-140">**Échec** de la copie du fichier (78)</span><span class="sxs-lookup"><span data-stu-id="345da-140">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="345da-141">**Paramètre de sécurité non valide** (79)</span><span class="sxs-lookup"><span data-stu-id="345da-141">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="345da-142">**Impossible de configurer le service TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="345da-142">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="345da-143">**Impossible de configurer le service DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="345da-143">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="345da-144">**Impossible de renouveler le bail DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="345da-144">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="345da-145">**Impossible de libérer le bail DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="345da-145">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="345da-146">**IP non activé sur l’adaptateur** (84)</span><span class="sxs-lookup"><span data-stu-id="345da-146">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="345da-147">**IPX non activé sur l’adaptateur** (85)</span><span class="sxs-lookup"><span data-stu-id="345da-147">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="345da-148">**Erreur liée à un nombre de trames/réseau** (86)</span><span class="sxs-lookup"><span data-stu-id="345da-148">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="345da-149">**Type de trame non valide** (87)</span><span class="sxs-lookup"><span data-stu-id="345da-149">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="345da-150">**Numéro de réseau non valide** (88)</span><span class="sxs-lookup"><span data-stu-id="345da-150">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="345da-151">**Numéro de réseau en double** (89)</span><span class="sxs-lookup"><span data-stu-id="345da-151">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="345da-152">**Paramètre hors limites** (90)</span><span class="sxs-lookup"><span data-stu-id="345da-152">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="345da-153">**Accès refusé** (91)</span><span class="sxs-lookup"><span data-stu-id="345da-153">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="345da-154">**Mémoire insuffisante** (92)</span><span class="sxs-lookup"><span data-stu-id="345da-154">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="345da-155">**Existe déjà** (93)</span><span class="sxs-lookup"><span data-stu-id="345da-155">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="345da-156">**Chemin d’accès, fichier ou objet introuvable** (94)</span><span class="sxs-lookup"><span data-stu-id="345da-156">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="345da-157">**Impossible de notifier le service** (95)</span><span class="sxs-lookup"><span data-stu-id="345da-157">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="345da-158">**Impossible d’informer le service DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="345da-158">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="345da-159">**Interface non configurable** (97)</span><span class="sxs-lookup"><span data-stu-id="345da-159">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="345da-160">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés** (98)</span><span class="sxs-lookup"><span data-stu-id="345da-160">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="345da-161">**DHCP n’est pas activé sur la carte** (100)</span><span class="sxs-lookup"><span data-stu-id="345da-161">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="345da-162">**Autre** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="345da-162">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="345da-163">Exemples</span><span class="sxs-lookup"><span data-stu-id="345da-163">Examples</span></span>

<span data-ttu-id="345da-164">L’exemple de code [activer WINS pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript, sur la Galerie TechNet, utilise **ENABLEWINS** pour activer WINS sur toutes les cartes réseau installées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="345da-164">The [Enable WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript code sample, on TechNet Gallery, uses **EnableWINS** to Enables WINS on all the network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="345da-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="345da-165">Requirements</span></span>



| <span data-ttu-id="345da-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="345da-166">Requirement</span></span> | <span data-ttu-id="345da-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="345da-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="345da-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="345da-168">Minimum supported client</span></span><br/> | <span data-ttu-id="345da-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="345da-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="345da-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="345da-170">Minimum supported server</span></span><br/> | <span data-ttu-id="345da-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="345da-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="345da-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="345da-172">Namespace</span></span><br/>                | <span data-ttu-id="345da-173">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="345da-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="345da-174">MOF</span><span class="sxs-lookup"><span data-stu-id="345da-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="345da-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="345da-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="345da-176">DLL</span><span class="sxs-lookup"><span data-stu-id="345da-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="345da-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="345da-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="345da-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="345da-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345da-179">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="345da-179">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="345da-180">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="345da-180">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="345da-181">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="345da-181">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="345da-182">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="345da-182">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="345da-183">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="345da-183">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

