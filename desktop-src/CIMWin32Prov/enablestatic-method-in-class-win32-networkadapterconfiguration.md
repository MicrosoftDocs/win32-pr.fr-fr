---
description: La méthode de classe WMI EnableStatic active l’adressage TCP/IP statique pour la carte réseau cible. Par conséquent, DHCP pour cette carte réseau est désactivé.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Méthode EnableStatic de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748141"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="87600-104">Méthode EnableStatic de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="87600-104">EnableStatic method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="87600-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableStatic** active l’adressage TCP/IP statique pour la carte réseau cible.</span><span class="sxs-lookup"><span data-stu-id="87600-105">The **EnableStatic** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables static TCP/IP addressing for the target network adapter.</span></span> <span data-ttu-id="87600-106">Par conséquent, DHCP pour cette carte réseau est désactivé.</span><span class="sxs-lookup"><span data-stu-id="87600-106">As a result, DHCP for this network adapter is disabled.</span></span>

<span data-ttu-id="87600-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="87600-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="87600-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="87600-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="87600-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87600-109">Syntax</span></span>


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a><span data-ttu-id="87600-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87600-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87600-111">*Adresse IP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87600-111">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87600-112">Répertorie toutes les adresses IP statiques pour la carte réseau actuelle.</span><span class="sxs-lookup"><span data-stu-id="87600-112">Lists all of the static IP addresses for the current network adapter.</span></span>

<span data-ttu-id="87600-113">Exemple : 155.34.22.0.</span><span class="sxs-lookup"><span data-stu-id="87600-113">Example: 155.34.22.0.</span></span>

</dd> <dt>

<span data-ttu-id="87600-114">*Masque_Sous_réseau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87600-114">*SubnetMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87600-115">Les masques de sous-réseau qui complètent les valeurs dans le paramètre *IPAddress* .</span><span class="sxs-lookup"><span data-stu-id="87600-115">Subnet masks that complement the values in the *IPAddress* parameter.</span></span>

<span data-ttu-id="87600-116">Exemple : 255.255.0.0.</span><span class="sxs-lookup"><span data-stu-id="87600-116">Example: 255.255.0.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87600-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87600-117">Return value</span></span>

<span data-ttu-id="87600-118">Retourne la valeur 0 (zéro) pour une exécution réussie lorsqu’un redémarrage n’est pas nécessaire, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et tout autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="87600-118">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="87600-119">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="87600-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="87600-120">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="87600-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="87600-121">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="87600-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="87600-122">0</span><span class="sxs-lookup"><span data-stu-id="87600-122">0</span></span>

<span data-ttu-id="87600-123">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="87600-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="87600-124">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="87600-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="87600-125">1</span><span class="sxs-lookup"><span data-stu-id="87600-125">1</span></span>

<span data-ttu-id="87600-126">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="87600-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="87600-127">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="87600-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="87600-128">64</span><span class="sxs-lookup"><span data-stu-id="87600-128">64</span></span>

<span data-ttu-id="87600-129">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="87600-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="87600-130">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="87600-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="87600-131">65</span><span class="sxs-lookup"><span data-stu-id="87600-131">65</span></span>

<span data-ttu-id="87600-132">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="87600-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="87600-133">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="87600-134">66</span><span class="sxs-lookup"><span data-stu-id="87600-134">66</span></span>

<span data-ttu-id="87600-135">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="87600-136">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="87600-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="87600-137">67</span><span class="sxs-lookup"><span data-stu-id="87600-137">67</span></span>

<span data-ttu-id="87600-138">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="87600-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="87600-139">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="87600-140">68</span><span class="sxs-lookup"><span data-stu-id="87600-140">68</span></span>

<span data-ttu-id="87600-141">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="87600-142">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="87600-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="87600-143">69</span><span class="sxs-lookup"><span data-stu-id="87600-143">69</span></span>

<span data-ttu-id="87600-144">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="87600-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="87600-145">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="87600-146">70</span><span class="sxs-lookup"><span data-stu-id="87600-146">70</span></span>

<span data-ttu-id="87600-147">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="87600-148">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="87600-149">71</span><span class="sxs-lookup"><span data-stu-id="87600-149">71</span></span>

<span data-ttu-id="87600-150">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="87600-151">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="87600-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="87600-152">72</span><span class="sxs-lookup"><span data-stu-id="87600-152">72</span></span>

<span data-ttu-id="87600-153">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="87600-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="87600-154">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="87600-155">73</span><span class="sxs-lookup"><span data-stu-id="87600-155">73</span></span>

<span data-ttu-id="87600-156">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="87600-157">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="87600-158">74</span><span class="sxs-lookup"><span data-stu-id="87600-158">74</span></span>

<span data-ttu-id="87600-159">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="87600-160">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="87600-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="87600-161">75</span><span class="sxs-lookup"><span data-stu-id="87600-161">75</span></span>

<span data-ttu-id="87600-162">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="87600-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="87600-163">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="87600-164">76</span><span class="sxs-lookup"><span data-stu-id="87600-164">76</span></span>

