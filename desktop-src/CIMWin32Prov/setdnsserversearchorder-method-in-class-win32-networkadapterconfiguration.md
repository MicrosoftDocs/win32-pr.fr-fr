---
description: SetDNSServerSearchOrder &\# 32 ; La méthode de classe WMI utilise un tableau d’éléments de chaîne pour définir l’ordre de recherche du serveur.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Méthode SetDNSServerSearchOrder de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033724"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="acf64-103">Méthode SetDNSServerSearchOrder de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf64-103">SetDNSServerSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="acf64-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSServerSearchOrder** utilise un tableau d’éléments de chaîne pour définir l’ordre de recherche du serveur.</span><span class="sxs-lookup"><span data-stu-id="acf64-104">The **SetDNSServerSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses an array of string elements to set the server search order.</span></span>

<span data-ttu-id="acf64-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="acf64-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="acf64-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="acf64-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="acf64-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acf64-107">Syntax</span></span>


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="acf64-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acf64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf64-109">*DNSServerSearchOrder* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acf64-109">*DNSServerSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acf64-110">Liste des adresses IP de serveur à interroger pour les serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="acf64-110">List of server IP addresses to query for DNS servers.</span></span>

<span data-ttu-id="acf64-111">Exemple : 130.215.24.1 ou 157.54.164.1</span><span class="sxs-lookup"><span data-stu-id="acf64-111">Example: 130.215.24.1 or 157.54.164.1</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf64-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acf64-112">Return value</span></span>

<span data-ttu-id="acf64-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="acf64-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="acf64-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="acf64-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="acf64-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="acf64-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="acf64-116">**Exécution réussie, aucun redémarrage requis** (0)</span><span class="sxs-lookup"><span data-stu-id="acf64-116">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-117">**Achèvement réussi, redémarrage requis** (1)</span><span class="sxs-lookup"><span data-stu-id="acf64-117">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-118">**Méthode non prise en charge sur cette plateforme** (64)</span><span class="sxs-lookup"><span data-stu-id="acf64-118">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-119">**Échec inconnu** (65)</span><span class="sxs-lookup"><span data-stu-id="acf64-119">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-120">**Masque de sous-réseau non valide** (66)</span><span class="sxs-lookup"><span data-stu-id="acf64-120">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-121">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée** (67)</span><span class="sxs-lookup"><span data-stu-id="acf64-121">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-122">**Paramètre d’entrée non valide** (68)</span><span class="sxs-lookup"><span data-stu-id="acf64-122">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-123">**Plus de 5 passerelles spécifiées** (69)</span><span class="sxs-lookup"><span data-stu-id="acf64-123">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-124">**Adresse IP non valide** (70)</span><span class="sxs-lookup"><span data-stu-id="acf64-124">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-125">**Adresse IP de passerelle non valide** (71)</span><span class="sxs-lookup"><span data-stu-id="acf64-125">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-126">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées** (72)</span><span class="sxs-lookup"><span data-stu-id="acf64-126">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-127">**Nom de domaine non valide** (73)</span><span class="sxs-lookup"><span data-stu-id="acf64-127">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-128">**Nom d’hôte non valide** (74)</span><span class="sxs-lookup"><span data-stu-id="acf64-128">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-129">**Aucun serveur WINS principal/secondaire défini** (75)</span><span class="sxs-lookup"><span data-stu-id="acf64-129">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-130">**Fichier non valide** (76)</span><span class="sxs-lookup"><span data-stu-id="acf64-130">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-131">**Chemin système non valide** (77)</span><span class="sxs-lookup"><span data-stu-id="acf64-131">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-132">**Échec** de la copie du fichier (78)</span><span class="sxs-lookup"><span data-stu-id="acf64-132">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-133">**Paramètre de sécurité non valide** (79)</span><span class="sxs-lookup"><span data-stu-id="acf64-133">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-134">**Impossible de configurer le service TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="acf64-134">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-135">**Impossible de configurer le service DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="acf64-135">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-136">**Impossible de renouveler le bail DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="acf64-136">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-137">**Impossible de libérer le bail DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="acf64-137">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-138">**IP non activé sur l’adaptateur** (84)</span><span class="sxs-lookup"><span data-stu-id="acf64-138">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-139">**IPX non activé sur l’adaptateur** (85)</span><span class="sxs-lookup"><span data-stu-id="acf64-139">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-140">**Erreur liée à un nombre de trames/réseau** (86)</span><span class="sxs-lookup"><span data-stu-id="acf64-140">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-141">**Type de trame non valide** (87)</span><span class="sxs-lookup"><span data-stu-id="acf64-141">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-142">**Numéro de réseau non valide** (88)</span><span class="sxs-lookup"><span data-stu-id="acf64-142">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-143">**Numéro de réseau en double** (89)</span><span class="sxs-lookup"><span data-stu-id="acf64-143">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-144">**Paramètre hors limites** (90)</span><span class="sxs-lookup"><span data-stu-id="acf64-144">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-145">**Accès refusé** (91)</span><span class="sxs-lookup"><span data-stu-id="acf64-145">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-146">**Mémoire insuffisante** (92)</span><span class="sxs-lookup"><span data-stu-id="acf64-146">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-147">**Existe déjà** (93)</span><span class="sxs-lookup"><span data-stu-id="acf64-147">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-148">**Chemin d’accès, fichier ou objet introuvable** (94)</span><span class="sxs-lookup"><span data-stu-id="acf64-148">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-149">**Impossible de notifier le service** (95)</span><span class="sxs-lookup"><span data-stu-id="acf64-149">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-150">**Impossible d’informer le service DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="acf64-150">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-151">**Interface non configurable** (97)</span><span class="sxs-lookup"><span data-stu-id="acf64-151">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-152">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés** (98)</span><span class="sxs-lookup"><span data-stu-id="acf64-152">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-153">**DHCP n’est pas activé sur la carte** (100)</span><span class="sxs-lookup"><span data-stu-id="acf64-153">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="acf64-154">**Autre** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="acf64-154">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="acf64-155">Notes</span><span class="sxs-lookup"><span data-stu-id="acf64-155">Remarks</span></span>

