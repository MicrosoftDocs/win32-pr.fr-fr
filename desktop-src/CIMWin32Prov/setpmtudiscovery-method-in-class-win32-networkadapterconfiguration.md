---
description: La méthode statique de la classe WMI SetPMTUDiscovery est utilisée pour activer la détection de l’unité de transmission maximale (MTU) sur le chemin d’accès à un hôte distant.
ms.assetid: 43c640bb-c4e7-4b4b-9c18-6cc426229954
ms.tgt_platform: multiple
title: Méthode SetPMTUDiscovery de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUDiscovery
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef3bc9ad5d6203077275f3665c4b0efc98265fbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748564"
---
# <a name="setpmtudiscovery-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="43568-103">Méthode SetPMTUDiscovery de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="43568-103">SetPMTUDiscovery method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="43568-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUDiscovery** est utilisée pour activer la détection de l’unité de transmission maximale (MTU) sur le chemin d’accès à un hôte distant.</span><span class="sxs-lookup"><span data-stu-id="43568-104">The **SetPMTUDiscovery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Maximum Transmission Unit (MTU) discovery over the path to a remote host.</span></span>

<span data-ttu-id="43568-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="43568-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="43568-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="43568-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="43568-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43568-107">Syntax</span></span>


```mof
uint32 SetPMTUDiscovery(
  [in] boolean PMTUDiscoveryEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="43568-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43568-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43568-109">*PMTUDiscoveryEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43568-109">*PMTUDiscoveryEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43568-110">Si la **valeur est true**, le protocole TCP est activé pour tenter de découvrir l’unité de transmission maximale (MTU) ou la plus grande taille de paquet sur le chemin d’accès à un hôte distant.</span><span class="sxs-lookup"><span data-stu-id="43568-110">If **true**, TCP is enabled to attempt to discover the Maximum Transmission Unit (MTU) or largest packet size over the path to a remote host.</span></span> <span data-ttu-id="43568-111">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="43568-111">The default is **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43568-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43568-112">Return value</span></span>

<span data-ttu-id="43568-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="43568-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="43568-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="43568-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="43568-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="43568-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="43568-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="43568-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="43568-117">0</span><span class="sxs-lookup"><span data-stu-id="43568-117">0</span></span>

<span data-ttu-id="43568-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="43568-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="43568-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="43568-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="43568-120">1</span><span class="sxs-lookup"><span data-stu-id="43568-120">1</span></span>

<span data-ttu-id="43568-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="43568-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="43568-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="43568-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="43568-123">64</span><span class="sxs-lookup"><span data-stu-id="43568-123">64</span></span>

<span data-ttu-id="43568-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="43568-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="43568-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="43568-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="43568-126">65</span><span class="sxs-lookup"><span data-stu-id="43568-126">65</span></span>

<span data-ttu-id="43568-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="43568-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="43568-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="43568-129">66</span><span class="sxs-lookup"><span data-stu-id="43568-129">66</span></span>

<span data-ttu-id="43568-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="43568-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="43568-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="43568-132">67</span><span class="sxs-lookup"><span data-stu-id="43568-132">67</span></span>

<span data-ttu-id="43568-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="43568-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="43568-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="43568-135">68</span><span class="sxs-lookup"><span data-stu-id="43568-135">68</span></span>

<span data-ttu-id="43568-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="43568-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="43568-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="43568-138">69</span><span class="sxs-lookup"><span data-stu-id="43568-138">69</span></span>

<span data-ttu-id="43568-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="43568-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="43568-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="43568-141">70</span><span class="sxs-lookup"><span data-stu-id="43568-141">70</span></span>

<span data-ttu-id="43568-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="43568-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="43568-144">71</span><span class="sxs-lookup"><span data-stu-id="43568-144">71</span></span>

<span data-ttu-id="43568-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="43568-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="43568-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="43568-147">72</span><span class="sxs-lookup"><span data-stu-id="43568-147">72</span></span>

<span data-ttu-id="43568-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="43568-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="43568-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="43568-150">73</span><span class="sxs-lookup"><span data-stu-id="43568-150">73</span></span>

<span data-ttu-id="43568-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="43568-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="43568-153">74</span><span class="sxs-lookup"><span data-stu-id="43568-153">74</span></span>

<span data-ttu-id="43568-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="43568-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="43568-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="43568-156">75</span><span class="sxs-lookup"><span data-stu-id="43568-156">75</span></span>

<span data-ttu-id="43568-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="43568-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="43568-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="43568-159">76</span><span class="sxs-lookup"><span data-stu-id="43568-159">76</span></span>

<span data-ttu-id="43568-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="43568-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="43568-162">77</span><span class="sxs-lookup"><span data-stu-id="43568-162">77</span></span>

<span data-ttu-id="43568-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="43568-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="43568-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="43568-165">78</span><span class="sxs-lookup"><span data-stu-id="43568-165">78</span></span>

<span data-ttu-id="43568-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="43568-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="43568-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="43568-168">79</span><span class="sxs-lookup"><span data-stu-id="43568-168">79</span></span>

<span data-ttu-id="43568-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="43568-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="43568-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="43568-171">80</span><span class="sxs-lookup"><span data-stu-id="43568-171">80</span></span>

<span data-ttu-id="43568-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="43568-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="43568-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="43568-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="43568-174">81</span><span class="sxs-lookup"><span data-stu-id="43568-174">81</span></span>

<span data-ttu-id="43568-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="43568-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="43568-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="43568-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="43568-177">82</span><span class="sxs-lookup"><span data-stu-id="43568-177">82</span></span>

<span data-ttu-id="43568-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="43568-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="43568-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="43568-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="43568-180">83</span><span class="sxs-lookup"><span data-stu-id="43568-180">83</span></span>

<span data-ttu-id="43568-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="43568-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="43568-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="43568-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="43568-183">84</span><span class="sxs-lookup"><span data-stu-id="43568-183">84</span></span>

<span data-ttu-id="43568-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="43568-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="43568-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="43568-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="43568-186">85 %</span><span class="sxs-lookup"><span data-stu-id="43568-186">85</span></span>

<span data-ttu-id="43568-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="43568-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="43568-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="43568-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="43568-189">86</span><span class="sxs-lookup"><span data-stu-id="43568-189">86</span></span>

<span data-ttu-id="43568-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="43568-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="43568-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="43568-192">87</span><span class="sxs-lookup"><span data-stu-id="43568-192">87</span></span>

<span data-ttu-id="43568-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="43568-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="43568-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="43568-195">88</span><span class="sxs-lookup"><span data-stu-id="43568-195">88</span></span>

<span data-ttu-id="43568-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="43568-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="43568-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="43568-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="43568-198">89</span><span class="sxs-lookup"><span data-stu-id="43568-198">89</span></span>

<span data-ttu-id="43568-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="43568-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="43568-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="43568-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="43568-201">90</span><span class="sxs-lookup"><span data-stu-id="43568-201">90</span></span>

<span data-ttu-id="43568-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="43568-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="43568-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="43568-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="43568-204">91</span><span class="sxs-lookup"><span data-stu-id="43568-204">91</span></span>

<span data-ttu-id="43568-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="43568-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="43568-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="43568-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="43568-207">92</span><span class="sxs-lookup"><span data-stu-id="43568-207">92</span></span>

<span data-ttu-id="43568-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="43568-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="43568-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="43568-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="43568-210">93</span><span class="sxs-lookup"><span data-stu-id="43568-210">93</span></span>

<span data-ttu-id="43568-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="43568-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="43568-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="43568-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="43568-213">94</span><span class="sxs-lookup"><span data-stu-id="43568-213">94</span></span>

<span data-ttu-id="43568-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="43568-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="43568-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="43568-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="43568-216">95</span><span class="sxs-lookup"><span data-stu-id="43568-216">95</span></span>

<span data-ttu-id="43568-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="43568-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="43568-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="43568-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="43568-219">96</span><span class="sxs-lookup"><span data-stu-id="43568-219">96</span></span>

<span data-ttu-id="43568-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="43568-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="43568-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="43568-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="43568-222">97</span><span class="sxs-lookup"><span data-stu-id="43568-222">97</span></span>

<span data-ttu-id="43568-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="43568-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="43568-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="43568-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="43568-225">98</span><span class="sxs-lookup"><span data-stu-id="43568-225">98</span></span>

<span data-ttu-id="43568-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="43568-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="43568-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="43568-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="43568-228">100</span><span class="sxs-lookup"><span data-stu-id="43568-228">100</span></span>

<span data-ttu-id="43568-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="43568-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="43568-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="43568-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="43568-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="43568-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43568-232">Notes</span><span class="sxs-lookup"><span data-stu-id="43568-232">Remarks</span></span>

<span data-ttu-id="43568-233">En détectant le chemin MTU et en limitant les segments TCP à cette taille, TCP peut éliminer la fragmentation sur les routeurs sur le chemin qui connecte les réseaux avec différents MTU.</span><span class="sxs-lookup"><span data-stu-id="43568-233">By discovering the Path MTU and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="43568-234">La fragmentation affecte le débit TCP et la congestion du réseau.</span><span class="sxs-lookup"><span data-stu-id="43568-234">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="43568-235">Si vous affectez la **valeur false** à ce paramètre, un MTU de 576 octets est utilisé pour toutes les connexions qui ne sont pas des ordinateurs sur le sous-réseau local</span><span class="sxs-lookup"><span data-stu-id="43568-235">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet</span></span>

## <a name="examples"></a><span data-ttu-id="43568-236">Exemples</span><span class="sxs-lookup"><span data-stu-id="43568-236">Examples</span></span>

<span data-ttu-id="43568-237">L’exemple VBScript [activer la découverte PMTU sur toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) permet à un ordinateur de découvrir automatiquement l’unité de transmission maximale sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="43568-237">The [Enable PMTU Discovery on all Network Adapters](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript sample enables a computer to automatically discover the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="43568-238">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43568-238">Requirements</span></span>



| <span data-ttu-id="43568-239">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43568-239">Requirement</span></span> | <span data-ttu-id="43568-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="43568-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43568-241">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43568-241">Minimum supported client</span></span><br/> | <span data-ttu-id="43568-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43568-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43568-243">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43568-243">Minimum supported server</span></span><br/> | <span data-ttu-id="43568-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43568-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43568-245">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="43568-245">Namespace</span></span><br/>                | <span data-ttu-id="43568-246">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="43568-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43568-247">MOF</span><span class="sxs-lookup"><span data-stu-id="43568-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43568-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43568-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43568-249">DLL</span><span class="sxs-lookup"><span data-stu-id="43568-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43568-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43568-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43568-251">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43568-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43568-252">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="43568-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="43568-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="43568-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="43568-254">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="43568-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="43568-255">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="43568-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="43568-256">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="43568-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

