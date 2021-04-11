---
description: La méthode statique de la classe WMI SetArpAlwaysSourceRoute est utilisée pour définir la transmission des requêtes ARP par TCP/IP.
ms.assetid: bbff4e2e-aea6-400e-8bd8-f62aaa9fa601
ms.tgt_platform: multiple
title: Méthode SetArpAlwaysSourceRoute de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpAlwaysSourceRoute
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7151fbbd13d3ac6fdf4ac3b129cdcb438abe73a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110358"
---
# <a name="setarpalwayssourceroute-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="0ea96-103">Méthode SetArpAlwaysSourceRoute de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ea96-103">SetArpAlwaysSourceRoute method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="0ea96-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetArpAlwaysSourceRoute** est utilisée pour définir la transmission des requêtes ARP par TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0ea96-104">The **SetArpAlwaysSourceRoute** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the transmission of ARP queries by TCP/IP.</span></span>

<span data-ttu-id="0ea96-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0ea96-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0ea96-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0ea96-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea96-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ea96-107">Syntax</span></span>


```mof
uint32 SetArpAlwaysSourceRoute(
  [in] boolean ArpAlwaysSourceRoute
);
```



## <a name="parameters"></a><span data-ttu-id="0ea96-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ea96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea96-109">*ArpAlwaysSourceRoute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ea96-109">*ArpAlwaysSourceRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-110">Si la **valeur est true**, TCP/IP est contraint de transmettre des requêtes ARP avec le routage source activé sur les réseaux Token Ring.</span><span class="sxs-lookup"><span data-stu-id="0ea96-110">If **true**, TCP/IP is forced to transmit ARP queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="0ea96-111">Par défaut, la pile transmet d’abord les requêtes ARP sans routage source, puis effectue une nouvelle tentative avec le routage source activé si aucune réponse n’est reçue.</span><span class="sxs-lookup"><span data-stu-id="0ea96-111">By default, the stack transmits ARP queries without source routing first, then retries with source routing enabled if no reply is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ea96-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ea96-112">Return value</span></span>

<span data-ttu-id="0ea96-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0ea96-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="0ea96-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0ea96-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0ea96-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0ea96-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0ea96-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="0ea96-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-117">0</span><span class="sxs-lookup"><span data-stu-id="0ea96-117">0</span></span>

<span data-ttu-id="0ea96-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0ea96-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="0ea96-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-120">1</span><span class="sxs-lookup"><span data-stu-id="0ea96-120">1</span></span>

<span data-ttu-id="0ea96-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="0ea96-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="0ea96-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-123">64</span><span class="sxs-lookup"><span data-stu-id="0ea96-123">64</span></span>

<span data-ttu-id="0ea96-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="0ea96-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="0ea96-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-126">65</span><span class="sxs-lookup"><span data-stu-id="0ea96-126">65</span></span>

<span data-ttu-id="0ea96-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="0ea96-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-129">66</span><span class="sxs-lookup"><span data-stu-id="0ea96-129">66</span></span>

<span data-ttu-id="0ea96-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="0ea96-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-132">67</span><span class="sxs-lookup"><span data-stu-id="0ea96-132">67</span></span>

<span data-ttu-id="0ea96-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="0ea96-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-135">68</span><span class="sxs-lookup"><span data-stu-id="0ea96-135">68</span></span>

<span data-ttu-id="0ea96-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="0ea96-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-138">69</span><span class="sxs-lookup"><span data-stu-id="0ea96-138">69</span></span>

<span data-ttu-id="0ea96-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0ea96-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-141">70</span><span class="sxs-lookup"><span data-stu-id="0ea96-141">70</span></span>

<span data-ttu-id="0ea96-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-144">71</span><span class="sxs-lookup"><span data-stu-id="0ea96-144">71</span></span>

<span data-ttu-id="0ea96-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="0ea96-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-147">72</span><span class="sxs-lookup"><span data-stu-id="0ea96-147">72</span></span>

<span data-ttu-id="0ea96-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="0ea96-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-150">73</span><span class="sxs-lookup"><span data-stu-id="0ea96-150">73</span></span>

<span data-ttu-id="0ea96-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-153">74</span><span class="sxs-lookup"><span data-stu-id="0ea96-153">74</span></span>

<span data-ttu-id="0ea96-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="0ea96-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-156">75</span><span class="sxs-lookup"><span data-stu-id="0ea96-156">75</span></span>

<span data-ttu-id="0ea96-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="0ea96-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-159">76</span><span class="sxs-lookup"><span data-stu-id="0ea96-159">76</span></span>

<span data-ttu-id="0ea96-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-162">77</span><span class="sxs-lookup"><span data-stu-id="0ea96-162">77</span></span>

<span data-ttu-id="0ea96-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="0ea96-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-165">78</span><span class="sxs-lookup"><span data-stu-id="0ea96-165">78</span></span>

<span data-ttu-id="0ea96-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="0ea96-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-168">79</span><span class="sxs-lookup"><span data-stu-id="0ea96-168">79</span></span>

<span data-ttu-id="0ea96-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="0ea96-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-171">80</span><span class="sxs-lookup"><span data-stu-id="0ea96-171">80</span></span>

