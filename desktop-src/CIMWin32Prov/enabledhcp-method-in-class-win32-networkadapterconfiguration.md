---
description: La méthode de classe WMI EnableDHCP active le protocole DHCP (Dynamic Host Configuration Protocol) pour le service avec cette carte réseau. DHCP permet d’allouer dynamiquement des adresses IP.
ms.assetid: 8c61d731-77a3-4ef4-bad9-26edaca60892
ms.tgt_platform: multiple
title: Méthode EnableDHCP de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDHCP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 002dedd3b0165053fea98dda035316676af638f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950562"
---
# <a name="enabledhcp-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="b556f-104">Méthode EnableDHCP de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="b556f-104">EnableDHCP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="b556f-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableDHCP** active le protocole DHCP (Dynamic Host Configuration Protocol) pour le service avec cette carte réseau.</span><span class="sxs-lookup"><span data-stu-id="b556f-105">The **EnableDHCP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span> <span data-ttu-id="b556f-106">DHCP permet d’allouer dynamiquement des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="b556f-106">DHCP allows IP addresses to be dynamically allocated.</span></span>

<span data-ttu-id="b556f-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b556f-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b556f-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b556f-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b556f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b556f-109">Syntax</span></span>


```mof
uint32 EnableDHCP();
```



## <a name="parameters"></a><span data-ttu-id="b556f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b556f-110">Parameters</span></span>

<span data-ttu-id="b556f-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b556f-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b556f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b556f-112">Return value</span></span>

<span data-ttu-id="b556f-113">Retourne la valeur 0 (zéro) pour une exécution réussie lorsqu’un redémarrage n’est pas nécessaire, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et tout autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b556f-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="b556f-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b556f-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b556f-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b556f-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b556f-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="b556f-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-117">0</span><span class="sxs-lookup"><span data-stu-id="b556f-117">0</span></span>

<span data-ttu-id="b556f-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b556f-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="b556f-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-120">1</span><span class="sxs-lookup"><span data-stu-id="b556f-120">1</span></span>

<span data-ttu-id="b556f-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="b556f-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="b556f-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-123">64</span><span class="sxs-lookup"><span data-stu-id="b556f-123">64</span></span>

<span data-ttu-id="b556f-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="b556f-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="b556f-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-126">65</span><span class="sxs-lookup"><span data-stu-id="b556f-126">65</span></span>

<span data-ttu-id="b556f-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="b556f-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-129">66</span><span class="sxs-lookup"><span data-stu-id="b556f-129">66</span></span>

<span data-ttu-id="b556f-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="b556f-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-132">67</span><span class="sxs-lookup"><span data-stu-id="b556f-132">67</span></span>

<span data-ttu-id="b556f-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="b556f-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-135">68</span><span class="sxs-lookup"><span data-stu-id="b556f-135">68</span></span>

<span data-ttu-id="b556f-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="b556f-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-138">69</span><span class="sxs-lookup"><span data-stu-id="b556f-138">69</span></span>

<span data-ttu-id="b556f-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b556f-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-141">70</span><span class="sxs-lookup"><span data-stu-id="b556f-141">70</span></span>

<span data-ttu-id="b556f-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-144">71</span><span class="sxs-lookup"><span data-stu-id="b556f-144">71</span></span>

<span data-ttu-id="b556f-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="b556f-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-147">72</span><span class="sxs-lookup"><span data-stu-id="b556f-147">72</span></span>

<span data-ttu-id="b556f-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="b556f-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-150">73</span><span class="sxs-lookup"><span data-stu-id="b556f-150">73</span></span>

<span data-ttu-id="b556f-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-153">74</span><span class="sxs-lookup"><span data-stu-id="b556f-153">74</span></span>

<span data-ttu-id="b556f-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="b556f-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-156">75</span><span class="sxs-lookup"><span data-stu-id="b556f-156">75</span></span>

<span data-ttu-id="b556f-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="b556f-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-159">76</span><span class="sxs-lookup"><span data-stu-id="b556f-159">76</span></span>

