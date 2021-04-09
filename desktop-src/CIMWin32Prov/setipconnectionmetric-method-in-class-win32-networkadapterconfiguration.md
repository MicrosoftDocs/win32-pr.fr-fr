---
description: La méthode SetIPConnectionMetric est utilisée pour définir la métrique de routage associée à cette carte IP liée.
ms.assetid: d7f7c0df-51e3-4dc8-8a53-977ecde075df
ms.tgt_platform: multiple
title: Méthode SetIPConnectionMetric de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPConnectionMetric
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73d6dde0a8faea2aeaf0982459e3c377bb1ac51d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110950"
---
# <a name="setipconnectionmetric-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="81fd4-103">Méthode SetIPConnectionMetric de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="81fd4-103">SetIPConnectionMetric method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="81fd4-104">La méthode **SetIPConnectionMetric** est utilisée pour définir la métrique de routage associée à cette carte IP liée.</span><span class="sxs-lookup"><span data-stu-id="81fd4-104">The **SetIPConnectionMetric** method is used to set the routing metric associated with this IP-bound adapter.</span></span>

<span data-ttu-id="81fd4-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="81fd4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="81fd4-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="81fd4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="81fd4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81fd4-107">Syntax</span></span>


```mof
uint32 SetIPConnectionMetric(
  [in] uint32 IPConnectionMetric
);
```



## <a name="parameters"></a><span data-ttu-id="81fd4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81fd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81fd4-109">*IPConnectionMetric* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81fd4-109">*IPConnectionMetric* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-110">Indique le coût d’utilisation des itinéraires configurés pour cette carte IP liée.</span><span class="sxs-lookup"><span data-stu-id="81fd4-110">Indicates the cost of using the configured routes for this IP-bound adapter.</span></span> <span data-ttu-id="81fd4-111">La valeur est pondérée pour ces itinéraires dans la table de routage IP.</span><span class="sxs-lookup"><span data-stu-id="81fd4-111">The value is weighted for those routes in the IP routing table.</span></span> <span data-ttu-id="81fd4-112">S’il existe plusieurs itinéraires vers une destination dans la table de routage, l’itinéraire avec la métrique la plus basse est utilisé.</span><span class="sxs-lookup"><span data-stu-id="81fd4-112">If there are multiple routes to a destination in the routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="81fd4-113">La plage de valeurs valides est comprise entre 1 et 9999.</span><span class="sxs-lookup"><span data-stu-id="81fd4-113">The range of valid values is 1 through 9999.</span></span> <span data-ttu-id="81fd4-114">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="81fd4-114">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81fd4-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81fd4-115">Return value</span></span>

<span data-ttu-id="81fd4-116">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="81fd4-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="81fd4-117">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="81fd4-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="81fd4-118">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="81fd4-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="81fd4-119">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="81fd4-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-120">0</span><span class="sxs-lookup"><span data-stu-id="81fd4-120">0</span></span>

<span data-ttu-id="81fd4-121">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="81fd4-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-122">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="81fd4-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-123">1</span><span class="sxs-lookup"><span data-stu-id="81fd4-123">1</span></span>

<span data-ttu-id="81fd4-124">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="81fd4-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-125">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="81fd4-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-126">64</span><span class="sxs-lookup"><span data-stu-id="81fd4-126">64</span></span>

<span data-ttu-id="81fd4-127">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="81fd4-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-128">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="81fd4-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-129">65</span><span class="sxs-lookup"><span data-stu-id="81fd4-129">65</span></span>

<span data-ttu-id="81fd4-130">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="81fd4-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-131">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-132">66</span><span class="sxs-lookup"><span data-stu-id="81fd4-132">66</span></span>

<span data-ttu-id="81fd4-133">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-134">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="81fd4-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-135">67</span><span class="sxs-lookup"><span data-stu-id="81fd4-135">67</span></span>

<span data-ttu-id="81fd4-136">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="81fd4-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-137">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-138">68</span><span class="sxs-lookup"><span data-stu-id="81fd4-138">68</span></span>

<span data-ttu-id="81fd4-139">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-140">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="81fd4-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-141">69</span><span class="sxs-lookup"><span data-stu-id="81fd4-141">69</span></span>

<span data-ttu-id="81fd4-142">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="81fd4-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-143">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-144">70</span><span class="sxs-lookup"><span data-stu-id="81fd4-144">70</span></span>

<span data-ttu-id="81fd4-145">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-146">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-147">71</span><span class="sxs-lookup"><span data-stu-id="81fd4-147">71</span></span>

<span data-ttu-id="81fd4-148">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-149">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="81fd4-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-150">72</span><span class="sxs-lookup"><span data-stu-id="81fd4-150">72</span></span>

<span data-ttu-id="81fd4-151">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="81fd4-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-152">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-153">73</span><span class="sxs-lookup"><span data-stu-id="81fd4-153">73</span></span>

<span data-ttu-id="81fd4-154">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-155">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-156">74</span><span class="sxs-lookup"><span data-stu-id="81fd4-156">74</span></span>

<span data-ttu-id="81fd4-157">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-158">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="81fd4-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-159">75</span><span class="sxs-lookup"><span data-stu-id="81fd4-159">75</span></span>

<span data-ttu-id="81fd4-160">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="81fd4-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-161">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-162">76</span><span class="sxs-lookup"><span data-stu-id="81fd4-162">76</span></span>

<span data-ttu-id="81fd4-163">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-164">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-165">77</span><span class="sxs-lookup"><span data-stu-id="81fd4-165">77</span></span>

<span data-ttu-id="81fd4-166">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-167">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="81fd4-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-168">78</span><span class="sxs-lookup"><span data-stu-id="81fd4-168">78</span></span>