<span data-ttu-id="87600-165">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="87600-166">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="87600-167">77</span><span class="sxs-lookup"><span data-stu-id="87600-167">77</span></span>

<span data-ttu-id="87600-168">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="87600-169">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="87600-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="87600-170">78</span><span class="sxs-lookup"><span data-stu-id="87600-170">78</span></span>

<span data-ttu-id="87600-171">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="87600-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="87600-172">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="87600-173">79</span><span class="sxs-lookup"><span data-stu-id="87600-173">79</span></span>

<span data-ttu-id="87600-174">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="87600-175">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="87600-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="87600-176">80</span><span class="sxs-lookup"><span data-stu-id="87600-176">80</span></span>

<span data-ttu-id="87600-177">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="87600-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="87600-178">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="87600-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="87600-179">81</span><span class="sxs-lookup"><span data-stu-id="87600-179">81</span></span>

<span data-ttu-id="87600-180">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="87600-180">Unable to configure DHCP service.</span></span> <span data-ttu-id="87600-181">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="87600-181">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="87600-182">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="87600-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="87600-183">82</span><span class="sxs-lookup"><span data-stu-id="87600-183">82</span></span>

<span data-ttu-id="87600-184">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="87600-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="87600-185">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="87600-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="87600-186">83</span><span class="sxs-lookup"><span data-stu-id="87600-186">83</span></span>

<span data-ttu-id="87600-187">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="87600-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="87600-188">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="87600-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="87600-189">84</span><span class="sxs-lookup"><span data-stu-id="87600-189">84</span></span>

<span data-ttu-id="87600-190">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="87600-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="87600-191">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="87600-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="87600-192">85 %</span><span class="sxs-lookup"><span data-stu-id="87600-192">85</span></span>

<span data-ttu-id="87600-193">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="87600-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="87600-194">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="87600-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="87600-195">86</span><span class="sxs-lookup"><span data-stu-id="87600-195">86</span></span>

<span data-ttu-id="87600-196">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="87600-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="87600-197">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="87600-198">87</span><span class="sxs-lookup"><span data-stu-id="87600-198">87</span></span>

<span data-ttu-id="87600-199">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="87600-200">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="87600-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="87600-201">88</span><span class="sxs-lookup"><span data-stu-id="87600-201">88</span></span>

<span data-ttu-id="87600-202">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="87600-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="87600-203">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="87600-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="87600-204">89</span><span class="sxs-lookup"><span data-stu-id="87600-204">89</span></span>

<span data-ttu-id="87600-205">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="87600-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="87600-206">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="87600-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="87600-207">90</span><span class="sxs-lookup"><span data-stu-id="87600-207">90</span></span>

<span data-ttu-id="87600-208">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="87600-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="87600-209">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="87600-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="87600-210">91</span><span class="sxs-lookup"><span data-stu-id="87600-210">91</span></span>

<span data-ttu-id="87600-211">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="87600-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="87600-212">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="87600-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="87600-213">92</span><span class="sxs-lookup"><span data-stu-id="87600-213">92</span></span>

<span data-ttu-id="87600-214">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="87600-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="87600-215">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="87600-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="87600-216">93</span><span class="sxs-lookup"><span data-stu-id="87600-216">93</span></span>

<span data-ttu-id="87600-217">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="87600-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="87600-218">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="87600-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="87600-219">94</span><span class="sxs-lookup"><span data-stu-id="87600-219">94</span></span>

<span data-ttu-id="87600-220">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="87600-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="87600-221">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="87600-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="87600-222">95</span><span class="sxs-lookup"><span data-stu-id="87600-222">95</span></span>

<span data-ttu-id="87600-223">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="87600-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="87600-224">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="87600-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="87600-225">96</span><span class="sxs-lookup"><span data-stu-id="87600-225">96</span></span>

<span data-ttu-id="87600-226">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="87600-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="87600-227">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="87600-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="87600-228">97</span><span class="sxs-lookup"><span data-stu-id="87600-228">97</span></span>

<span data-ttu-id="87600-229">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="87600-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="87600-230">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="87600-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="87600-231">98</span><span class="sxs-lookup"><span data-stu-id="87600-231">98</span></span>

<span data-ttu-id="87600-232">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="87600-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="87600-233">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="87600-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="87600-234">100</span><span class="sxs-lookup"><span data-stu-id="87600-234">100</span></span>

<span data-ttu-id="87600-235">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="87600-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="87600-236">**2147786788**</span><span class="sxs-lookup"><span data-stu-id="87600-236">**2147786788**</span></span>
</dt> <dd>