<span data-ttu-id="b556f-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-162">77</span><span class="sxs-lookup"><span data-stu-id="b556f-162">77</span></span>

<span data-ttu-id="b556f-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="b556f-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-165">78</span><span class="sxs-lookup"><span data-stu-id="b556f-165">78</span></span>

<span data-ttu-id="b556f-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="b556f-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-168">79</span><span class="sxs-lookup"><span data-stu-id="b556f-168">79</span></span>

<span data-ttu-id="b556f-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="b556f-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-171">80</span><span class="sxs-lookup"><span data-stu-id="b556f-171">80</span></span>

<span data-ttu-id="b556f-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b556f-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="b556f-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-174">81</span><span class="sxs-lookup"><span data-stu-id="b556f-174">81</span></span>

<span data-ttu-id="b556f-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="b556f-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="b556f-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-177">82</span><span class="sxs-lookup"><span data-stu-id="b556f-177">82</span></span>

<span data-ttu-id="b556f-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="b556f-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="b556f-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-180">83</span><span class="sxs-lookup"><span data-stu-id="b556f-180">83</span></span>

<span data-ttu-id="b556f-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="b556f-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="b556f-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-183">84</span><span class="sxs-lookup"><span data-stu-id="b556f-183">84</span></span>

<span data-ttu-id="b556f-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="b556f-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="b556f-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-186">85 %</span><span class="sxs-lookup"><span data-stu-id="b556f-186">85</span></span>

<span data-ttu-id="b556f-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="b556f-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="b556f-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-189">86</span><span class="sxs-lookup"><span data-stu-id="b556f-189">86</span></span>

<span data-ttu-id="b556f-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="b556f-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-192">87</span><span class="sxs-lookup"><span data-stu-id="b556f-192">87</span></span>

<span data-ttu-id="b556f-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="b556f-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-195">88</span><span class="sxs-lookup"><span data-stu-id="b556f-195">88</span></span>

<span data-ttu-id="b556f-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="b556f-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="b556f-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-198">89</span><span class="sxs-lookup"><span data-stu-id="b556f-198">89</span></span>

<span data-ttu-id="b556f-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="b556f-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="b556f-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-201">90</span><span class="sxs-lookup"><span data-stu-id="b556f-201">90</span></span>

<span data-ttu-id="b556f-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="b556f-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="b556f-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-204">91</span><span class="sxs-lookup"><span data-stu-id="b556f-204">91</span></span>

<span data-ttu-id="b556f-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="b556f-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="b556f-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-207">92</span><span class="sxs-lookup"><span data-stu-id="b556f-207">92</span></span>

<span data-ttu-id="b556f-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="b556f-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="b556f-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-210">93</span><span class="sxs-lookup"><span data-stu-id="b556f-210">93</span></span>

<span data-ttu-id="b556f-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="b556f-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="b556f-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-213">94</span><span class="sxs-lookup"><span data-stu-id="b556f-213">94</span></span>

<span data-ttu-id="b556f-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="b556f-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="b556f-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-216">95</span><span class="sxs-lookup"><span data-stu-id="b556f-216">95</span></span>

<span data-ttu-id="b556f-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="b556f-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="b556f-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-219">96</span><span class="sxs-lookup"><span data-stu-id="b556f-219">96</span></span>

<span data-ttu-id="b556f-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="b556f-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="b556f-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-222">97</span><span class="sxs-lookup"><span data-stu-id="b556f-222">97</span></span>

<span data-ttu-id="b556f-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="b556f-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="b556f-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-225">98</span><span class="sxs-lookup"><span data-stu-id="b556f-225">98</span></span>

<span data-ttu-id="b556f-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="b556f-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="b556f-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-228">100</span><span class="sxs-lookup"><span data-stu-id="b556f-228">100</span></span>

