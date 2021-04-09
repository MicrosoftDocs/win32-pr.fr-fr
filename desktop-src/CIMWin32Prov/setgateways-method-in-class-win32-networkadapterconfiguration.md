---
description: SetGateways &\# 32 ; La méthode de classe WMI spécifie une liste de passerelles pour le routage des paquets vers un sous-réseau différent du sous-réseau auquel la carte réseau est connectée.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Méthode SetGateways de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861317"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="20dda-103">Méthode SetGateways de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="20dda-103">SetGateways method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="20dda-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetGateways** spécifie une liste de passerelles pour le routage des paquets vers un sous-réseau différent du sous-réseau auquel la carte réseau est connectée.</span><span class="sxs-lookup"><span data-stu-id="20dda-104">The **SetGateways** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method specifies a list of gateways for routing packets to a subnet that is different from the subnet that the network adapter is connected to.</span></span>

<span data-ttu-id="20dda-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="20dda-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="20dda-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="20dda-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="20dda-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20dda-107">Syntax</span></span>


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a><span data-ttu-id="20dda-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20dda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20dda-109">*DefaultIPGateway* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20dda-109">*DefaultIPGateway* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20dda-110">Liste des adresses IP vers les passerelles où les paquets réseau sont routés.</span><span class="sxs-lookup"><span data-stu-id="20dda-110">List of IP addresses to gateways where network packets are routed.</span></span>

</dd> <dt>

<span data-ttu-id="20dda-111">*GatewayCostMetric* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="20dda-111">*GatewayCostMetric* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20dda-112">Affecte une valeur comprise entre 1 et 9999, qui est utilisée pour calculer les itinéraires les plus rapides et les plus fiables.</span><span class="sxs-lookup"><span data-stu-id="20dda-112">Assigns a value that ranges from 1 to 9999, which is used to calculate the fastest and most reliable routes.</span></span> <span data-ttu-id="20dda-113">Les valeurs de ce paramètre correspondent aux valeurs du paramètre *DefaultIPGateway* .</span><span class="sxs-lookup"><span data-stu-id="20dda-113">The values of this parameter correspond with the values in the *DefaultIPGateway* parameter.</span></span> <span data-ttu-id="20dda-114">La valeur par défaut d’une passerelle est 1.</span><span class="sxs-lookup"><span data-stu-id="20dda-114">The default value for a gateway is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20dda-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20dda-115">Return value</span></span>

<span data-ttu-id="20dda-116">Retourne la valeur 0 (zéro) pour une exécution réussie lorsqu’un redémarrage n’est pas nécessaire, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et toute autre valeur en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="20dda-116">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other value if there is an error.</span></span> <span data-ttu-id="20dda-117">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="20dda-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="20dda-118">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="20dda-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="20dda-119">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="20dda-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-120">0</span><span class="sxs-lookup"><span data-stu-id="20dda-120">0</span></span>

</dd> <dt>

<span data-ttu-id="20dda-121">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="20dda-121">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-122">1</span><span class="sxs-lookup"><span data-stu-id="20dda-122">1</span></span>

</dd> <dt>

<span data-ttu-id="20dda-123">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="20dda-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-124">64</span><span class="sxs-lookup"><span data-stu-id="20dda-124">64</span></span>

<span data-ttu-id="20dda-125">Méthode non prise en charge lorsque la carte réseau est en mode DHCP.</span><span class="sxs-lookup"><span data-stu-id="20dda-125">Method not supported when the NIC is in DHCP mode.</span></span>

</dd> <dt>

<span data-ttu-id="20dda-126">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="20dda-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-127">65</span><span class="sxs-lookup"><span data-stu-id="20dda-127">65</span></span>

</dd> <dt>

<span data-ttu-id="20dda-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-129">66</span><span class="sxs-lookup"><span data-stu-id="20dda-129">66</span></span>

</dd> <dt>

<span data-ttu-id="20dda-130">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="20dda-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-131">67</span><span class="sxs-lookup"><span data-stu-id="20dda-131">67</span></span>

</dd> <dt>

<span data-ttu-id="20dda-132">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-133">68</span><span class="sxs-lookup"><span data-stu-id="20dda-133">68</span></span>

</dd> <dt>