<span data-ttu-id="87600-237">Verrou d’écriture non activé.</span><span class="sxs-lookup"><span data-stu-id="87600-237">Write lock not enabled.</span></span> <span data-ttu-id="87600-238">Pour plus d’informations, consultez [**INetCfgLock :: AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87600-238">For more information, see [**INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="87600-239">**Autres**</span><span class="sxs-lookup"><span data-stu-id="87600-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="87600-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="87600-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87600-241">Notes</span><span class="sxs-lookup"><span data-stu-id="87600-241">Remarks</span></span>

<span data-ttu-id="87600-242">Lorsque vous utilisez **EnableStatic** pour modifier l’adresse IP de l’ordinateur distant, tout en étant connecté via cet adaptateur, vous risquez de perdre la connexion à l’ordinateur distant et de recevoir un message d’erreur RPC non disponible-.</span><span class="sxs-lookup"><span data-stu-id="87600-242">When using **EnableStatic** to change the IP address of the remote computer, while being connected through that adapter, you will likely loose connection to the remote computer, and receive an RPC not available error-message.</span></span> <span data-ttu-id="87600-243">(Toutefois, les paramètres sont modifiés).</span><span class="sxs-lookup"><span data-stu-id="87600-243">(the settings are changed however).</span></span> <span data-ttu-id="87600-244">Pour éviter ce scénario, envisagez de modifier la passerelle et/ou les paramètres DNS avant de définir l’adresse IP de la carte.</span><span class="sxs-lookup"><span data-stu-id="87600-244">To avoid this scenario, consider changing the Gateway and/or DNS-settings prior to setting the adapter's IP-address.</span></span>

<span data-ttu-id="87600-245">Lorsque vous utilisez **EnableStatic** pour attribuer à un adaptateur une configuration IP statique, la fonction retourne « 81-impossible de configurer le service DHCP » si la carte est déjà configurée avec une adresse statique.</span><span class="sxs-lookup"><span data-stu-id="87600-245">When using **EnableStatic** to give an adapter a static IP configuration, the function returns an "81 - Unable to configure DHCP service" if the adapter is already configured with a static address.</span></span> <span data-ttu-id="87600-246">Toutefois, la fonction fonctionne toujours dans le paramètre avec la nouvelle opération.</span><span class="sxs-lookup"><span data-stu-id="87600-246">However, the function still succeeds in setting with the new operation.</span></span>

## <a name="examples"></a><span data-ttu-id="87600-247">Exemples</span><span class="sxs-lookup"><span data-stu-id="87600-247">Examples</span></span>

<span data-ttu-id="87600-248">L' [adresse IP statique, puis la jointure à un](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) exemple de code PowerShell de domaine, sur la Galerie TechNet, utilise **EnableStatic** pour ajouter une adresse IP statique à un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="87600-248">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell code sample, on TechNet Gallery, uses **EnableStatic** to add a static IP to a local machine.</span></span>

<span data-ttu-id="87600-249">L’exemple de code VBScript [attribuer une adresse IP statique](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) , sur la Galerie TechNet, utilise **EnableStatic** pour définir l’adresse IP d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="87600-249">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript code example, on TechNet Gallery, uses **EnableStatic** to set the IP address of a computer.</span></span>

<span data-ttu-id="87600-250">L’exemple VBScript suivant montre comment désactiver l’utilisation de DHCP sur une instance de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="87600-250">The following VBScript sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="87600-251">Dans ce cas, nous spécifions l’adaptateur avec un index égal à 0.</span><span class="sxs-lookup"><span data-stu-id="87600-251">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="87600-252">L’index approprié doit être sélectionné à partir des instances de la carte réseau Win32 \_ pour d’autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="87600-252">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="87600-253">Ce script s’applique uniquement aux systèmes basés sur NT modifiez les ipaddr et les variables de sous-réseau ci-dessous en fonction des valeurs que vous souhaitez appliquer à l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="87600-253">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



<span data-ttu-id="87600-254">L’exemple perl suivant montre comment désactiver l’utilisation de DHCP sur une instance de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="87600-254">The following Perl sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="87600-255">Dans ce cas, nous spécifions l’adaptateur avec un index égal à 0.</span><span class="sxs-lookup"><span data-stu-id="87600-255">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="87600-256">L’index approprié doit être sélectionné à partir des instances de la carte réseau Win32 \_ pour d’autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="87600-256">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="87600-257">Ce script s’applique uniquement aux systèmes basés sur NT modifiez les ipaddr et les variables de sous-réseau ci-dessous en fonction des valeurs que vous souhaitez appliquer à l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="87600-257">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="87600-258">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87600-258">Requirements</span></span>



| <span data-ttu-id="87600-259">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87600-259">Requirement</span></span> | <span data-ttu-id="87600-260">Valeur</span><span class="sxs-lookup"><span data-stu-id="87600-260">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87600-261">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87600-261">Minimum supported client</span></span><br/> | <span data-ttu-id="87600-262">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87600-262">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87600-263">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87600-263">Minimum supported server</span></span><br/> | <span data-ttu-id="87600-264">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87600-264">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87600-265">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87600-265">Namespace</span></span><br/>                | <span data-ttu-id="87600-266">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="87600-266">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87600-267">MOF</span><span class="sxs-lookup"><span data-stu-id="87600-267">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87600-268"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87600-268"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87600-269">DLL</span><span class="sxs-lookup"><span data-stu-id="87600-269">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87600-270"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87600-270"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87600-271">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87600-271">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87600-272">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="87600-272">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="87600-273">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="87600-273">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="87600-274">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="87600-274">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="87600-275">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="87600-275">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="87600-276">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="87600-276">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

