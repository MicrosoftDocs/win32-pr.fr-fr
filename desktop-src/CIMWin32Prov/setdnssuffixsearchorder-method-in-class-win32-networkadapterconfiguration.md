---
description: La méthode statique de classe WMI SetDNSSuffixSearchOrder utilise un tableau d’éléments de chaîne pour définir l’ordre de recherche du suffixe.
ms.assetid: 1ad9fc99-8c57-43d4-92d2-b12f2c1451cb
ms.tgt_platform: multiple
title: Méthode SetDNSSuffixSearchOrder de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSSuffixSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10088b1d0722f968e5d3742984baa91ec3e423aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861382"
---
# <a name="setdnssuffixsearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="9d334-103">Méthode SetDNSSuffixSearchOrder de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d334-103">SetDNSSuffixSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="9d334-104">La méthode statique de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSSuffixSearchOrder** utilise un tableau d’éléments de chaîne pour définir l’ordre de recherche du suffixe.</span><span class="sxs-lookup"><span data-stu-id="9d334-104">The **SetDNSSuffixSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method uses an array of string elements to set the suffix search order.</span></span>

<span data-ttu-id="9d334-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9d334-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9d334-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9d334-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d334-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d334-107">Syntax</span></span>


```mof
uint32 SetDNSSuffixSearchOrder(
  [in] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="9d334-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d334-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d334-109">*DNSDomainSuffixSearchOrder* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d334-109">*DNSDomainSuffixSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d334-110">Liste des suffixes de serveur à interroger pour les serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="9d334-110">List of server suffixes to query for DNS servers.</span></span> <span data-ttu-id="9d334-111">L’emplacement du Registre du suffixe DNS est **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **services** \\ **tcpip \| nameserver**</span><span class="sxs-lookup"><span data-stu-id="9d334-111">The registry location of the DNS suffix is **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Tcpip\|NameServer**</span></span>

<span data-ttu-id="9d334-112">Exemple : "suffix1.company.com", "suffix2.company.com"</span><span class="sxs-lookup"><span data-stu-id="9d334-112">Example: "suffix1.company.com", "suffix2.company.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d334-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d334-113">Return value</span></span>

<span data-ttu-id="9d334-114">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9d334-114">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="9d334-115">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9d334-115">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9d334-116">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9d334-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9d334-117">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="9d334-117">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-118">0</span><span class="sxs-lookup"><span data-stu-id="9d334-118">0</span></span>

<span data-ttu-id="9d334-119">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9d334-119">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-120">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="9d334-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-121">1</span><span class="sxs-lookup"><span data-stu-id="9d334-121">1</span></span>

<span data-ttu-id="9d334-122">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="9d334-122">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-123">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="9d334-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-124">64</span><span class="sxs-lookup"><span data-stu-id="9d334-124">64</span></span>

<span data-ttu-id="9d334-125">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="9d334-125">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-126">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="9d334-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-127">65</span><span class="sxs-lookup"><span data-stu-id="9d334-127">65</span></span>

<span data-ttu-id="9d334-128">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="9d334-128">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-129">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-129">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-130">66</span><span class="sxs-lookup"><span data-stu-id="9d334-130">66</span></span>

<span data-ttu-id="9d334-131">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-131">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-132">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="9d334-132">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-133">67</span><span class="sxs-lookup"><span data-stu-id="9d334-133">67</span></span>

<span data-ttu-id="9d334-134">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="9d334-134">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-135">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-135">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-136">68</span><span class="sxs-lookup"><span data-stu-id="9d334-136">68</span></span>

<span data-ttu-id="9d334-137">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-137">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-138">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="9d334-138">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-139">69</span><span class="sxs-lookup"><span data-stu-id="9d334-139">69</span></span>

<span data-ttu-id="9d334-140">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9d334-140">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-141">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-141">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-142">70</span><span class="sxs-lookup"><span data-stu-id="9d334-142">70</span></span>

<span data-ttu-id="9d334-143">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-143">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-144">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-144">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-145">71</span><span class="sxs-lookup"><span data-stu-id="9d334-145">71</span></span>

<span data-ttu-id="9d334-146">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-146">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-147">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="9d334-147">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-148">72</span><span class="sxs-lookup"><span data-stu-id="9d334-148">72</span></span>

<span data-ttu-id="9d334-149">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="9d334-149">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-150">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-150">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-151">73</span><span class="sxs-lookup"><span data-stu-id="9d334-151">73</span></span>

<span data-ttu-id="9d334-152">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-152">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-153">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-153">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-154">74</span><span class="sxs-lookup"><span data-stu-id="9d334-154">74</span></span>

<span data-ttu-id="9d334-155">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-155">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-156">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="9d334-156">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-157">75</span><span class="sxs-lookup"><span data-stu-id="9d334-157">75</span></span>

<span data-ttu-id="9d334-158">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="9d334-158">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-159">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-159">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-160">76</span><span class="sxs-lookup"><span data-stu-id="9d334-160">76</span></span>

<span data-ttu-id="9d334-161">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-161">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-162">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-162">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-163">77</span><span class="sxs-lookup"><span data-stu-id="9d334-163">77</span></span>

<span data-ttu-id="9d334-164">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-164">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-165">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="9d334-165">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-166">78</span><span class="sxs-lookup"><span data-stu-id="9d334-166">78</span></span>

<span data-ttu-id="9d334-167">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="9d334-167">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-168">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-168">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-169">79</span><span class="sxs-lookup"><span data-stu-id="9d334-169">79</span></span>

<span data-ttu-id="9d334-170">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-170">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-171">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="9d334-171">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-172">80</span><span class="sxs-lookup"><span data-stu-id="9d334-172">80</span></span>

<span data-ttu-id="9d334-173">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9d334-173">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-174">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="9d334-174">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-175">81</span><span class="sxs-lookup"><span data-stu-id="9d334-175">81</span></span>

<span data-ttu-id="9d334-176">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="9d334-176">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-177">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="9d334-177">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-178">82</span><span class="sxs-lookup"><span data-stu-id="9d334-178">82</span></span>

<span data-ttu-id="9d334-179">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="9d334-179">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-180">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="9d334-180">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-181">83</span><span class="sxs-lookup"><span data-stu-id="9d334-181">83</span></span>

<span data-ttu-id="9d334-182">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="9d334-182">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-183">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="9d334-183">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-184">84</span><span class="sxs-lookup"><span data-stu-id="9d334-184">84</span></span>

<span data-ttu-id="9d334-185">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="9d334-185">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-186">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="9d334-186">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-187">85 %</span><span class="sxs-lookup"><span data-stu-id="9d334-187">85</span></span>

<span data-ttu-id="9d334-188">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="9d334-188">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-189">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="9d334-189">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-190">86</span><span class="sxs-lookup"><span data-stu-id="9d334-190">86</span></span>

<span data-ttu-id="9d334-191">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="9d334-191">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-192">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-192">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-193">87</span><span class="sxs-lookup"><span data-stu-id="9d334-193">87</span></span>

<span data-ttu-id="9d334-194">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-194">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-195">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="9d334-195">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-196">88</span><span class="sxs-lookup"><span data-stu-id="9d334-196">88</span></span>

<span data-ttu-id="9d334-197">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="9d334-197">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-198">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="9d334-198">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-199">89</span><span class="sxs-lookup"><span data-stu-id="9d334-199">89</span></span>

<span data-ttu-id="9d334-200">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="9d334-200">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-201">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="9d334-201">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-202">90</span><span class="sxs-lookup"><span data-stu-id="9d334-202">90</span></span>

<span data-ttu-id="9d334-203">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="9d334-203">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-204">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="9d334-204">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-205">91</span><span class="sxs-lookup"><span data-stu-id="9d334-205">91</span></span>

<span data-ttu-id="9d334-206">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="9d334-206">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-207">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="9d334-207">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-208">92</span><span class="sxs-lookup"><span data-stu-id="9d334-208">92</span></span>

<span data-ttu-id="9d334-209">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="9d334-209">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-210">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="9d334-210">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-211">93</span><span class="sxs-lookup"><span data-stu-id="9d334-211">93</span></span>

<span data-ttu-id="9d334-212">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="9d334-212">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-213">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="9d334-213">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-214">94</span><span class="sxs-lookup"><span data-stu-id="9d334-214">94</span></span>

<span data-ttu-id="9d334-215">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="9d334-215">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-216">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="9d334-216">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-217">95</span><span class="sxs-lookup"><span data-stu-id="9d334-217">95</span></span>

<span data-ttu-id="9d334-218">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="9d334-218">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-219">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="9d334-219">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-220">96</span><span class="sxs-lookup"><span data-stu-id="9d334-220">96</span></span>

<span data-ttu-id="9d334-221">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="9d334-221">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-222">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="9d334-222">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-223">97</span><span class="sxs-lookup"><span data-stu-id="9d334-223">97</span></span>

<span data-ttu-id="9d334-224">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="9d334-224">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-225">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="9d334-225">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-226">98</span><span class="sxs-lookup"><span data-stu-id="9d334-226">98</span></span>

<span data-ttu-id="9d334-227">Tous les baux DHCP ne sont pas libérés ni renouvelés.</span><span class="sxs-lookup"><span data-stu-id="9d334-227">Not all DHCP leases are released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-228">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="9d334-228">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-229">100</span><span class="sxs-lookup"><span data-stu-id="9d334-229">100</span></span>

<span data-ttu-id="9d334-230">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="9d334-230">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9d334-231">**Autres**</span><span class="sxs-lookup"><span data-stu-id="9d334-231">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9d334-232">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="9d334-232">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d334-233">Notes</span><span class="sxs-lookup"><span data-stu-id="9d334-233">Remarks</span></span>

<span data-ttu-id="9d334-234">Il s’agit d’un appel indépendant de l’instance qui s’applique à tous les adaptateurs, mais uniquement pour Windows.</span><span class="sxs-lookup"><span data-stu-id="9d334-234">This is an instance-independent call that applies to all adapters but only for Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="9d334-235">Exemples</span><span class="sxs-lookup"><span data-stu-id="9d334-235">Examples</span></span>

<span data-ttu-id="9d334-236">L’exemple de code [modifier l’ordre de recherche du suffixe DNS pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript permet de configurer un ordinateur pour qu’il utilise deux suffixes DNS lors des recherches DNS.</span><span class="sxs-lookup"><span data-stu-id="9d334-236">The [Modify the DNS Suffix Search Order for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript code sample configures a computer to use two DNS suffixes when performing DNS searches.</span></span>

<span data-ttu-id="9d334-237">L’exemple de script [activer des paramètres DHCP sur un ordinateur](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) permet de configurer tous les paramètres généralement requis pour activer DHCP sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9d334-237">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample configures all the settings typically required to enable DHCP on a computer.</span></span>

<span data-ttu-id="9d334-238">Le code PowerShell suivant définit l’ordre de recherche du suffixe DNS.</span><span class="sxs-lookup"><span data-stu-id="9d334-238">The following PowerShell code sets the DNS suffix search order.</span></span>


```PowerShell
#First store the suffixes to set in a variable
$suffixes = 'microsoft.com', 'google.com', 'yahoo.com'

#Since this is a static method, get a class object and then call the method. 
$class = [wmiclass]'Win32_NetworkAdapterConfiguration'
$class.SetDNSSuffixSearchOrder($suffixes)
```



## <a name="requirements"></a><span data-ttu-id="9d334-239">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d334-239">Requirements</span></span>



| <span data-ttu-id="9d334-240">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d334-240">Requirement</span></span> | <span data-ttu-id="9d334-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d334-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d334-242">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d334-242">Minimum supported client</span></span><br/> | <span data-ttu-id="9d334-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d334-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d334-244">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d334-244">Minimum supported server</span></span><br/> | <span data-ttu-id="9d334-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d334-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d334-246">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9d334-246">Namespace</span></span><br/>                | <span data-ttu-id="9d334-247">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9d334-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9d334-248">MOF</span><span class="sxs-lookup"><span data-stu-id="9d334-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d334-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d334-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d334-250">DLL</span><span class="sxs-lookup"><span data-stu-id="9d334-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d334-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d334-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d334-252">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d334-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d334-253">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="9d334-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9d334-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="9d334-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="9d334-255">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="9d334-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="9d334-256">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="9d334-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="9d334-257">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="9d334-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