<span data-ttu-id="20dda-134">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="20dda-134">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-135">69</span><span class="sxs-lookup"><span data-stu-id="20dda-135">69</span></span>

</dd> <dt>

<span data-ttu-id="20dda-136">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-136">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-137">70</span><span class="sxs-lookup"><span data-stu-id="20dda-137">70</span></span>

</dd> <dt>

<span data-ttu-id="20dda-138">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-138">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-139">71</span><span class="sxs-lookup"><span data-stu-id="20dda-139">71</span></span>

</dd> <dt>

<span data-ttu-id="20dda-140">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="20dda-140">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-141">72</span><span class="sxs-lookup"><span data-stu-id="20dda-141">72</span></span>

</dd> <dt>

<span data-ttu-id="20dda-142">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-142">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-143">73</span><span class="sxs-lookup"><span data-stu-id="20dda-143">73</span></span>

</dd> <dt>

<span data-ttu-id="20dda-144">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-144">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-145">74</span><span class="sxs-lookup"><span data-stu-id="20dda-145">74</span></span>

</dd> <dt>

<span data-ttu-id="20dda-146">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="20dda-146">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-147">75</span><span class="sxs-lookup"><span data-stu-id="20dda-147">75</span></span>

</dd> <dt>

<span data-ttu-id="20dda-148">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-148">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-149">76</span><span class="sxs-lookup"><span data-stu-id="20dda-149">76</span></span>

</dd> <dt>

<span data-ttu-id="20dda-150">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-150">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-151">77</span><span class="sxs-lookup"><span data-stu-id="20dda-151">77</span></span>

</dd> <dt>

<span data-ttu-id="20dda-152">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="20dda-152">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-153">78</span><span class="sxs-lookup"><span data-stu-id="20dda-153">78</span></span>

</dd> <dt>

<span data-ttu-id="20dda-154">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-154">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-155">79</span><span class="sxs-lookup"><span data-stu-id="20dda-155">79</span></span>

</dd> <dt>

<span data-ttu-id="20dda-156">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="20dda-156">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-157">80</span><span class="sxs-lookup"><span data-stu-id="20dda-157">80</span></span>

</dd> <dt>

<span data-ttu-id="20dda-158">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="20dda-158">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-159">81</span><span class="sxs-lookup"><span data-stu-id="20dda-159">81</span></span>

</dd> <dt>

<span data-ttu-id="20dda-160">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="20dda-160">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-161">82</span><span class="sxs-lookup"><span data-stu-id="20dda-161">82</span></span>

</dd> <dt>

<span data-ttu-id="20dda-162">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="20dda-162">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-163">83</span><span class="sxs-lookup"><span data-stu-id="20dda-163">83</span></span>

</dd> <dt>

<span data-ttu-id="20dda-164">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="20dda-164">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-165">84</span><span class="sxs-lookup"><span data-stu-id="20dda-165">84</span></span>

</dd> <dt>

<span data-ttu-id="20dda-166">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="20dda-166">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-167">85 %</span><span class="sxs-lookup"><span data-stu-id="20dda-167">85</span></span>

</dd> <dt>

<span data-ttu-id="20dda-168">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="20dda-168">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-169">86</span><span class="sxs-lookup"><span data-stu-id="20dda-169">86</span></span>

</dd> <dt>

<span data-ttu-id="20dda-170">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-170">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-171">87</span><span class="sxs-lookup"><span data-stu-id="20dda-171">87</span></span>

</dd> <dt>

<span data-ttu-id="20dda-172">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="20dda-172">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-173">88</span><span class="sxs-lookup"><span data-stu-id="20dda-173">88</span></span>

</dd> <dt>

<span data-ttu-id="20dda-174">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="20dda-174">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-175">89</span><span class="sxs-lookup"><span data-stu-id="20dda-175">89</span></span>

</dd> <dt>

<span data-ttu-id="20dda-176">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="20dda-176">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-177">90</span><span class="sxs-lookup"><span data-stu-id="20dda-177">90</span></span>

</dd> <dt>

<span data-ttu-id="20dda-178">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="20dda-178">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-179">91</span><span class="sxs-lookup"><span data-stu-id="20dda-179">91</span></span>

</dd> <dt>

<span data-ttu-id="20dda-180">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="20dda-180">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-181">92</span><span class="sxs-lookup"><span data-stu-id="20dda-181">92</span></span>