<span data-ttu-id="acf64-156">Il s’agit d’un appel de méthode dépendant de l’instance qui s’applique sur la base de chaque adaptateur.</span><span class="sxs-lookup"><span data-stu-id="acf64-156">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="acf64-157">Une fois que les serveurs DNS statiques sont spécifiés pour commencer à utiliser le protocole DHCP (Dynamic Host Configuration Protocol) au lieu de serveurs DNS statiques, vous pouvez appeler la méthode sans fournir de paramètres « in ».</span><span class="sxs-lookup"><span data-stu-id="acf64-157">After static DNS servers are specified to start using Dynamic Host Configuration Protocol (DHCP) instead of static DNS servers, you can call the method without supplying "in" parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="acf64-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="acf64-158">Examples</span></span>

<span data-ttu-id="acf64-159">L’exemple de [commande définir l’ordre de recherche des serveurs DNS pour plusieurs ordinateurs dans une unité d’organisation](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) dans la Galerie TechNet récupère ou définit l’ordre de recherche des serveurs DNS pour plusieurs ordinateurs appartenant à une unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="acf64-159">The [Set DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) VBScript sample on TechNet Gallery retrieves or sets DNS Server search order for multiple computers that belongs to one organizational unit.</span></span>

<span data-ttu-id="acf64-160">L’exemple de [modification de l’ordre de recherche d’un serveur DNS pour une carte réseau](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) configure une carte réseau TCP/IP pour utiliser deux serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="acf64-160">The [Modify the DNS Server Search Order for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript sample configures a TCP/IP-bound network adapter to use two DNS servers.</span></span>

## <a name="requirements"></a><span data-ttu-id="acf64-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acf64-161">Requirements</span></span>



| <span data-ttu-id="acf64-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acf64-162">Requirement</span></span> | <span data-ttu-id="acf64-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="acf64-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acf64-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acf64-164">Minimum supported client</span></span><br/> | <span data-ttu-id="acf64-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acf64-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="acf64-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acf64-166">Minimum supported server</span></span><br/> | <span data-ttu-id="acf64-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acf64-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="acf64-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="acf64-168">Namespace</span></span><br/>                | <span data-ttu-id="acf64-169">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="acf64-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="acf64-170">MOF</span><span class="sxs-lookup"><span data-stu-id="acf64-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acf64-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acf64-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="acf64-172">DLL</span><span class="sxs-lookup"><span data-stu-id="acf64-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acf64-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acf64-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acf64-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acf64-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf64-175">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="acf64-175">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="acf64-176">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="acf64-176">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="acf64-177">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="acf64-177">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="acf64-178">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="acf64-178">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="acf64-179">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="acf64-179">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