<span data-ttu-id="b556f-229">DHCP n’est pas activé sur la carte.</span><span class="sxs-lookup"><span data-stu-id="b556f-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b556f-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="b556f-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="b556f-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="b556f-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b556f-232">Notes</span><span class="sxs-lookup"><span data-stu-id="b556f-232">Remarks</span></span>

<span data-ttu-id="b556f-233">Cette méthode n’efface pas les passerelles par défaut statiques présentes sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b556f-233">This method does not clears any static default gateways present on the machine.</span></span>

## <a name="examples"></a><span data-ttu-id="b556f-234">Exemples</span><span class="sxs-lookup"><span data-stu-id="b556f-234">Examples</span></span>

<span data-ttu-id="b556f-235">L’exemple de code [activer DHCP et affecter des serveurs DNS](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript dans la Galerie TechNet utilise EnableDHCP pour activer DHCP et affecter des serveurs DNS à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b556f-235">The [Enable DHCP and Assign DNS Servers](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript code sample on TechNet Gallery uses EnableDHCP to enable DHCP and assign DNS servers to a computer.</span></span>

<span data-ttu-id="b556f-236">L’exemple de code VBScript suivant montre comment activer l’utilisation du protocole DHCP sur une instance de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="b556f-236">The following VBScript code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="b556f-237">Dans ce cas, nous spécifions l’adaptateur avec un index égal à 0.</span><span class="sxs-lookup"><span data-stu-id="b556f-237">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="b556f-238">L’index approprié doit être sélectionné à partir des instances de la carte réseau Win32 \_ pour d’autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="b556f-238">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="b556f-239">Pris en charge sur les plateformes NT uniquement.</span><span class="sxs-lookup"><span data-stu-id="b556f-239">Supported on NT platforms only.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=0")

RetVal = Adapter.EnableDHCP()

if RetVal = 0 then 
 WScript.Echo "DHCP Enabled"
else 
 WScript.Echo "DHCP enable failed"
end if
```



<span data-ttu-id="b556f-240">L’exemple de code perl suivant montre comment activer l’utilisation du protocole DHCP sur une instance de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="b556f-240">The following Perl code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="b556f-241">Dans ce cas, nous spécifions l’adaptateur avec un index égal à 0.</span><span class="sxs-lookup"><span data-stu-id="b556f-241">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="b556f-242">L’index approprié doit être sélectionné à partir des instances de la carte réseau Win32 \_ pour d’autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="b556f-242">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="b556f-243">Pris en charge sur les plateformes NT uniquement.</span><span class="sxs-lookup"><span data-stu-id="b556f-243">Supported on NT platforms only.</span></span>

 


```
use strict;
use Win32::OLE;

my ( $Adapter, $RetVal );

eval { $Adapter = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
       Get("Win32_NetworkAdapterConfiguration=0"); };
unless ($@)
{
 print "\n";
 $RetVal = $Adapter->EnableDHCP();
 if ( $RetVal == 0)
 {
  print "DHCP Enabled\n";
 }
 else
 {
  print "DHCP enable failed\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="b556f-244">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b556f-244">Requirements</span></span>



| <span data-ttu-id="b556f-245">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b556f-245">Requirement</span></span> | <span data-ttu-id="b556f-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="b556f-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b556f-247">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b556f-247">Minimum supported client</span></span><br/> | <span data-ttu-id="b556f-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b556f-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b556f-249">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b556f-249">Minimum supported server</span></span><br/> | <span data-ttu-id="b556f-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b556f-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b556f-251">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b556f-251">Namespace</span></span><br/>                | <span data-ttu-id="b556f-252">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b556f-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b556f-253">MOF</span><span class="sxs-lookup"><span data-stu-id="b556f-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b556f-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b556f-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b556f-255">DLL</span><span class="sxs-lookup"><span data-stu-id="b556f-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b556f-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b556f-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b556f-257">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b556f-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b556f-258">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="b556f-258">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b556f-259">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="b556f-259">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="b556f-260">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="b556f-260">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="b556f-261">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="b556f-261">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="b556f-262">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="b556f-262">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