</dd> <dt>

<span data-ttu-id="20dda-182">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="20dda-182">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-183">93</span><span class="sxs-lookup"><span data-stu-id="20dda-183">93</span></span>

</dd> <dt>

<span data-ttu-id="20dda-184">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="20dda-184">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-185">94</span><span class="sxs-lookup"><span data-stu-id="20dda-185">94</span></span>

</dd> <dt>

<span data-ttu-id="20dda-186">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="20dda-186">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-187">95</span><span class="sxs-lookup"><span data-stu-id="20dda-187">95</span></span>

</dd> <dt>

<span data-ttu-id="20dda-188">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="20dda-188">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-189">96</span><span class="sxs-lookup"><span data-stu-id="20dda-189">96</span></span>

</dd> <dt>

<span data-ttu-id="20dda-190">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="20dda-190">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-191">97</span><span class="sxs-lookup"><span data-stu-id="20dda-191">97</span></span>

</dd> <dt>

<span data-ttu-id="20dda-192">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="20dda-192">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-193">98</span><span class="sxs-lookup"><span data-stu-id="20dda-193">98</span></span>

</dd> <dt>

<span data-ttu-id="20dda-194">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="20dda-194">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-195">100</span><span class="sxs-lookup"><span data-stu-id="20dda-195">100</span></span>

</dd> <dt>

<span data-ttu-id="20dda-196">**Autres**</span><span class="sxs-lookup"><span data-stu-id="20dda-196">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="20dda-197">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="20dda-197">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20dda-198">Notes</span><span class="sxs-lookup"><span data-stu-id="20dda-198">Remarks</span></span>

<span data-ttu-id="20dda-199">Cette méthode fonctionne uniquement lorsque la carte d’interface réseau (NIC) est en mode IP statique.</span><span class="sxs-lookup"><span data-stu-id="20dda-199">This method only works when the Network Interface Card (NIC) is in the static IP mode.</span></span>

<span data-ttu-id="20dda-200">Pour effacer la passerelle, définissez votre passerelle sur la même adresse IP que celle que vous utilisez sur [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="20dda-200">To clear the gateway, set your gateway to the same IP you use on [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span></span>

## <a name="examples"></a><span data-ttu-id="20dda-201">Exemples</span><span class="sxs-lookup"><span data-stu-id="20dda-201">Examples</span></span>

<span data-ttu-id="20dda-202">L’exemple de [modification de passerelles pour une carte réseau](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) configure deux passerelles pour une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="20dda-202">The [Modify the Gateways for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript sample configures two gateways for a network adapter.</span></span>

<span data-ttu-id="20dda-203">L’exemple VBScript [attribuer une adresse IP statique](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) définit l’adresse IP et la passerelle d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="20dda-203">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript sample sets the IP address and gateway of a computer.</span></span>

<span data-ttu-id="20dda-204">L' [adresse IP statique, puis la jointure à un](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) exemple PowerShell de domaine facilite la reconstruction des machines.</span><span class="sxs-lookup"><span data-stu-id="20dda-204">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell sample assists in rebuilding machines.</span></span>

## <a name="requirements"></a><span data-ttu-id="20dda-205">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20dda-205">Requirements</span></span>



| <span data-ttu-id="20dda-206">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20dda-206">Requirement</span></span> | <span data-ttu-id="20dda-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="20dda-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20dda-208">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20dda-208">Minimum supported client</span></span><br/> | <span data-ttu-id="20dda-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20dda-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20dda-210">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20dda-210">Minimum supported server</span></span><br/> | <span data-ttu-id="20dda-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20dda-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20dda-212">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="20dda-212">Namespace</span></span><br/>                | <span data-ttu-id="20dda-213">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="20dda-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20dda-214">MOF</span><span class="sxs-lookup"><span data-stu-id="20dda-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20dda-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20dda-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20dda-216">DLL</span><span class="sxs-lookup"><span data-stu-id="20dda-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20dda-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20dda-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20dda-218">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20dda-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20dda-219">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="20dda-219">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="20dda-220">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="20dda-220">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="20dda-221">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="20dda-221">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="20dda-222">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="20dda-222">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="20dda-223">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="20dda-223">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

