---
description: La méthode statique de la classe WMI EnableDNS active le système DNS (Domain Name System) pour le service.
ms.assetid: 083dccb1-eb38-4ae5-a252-0001759c0f50
ms.tgt_platform: multiple
title: Méthode EnableDNS de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDNS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc217211455d8804de47b2b3ffc761d4328fa49a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110514"
---
# <a name="enabledns-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="44f79-103">Méthode EnableDNS de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="44f79-103">EnableDNS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="44f79-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableDNS** active le système DNS (Domain Name System) pour le service.</span><span class="sxs-lookup"><span data-stu-id="44f79-104">The **EnableDNS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables the Domain Name System (DNS) for service.</span></span>

<span data-ttu-id="44f79-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="44f79-105">This topic uses the Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="44f79-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="44f79-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="44f79-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44f79-107">Syntax</span></span>


```mof
uint32 EnableDNS(
  [in, optional] string DNSHostName,
  [in, optional] string DNSDomain,
  [in, optional] string DNSServerSearchOrder[],
  [in, optional] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="44f79-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44f79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f79-109">*DNSHostName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="44f79-109">*DNSHostName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44f79-110">Nom de l’hôte DNS que cette méthode active.</span><span class="sxs-lookup"><span data-stu-id="44f79-110">Name of the DNS host that this method enables.</span></span>

<span data-ttu-id="44f79-111">Exemple : « corpdns »</span><span class="sxs-lookup"><span data-stu-id="44f79-111">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="44f79-112">*Dnsdomain* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="44f79-112">*DNSDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44f79-113">Représente un nom d’organisation suivi d’un point et d’une extension qui indique le type d’organisation.</span><span class="sxs-lookup"><span data-stu-id="44f79-113">Represents an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="44f79-114">Exemple : « microsoft.com »</span><span class="sxs-lookup"><span data-stu-id="44f79-114">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="44f79-115">*DNSServerSearchOrder* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="44f79-115">*DNSServerSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44f79-116">Liste des adresses IP de serveur à interroger pour les serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="44f79-116">List of server IP addresses to query for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-117">*DNSDomainSuffixSearchOrder* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="44f79-117">*DNSDomainSuffixSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44f79-118">Suffixe de domaine DNS ajouté à un nom d’hôte lors de la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="44f79-118">DNS domain suffix that is appended to a host name during name resolution.</span></span> <span data-ttu-id="44f79-119">Lors de la résolution d’un nom de domaine complet (FQDN) à partir d’un nom d’hôte uniquement, le système ajoute le nom de domaine local.</span><span class="sxs-lookup"><span data-stu-id="44f79-119">When resolving a fully qualified domain name (FQDN) from a host-only name, the system appends the local domain name.</span></span> <span data-ttu-id="44f79-120">Si la résolution de noms échoue, le système utilise la liste de suffixes de domaine pour créer des noms de domaine complets supplémentaires dans l’ordre indiqué, puis interroge les serveurs DNS pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="44f79-120">If the name resolution is not successful, the system uses the domain suffix list to create additional FQDNs in the order listed, and then queries DNS servers for each one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f79-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44f79-121">Return value</span></span>

<span data-ttu-id="44f79-122">Retourne la valeur 0 (zéro) pour une exécution réussie lorsqu’un redémarrage n’est pas nécessaire, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et tout autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="44f79-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="44f79-123">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="44f79-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="44f79-124">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="44f79-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="44f79-125">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="44f79-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-126">0</span><span class="sxs-lookup"><span data-stu-id="44f79-126">0</span></span>

<span data-ttu-id="44f79-127">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="44f79-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-128">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="44f79-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-129">1</span><span class="sxs-lookup"><span data-stu-id="44f79-129">1</span></span>

<span data-ttu-id="44f79-130">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="44f79-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-131">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="44f79-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-132">64</span><span class="sxs-lookup"><span data-stu-id="44f79-132">64</span></span>

<span data-ttu-id="44f79-133">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="44f79-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-134">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="44f79-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-135">65</span><span class="sxs-lookup"><span data-stu-id="44f79-135">65</span></span>

<span data-ttu-id="44f79-136">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="44f79-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-137">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-138">66</span><span class="sxs-lookup"><span data-stu-id="44f79-138">66</span></span>

<span data-ttu-id="44f79-139">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-140">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="44f79-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-141">67</span><span class="sxs-lookup"><span data-stu-id="44f79-141">67</span></span>

<span data-ttu-id="44f79-142">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="44f79-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-143">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-144">68</span><span class="sxs-lookup"><span data-stu-id="44f79-144">68</span></span>

<span data-ttu-id="44f79-145">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-146">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="44f79-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-147">69</span><span class="sxs-lookup"><span data-stu-id="44f79-147">69</span></span>

<span data-ttu-id="44f79-148">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="44f79-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-149">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-150">70</span><span class="sxs-lookup"><span data-stu-id="44f79-150">70</span></span>

<span data-ttu-id="44f79-151">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-152">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-153">71</span><span class="sxs-lookup"><span data-stu-id="44f79-153">71</span></span>

<span data-ttu-id="44f79-154">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-155">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="44f79-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-156">72</span><span class="sxs-lookup"><span data-stu-id="44f79-156">72</span></span>

<span data-ttu-id="44f79-157">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="44f79-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-158">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-159">73</span><span class="sxs-lookup"><span data-stu-id="44f79-159">73</span></span>

<span data-ttu-id="44f79-160">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-161">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-162">74</span><span class="sxs-lookup"><span data-stu-id="44f79-162">74</span></span>

<span data-ttu-id="44f79-163">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-164">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="44f79-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-165">75</span><span class="sxs-lookup"><span data-stu-id="44f79-165">75</span></span>

<span data-ttu-id="44f79-166">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="44f79-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-167">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-168">76</span><span class="sxs-lookup"><span data-stu-id="44f79-168">76</span></span>

<span data-ttu-id="44f79-169">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-170">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-171">77</span><span class="sxs-lookup"><span data-stu-id="44f79-171">77</span></span>

<span data-ttu-id="44f79-172">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-173">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="44f79-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-174">78</span><span class="sxs-lookup"><span data-stu-id="44f79-174">78</span></span>

<span data-ttu-id="44f79-175">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="44f79-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-176">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-177">79</span><span class="sxs-lookup"><span data-stu-id="44f79-177">79</span></span>

<span data-ttu-id="44f79-178">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-179">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="44f79-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-180">80</span><span class="sxs-lookup"><span data-stu-id="44f79-180">80</span></span>

<span data-ttu-id="44f79-181">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="44f79-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-182">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="44f79-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-183">81</span><span class="sxs-lookup"><span data-stu-id="44f79-183">81</span></span>

<span data-ttu-id="44f79-184">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="44f79-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-185">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="44f79-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-186">82</span><span class="sxs-lookup"><span data-stu-id="44f79-186">82</span></span>

<span data-ttu-id="44f79-187">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="44f79-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-188">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="44f79-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-189">83</span><span class="sxs-lookup"><span data-stu-id="44f79-189">83</span></span>

<span data-ttu-id="44f79-190">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="44f79-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-191">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="44f79-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-192">84</span><span class="sxs-lookup"><span data-stu-id="44f79-192">84</span></span>

<span data-ttu-id="44f79-193">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="44f79-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-194">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="44f79-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-195">85 %</span><span class="sxs-lookup"><span data-stu-id="44f79-195">85</span></span>

<span data-ttu-id="44f79-196">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="44f79-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-197">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="44f79-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-198">86</span><span class="sxs-lookup"><span data-stu-id="44f79-198">86</span></span>

<span data-ttu-id="44f79-199">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="44f79-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-200">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-201">87</span><span class="sxs-lookup"><span data-stu-id="44f79-201">87</span></span>

<span data-ttu-id="44f79-202">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-203">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="44f79-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-204">88</span><span class="sxs-lookup"><span data-stu-id="44f79-204">88</span></span>

<span data-ttu-id="44f79-205">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="44f79-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-206">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="44f79-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-207">89</span><span class="sxs-lookup"><span data-stu-id="44f79-207">89</span></span>

<span data-ttu-id="44f79-208">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="44f79-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-209">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="44f79-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-210">90</span><span class="sxs-lookup"><span data-stu-id="44f79-210">90</span></span>

<span data-ttu-id="44f79-211">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="44f79-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-212">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="44f79-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-213">91</span><span class="sxs-lookup"><span data-stu-id="44f79-213">91</span></span>

<span data-ttu-id="44f79-214">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="44f79-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-215">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="44f79-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-216">92</span><span class="sxs-lookup"><span data-stu-id="44f79-216">92</span></span>

<span data-ttu-id="44f79-217">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="44f79-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-218">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="44f79-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-219">93</span><span class="sxs-lookup"><span data-stu-id="44f79-219">93</span></span>

<span data-ttu-id="44f79-220">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="44f79-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-221">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="44f79-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-222">94</span><span class="sxs-lookup"><span data-stu-id="44f79-222">94</span></span>

<span data-ttu-id="44f79-223">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="44f79-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-224">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="44f79-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-225">95</span><span class="sxs-lookup"><span data-stu-id="44f79-225">95</span></span>

<span data-ttu-id="44f79-226">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="44f79-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-227">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="44f79-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-228">96</span><span class="sxs-lookup"><span data-stu-id="44f79-228">96</span></span>

<span data-ttu-id="44f79-229">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="44f79-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-230">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="44f79-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-231">97</span><span class="sxs-lookup"><span data-stu-id="44f79-231">97</span></span>

<span data-ttu-id="44f79-232">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="44f79-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-233">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="44f79-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-234">98</span><span class="sxs-lookup"><span data-stu-id="44f79-234">98</span></span>

<span data-ttu-id="44f79-235">Tous les baux DHCP ne peuvent pas être libérés ni renouvelés.</span><span class="sxs-lookup"><span data-stu-id="44f79-235">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-236">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="44f79-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-237">100</span><span class="sxs-lookup"><span data-stu-id="44f79-237">100</span></span>

<span data-ttu-id="44f79-238">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="44f79-238">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="44f79-239">**Autres**</span><span class="sxs-lookup"><span data-stu-id="44f79-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="44f79-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="44f79-240">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="44f79-241">Exemples</span><span class="sxs-lookup"><span data-stu-id="44f79-241">Examples</span></span>

<span data-ttu-id="44f79-242">L’exemple de code suivant, tiré de l’exemple de code VBScript [Activer DNS sur toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) de la Galerie TechNet, active DNS pour toutes les cartes réseau d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="44f79-242">The following code sample, taken from the [Enable DNS on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) VBScript code sample on TechNet Gallery, enables DNS for all network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
strHostName = "fabrikam1" 
arrDNSSuffixes = Array("hr.fabrikam.com", "research.fabrikam.com") 
objNetworkSettings.EnableDNS strHostName, , , arrDNSSuffixes 
```



## <a name="requirements"></a><span data-ttu-id="44f79-243">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44f79-243">Requirements</span></span>



| <span data-ttu-id="44f79-244">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44f79-244">Requirement</span></span> | <span data-ttu-id="44f79-245">Valeur</span><span class="sxs-lookup"><span data-stu-id="44f79-245">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44f79-246">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44f79-246">Minimum supported client</span></span><br/> | <span data-ttu-id="44f79-247">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44f79-247">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44f79-248">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44f79-248">Minimum supported server</span></span><br/> | <span data-ttu-id="44f79-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44f79-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44f79-250">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="44f79-250">Namespace</span></span><br/>                | <span data-ttu-id="44f79-251">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="44f79-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44f79-252">MOF</span><span class="sxs-lookup"><span data-stu-id="44f79-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44f79-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44f79-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44f79-254">DLL</span><span class="sxs-lookup"><span data-stu-id="44f79-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44f79-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44f79-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44f79-256">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44f79-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f79-257">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="44f79-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="44f79-258">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="44f79-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="44f79-259">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="44f79-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="44f79-260">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="44f79-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="44f79-261">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="44f79-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