<span data-ttu-id="81fd4-169">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="81fd4-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-170">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-171">79</span><span class="sxs-lookup"><span data-stu-id="81fd4-171">79</span></span>

<span data-ttu-id="81fd4-172">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-173">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="81fd4-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-174">80</span><span class="sxs-lookup"><span data-stu-id="81fd4-174">80</span></span>

<span data-ttu-id="81fd4-175">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="81fd4-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-176">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="81fd4-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-177">81</span><span class="sxs-lookup"><span data-stu-id="81fd4-177">81</span></span>

<span data-ttu-id="81fd4-178">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="81fd4-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-179">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="81fd4-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-180">82</span><span class="sxs-lookup"><span data-stu-id="81fd4-180">82</span></span>

<span data-ttu-id="81fd4-181">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="81fd4-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-182">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="81fd4-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-183">83</span><span class="sxs-lookup"><span data-stu-id="81fd4-183">83</span></span>

<span data-ttu-id="81fd4-184">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="81fd4-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-185">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="81fd4-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-186">84</span><span class="sxs-lookup"><span data-stu-id="81fd4-186">84</span></span>

<span data-ttu-id="81fd4-187">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="81fd4-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-188">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="81fd4-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-189">85 %</span><span class="sxs-lookup"><span data-stu-id="81fd4-189">85</span></span>

<span data-ttu-id="81fd4-190">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="81fd4-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-191">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="81fd4-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-192">86</span><span class="sxs-lookup"><span data-stu-id="81fd4-192">86</span></span>

<span data-ttu-id="81fd4-193">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="81fd4-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-194">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-195">87</span><span class="sxs-lookup"><span data-stu-id="81fd4-195">87</span></span>

<span data-ttu-id="81fd4-196">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-197">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="81fd4-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-198">88</span><span class="sxs-lookup"><span data-stu-id="81fd4-198">88</span></span>

<span data-ttu-id="81fd4-199">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="81fd4-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-200">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="81fd4-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-201">89</span><span class="sxs-lookup"><span data-stu-id="81fd4-201">89</span></span>

<span data-ttu-id="81fd4-202">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="81fd4-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-203">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="81fd4-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-204">90</span><span class="sxs-lookup"><span data-stu-id="81fd4-204">90</span></span>

<span data-ttu-id="81fd4-205">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="81fd4-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-206">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="81fd4-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-207">91</span><span class="sxs-lookup"><span data-stu-id="81fd4-207">91</span></span>

<span data-ttu-id="81fd4-208">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="81fd4-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-209">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="81fd4-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-210">92</span><span class="sxs-lookup"><span data-stu-id="81fd4-210">92</span></span>

<span data-ttu-id="81fd4-211">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="81fd4-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-212">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="81fd4-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-213">93</span><span class="sxs-lookup"><span data-stu-id="81fd4-213">93</span></span>

<span data-ttu-id="81fd4-214">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="81fd4-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-215">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="81fd4-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-216">94</span><span class="sxs-lookup"><span data-stu-id="81fd4-216">94</span></span>

<span data-ttu-id="81fd4-217">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="81fd4-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-218">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="81fd4-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-219">95</span><span class="sxs-lookup"><span data-stu-id="81fd4-219">95</span></span>

<span data-ttu-id="81fd4-220">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="81fd4-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-221">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="81fd4-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-222">96</span><span class="sxs-lookup"><span data-stu-id="81fd4-222">96</span></span>

<span data-ttu-id="81fd4-223">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="81fd4-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-224">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="81fd4-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-225">97</span><span class="sxs-lookup"><span data-stu-id="81fd4-225">97</span></span>

<span data-ttu-id="81fd4-226">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="81fd4-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-227">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="81fd4-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-228">98</span><span class="sxs-lookup"><span data-stu-id="81fd4-228">98</span></span>

<span data-ttu-id="81fd4-229">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="81fd4-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-230">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="81fd4-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-231">100</span><span class="sxs-lookup"><span data-stu-id="81fd4-231">100</span></span>

<span data-ttu-id="81fd4-232">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="81fd4-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="81fd4-233">**Autres**</span><span class="sxs-lookup"><span data-stu-id="81fd4-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="81fd4-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="81fd4-234">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="81fd4-235">Exemples</span><span class="sxs-lookup"><span data-stu-id="81fd4-235">Examples</span></span>

<span data-ttu-id="81fd4-236">L’exemple de [modification de la métrique de la connexion IP pour une carte réseau](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) définit la mesure de la connexion IP pour une carte réseau sur 100.</span><span class="sxs-lookup"><span data-stu-id="81fd4-236">The [Modify the IP Connection Metric for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript sample sets the IP connection metric for a network adapter to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="81fd4-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81fd4-237">Requirements</span></span>



| <span data-ttu-id="81fd4-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81fd4-238">Requirement</span></span> | <span data-ttu-id="81fd4-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="81fd4-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81fd4-240">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81fd4-240">Minimum supported client</span></span><br/> | <span data-ttu-id="81fd4-241">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81fd4-241">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="81fd4-242">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81fd4-242">Minimum supported server</span></span><br/> | <span data-ttu-id="81fd4-243">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81fd4-243">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="81fd4-244">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="81fd4-244">Namespace</span></span><br/>                | <span data-ttu-id="81fd4-245">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="81fd4-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81fd4-246">MOF</span><span class="sxs-lookup"><span data-stu-id="81fd4-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81fd4-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81fd4-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81fd4-248">DLL</span><span class="sxs-lookup"><span data-stu-id="81fd4-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81fd4-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81fd4-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81fd4-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81fd4-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81fd4-251">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="81fd4-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="81fd4-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="81fd4-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="81fd4-253">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="81fd4-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="81fd4-254">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="81fd4-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="81fd4-255">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="81fd4-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