<span data-ttu-id="0ea96-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0ea96-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="0ea96-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-174">81</span><span class="sxs-lookup"><span data-stu-id="0ea96-174">81</span></span>

<span data-ttu-id="0ea96-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="0ea96-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="0ea96-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-177">82</span><span class="sxs-lookup"><span data-stu-id="0ea96-177">82</span></span>

<span data-ttu-id="0ea96-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="0ea96-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="0ea96-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-180">83</span><span class="sxs-lookup"><span data-stu-id="0ea96-180">83</span></span>

<span data-ttu-id="0ea96-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="0ea96-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="0ea96-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-183">84</span><span class="sxs-lookup"><span data-stu-id="0ea96-183">84</span></span>

<span data-ttu-id="0ea96-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="0ea96-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="0ea96-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-186">85 %</span><span class="sxs-lookup"><span data-stu-id="0ea96-186">85</span></span>

<span data-ttu-id="0ea96-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="0ea96-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="0ea96-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-189">86</span><span class="sxs-lookup"><span data-stu-id="0ea96-189">86</span></span>

<span data-ttu-id="0ea96-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="0ea96-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-192">87</span><span class="sxs-lookup"><span data-stu-id="0ea96-192">87</span></span>

<span data-ttu-id="0ea96-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="0ea96-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-195">88</span><span class="sxs-lookup"><span data-stu-id="0ea96-195">88</span></span>

<span data-ttu-id="0ea96-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="0ea96-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="0ea96-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-198">89</span><span class="sxs-lookup"><span data-stu-id="0ea96-198">89</span></span>

<span data-ttu-id="0ea96-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="0ea96-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="0ea96-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-201">90</span><span class="sxs-lookup"><span data-stu-id="0ea96-201">90</span></span>

<span data-ttu-id="0ea96-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="0ea96-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="0ea96-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-204">91</span><span class="sxs-lookup"><span data-stu-id="0ea96-204">91</span></span>

<span data-ttu-id="0ea96-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0ea96-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="0ea96-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-207">92</span><span class="sxs-lookup"><span data-stu-id="0ea96-207">92</span></span>

<span data-ttu-id="0ea96-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="0ea96-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="0ea96-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-210">93</span><span class="sxs-lookup"><span data-stu-id="0ea96-210">93</span></span>

<span data-ttu-id="0ea96-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0ea96-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="0ea96-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-213">94</span><span class="sxs-lookup"><span data-stu-id="0ea96-213">94</span></span>

<span data-ttu-id="0ea96-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="0ea96-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="0ea96-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-216">95</span><span class="sxs-lookup"><span data-stu-id="0ea96-216">95</span></span>

<span data-ttu-id="0ea96-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="0ea96-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="0ea96-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-219">96</span><span class="sxs-lookup"><span data-stu-id="0ea96-219">96</span></span>

<span data-ttu-id="0ea96-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="0ea96-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="0ea96-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-222">97</span><span class="sxs-lookup"><span data-stu-id="0ea96-222">97</span></span>

<span data-ttu-id="0ea96-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="0ea96-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="0ea96-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-225">98</span><span class="sxs-lookup"><span data-stu-id="0ea96-225">98</span></span>

<span data-ttu-id="0ea96-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="0ea96-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="0ea96-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-228">100</span><span class="sxs-lookup"><span data-stu-id="0ea96-228">100</span></span>

<span data-ttu-id="0ea96-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="0ea96-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0ea96-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="0ea96-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="0ea96-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="0ea96-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0ea96-232">Exemples</span><span class="sxs-lookup"><span data-stu-id="0ea96-232">Examples</span></span>

<span data-ttu-id="0ea96-233">L’exemple [modifier les requêtes ARP pour utiliser le code source de routage](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) dans la Galerie TechNet utilise **SETARPALWAYSSOURCEROUTE** pour configurer TCP/IP pour toujours utiliser le routage source sur tous les réseaux Token Ring.</span><span class="sxs-lookup"><span data-stu-id="0ea96-233">The [Modify ARP Queries to Use Source Routing](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) VBScript sample on TechNet Gallery uses **SetArpAlwaysSourceRoute** to configure TCP/IP to always use source routing on all Token Ring networks.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea96-234">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ea96-234">Requirements</span></span>



| <span data-ttu-id="0ea96-235">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ea96-235">Requirement</span></span> | <span data-ttu-id="0ea96-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ea96-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea96-237">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ea96-237">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea96-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ea96-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0ea96-239">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ea96-239">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea96-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ea96-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ea96-241">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0ea96-241">Namespace</span></span><br/>                | <span data-ttu-id="0ea96-242">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0ea96-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0ea96-243">MOF</span><span class="sxs-lookup"><span data-stu-id="0ea96-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ea96-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ea96-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ea96-245">DLL</span><span class="sxs-lookup"><span data-stu-id="0ea96-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ea96-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ea96-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea96-247">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ea96-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea96-248">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="0ea96-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0ea96-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="0ea96-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="0ea96-250">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="0ea96-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="0ea96-251">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="0ea96-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="0ea96-252">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="0ea96-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

