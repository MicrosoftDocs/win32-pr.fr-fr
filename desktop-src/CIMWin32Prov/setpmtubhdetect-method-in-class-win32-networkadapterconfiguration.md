---
description: La méthode statique de la classe WMI SetPMTUBHDetect est utilisée pour activer la détection des routeurs de trou noir lors de la détection de l’unité de transmission de chemin d’accès.
ms.assetid: a1e45ed9-85a9-4fdd-890a-d578c3f94b72
ms.tgt_platform: multiple
title: Méthode SetPMTUBHDetect de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUBHDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 098652c6ea0a53f9d3b1f616def3dd8b5e7228af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110942"
---
# <a name="setpmtubhdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="12c02-103">Méthode SetPMTUBHDetect de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="12c02-103">SetPMTUBHDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="12c02-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUBHDetect** est utilisée pour activer la détection des routeurs de trou noir lors de la détection de l’unité de transmission de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="12c02-104">The **SetPMTUBHDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable the detection of Black Hole routers while doing Path MTU Discovery.</span></span>

<span data-ttu-id="12c02-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="12c02-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="12c02-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="12c02-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="12c02-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12c02-107">Syntax</span></span>


```mof
uint32 SetPMTUBHDetect(
  [in] boolean PMTUBHDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="12c02-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12c02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c02-109">*PMTUBHDetectEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12c02-109">*PMTUBHDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c02-110">Si la **valeur est true**, le protocole TCP tente de détecter les paquets de trous noirs et de routage dans différents chemins d’accès réseau.</span><span class="sxs-lookup"><span data-stu-id="12c02-110">If **true**, TCP attempts to discover Black Hole and route packets in different network paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c02-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12c02-111">Return value</span></span>

<span data-ttu-id="12c02-112">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="12c02-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="12c02-113">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="12c02-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="12c02-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="12c02-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="12c02-115">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="12c02-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-116">0</span><span class="sxs-lookup"><span data-stu-id="12c02-116">0</span></span>

<span data-ttu-id="12c02-117">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="12c02-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-118">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="12c02-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-119">1</span><span class="sxs-lookup"><span data-stu-id="12c02-119">1</span></span>

<span data-ttu-id="12c02-120">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="12c02-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-121">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="12c02-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-122">64</span><span class="sxs-lookup"><span data-stu-id="12c02-122">64</span></span>

<span data-ttu-id="12c02-123">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="12c02-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-124">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="12c02-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-125">65</span><span class="sxs-lookup"><span data-stu-id="12c02-125">65</span></span>

<span data-ttu-id="12c02-126">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="12c02-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-127">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-128">66</span><span class="sxs-lookup"><span data-stu-id="12c02-128">66</span></span>

<span data-ttu-id="12c02-129">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-130">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="12c02-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-131">67</span><span class="sxs-lookup"><span data-stu-id="12c02-131">67</span></span>

<span data-ttu-id="12c02-132">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="12c02-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-133">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-134">68</span><span class="sxs-lookup"><span data-stu-id="12c02-134">68</span></span>

<span data-ttu-id="12c02-135">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-136">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="12c02-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-137">69</span><span class="sxs-lookup"><span data-stu-id="12c02-137">69</span></span>

<span data-ttu-id="12c02-138">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="12c02-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-139">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-140">70</span><span class="sxs-lookup"><span data-stu-id="12c02-140">70</span></span>

<span data-ttu-id="12c02-141">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-142">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-143">71</span><span class="sxs-lookup"><span data-stu-id="12c02-143">71</span></span>

<span data-ttu-id="12c02-144">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-145">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="12c02-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-146">72</span><span class="sxs-lookup"><span data-stu-id="12c02-146">72</span></span>

<span data-ttu-id="12c02-147">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="12c02-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-148">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-149">73</span><span class="sxs-lookup"><span data-stu-id="12c02-149">73</span></span>

<span data-ttu-id="12c02-150">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-151">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-152">74</span><span class="sxs-lookup"><span data-stu-id="12c02-152">74</span></span>

<span data-ttu-id="12c02-153">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-154">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="12c02-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-155">75</span><span class="sxs-lookup"><span data-stu-id="12c02-155">75</span></span>

<span data-ttu-id="12c02-156">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="12c02-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-157">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-158">76</span><span class="sxs-lookup"><span data-stu-id="12c02-158">76</span></span>

<span data-ttu-id="12c02-159">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-160">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-161">77</span><span class="sxs-lookup"><span data-stu-id="12c02-161">77</span></span>

<span data-ttu-id="12c02-162">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-163">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="12c02-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-164">78</span><span class="sxs-lookup"><span data-stu-id="12c02-164">78</span></span>

<span data-ttu-id="12c02-165">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="12c02-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-166">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-167">79</span><span class="sxs-lookup"><span data-stu-id="12c02-167">79</span></span>

<span data-ttu-id="12c02-168">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-169">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="12c02-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-170">80</span><span class="sxs-lookup"><span data-stu-id="12c02-170">80</span></span>

<span data-ttu-id="12c02-171">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="12c02-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-172">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="12c02-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-173">81</span><span class="sxs-lookup"><span data-stu-id="12c02-173">81</span></span>

<span data-ttu-id="12c02-174">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="12c02-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-175">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="12c02-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-176">82</span><span class="sxs-lookup"><span data-stu-id="12c02-176">82</span></span>

<span data-ttu-id="12c02-177">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="12c02-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-178">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="12c02-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-179">83</span><span class="sxs-lookup"><span data-stu-id="12c02-179">83</span></span>

<span data-ttu-id="12c02-180">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="12c02-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-181">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="12c02-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-182">84</span><span class="sxs-lookup"><span data-stu-id="12c02-182">84</span></span>

<span data-ttu-id="12c02-183">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="12c02-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-184">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="12c02-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-185">85 %</span><span class="sxs-lookup"><span data-stu-id="12c02-185">85</span></span>

<span data-ttu-id="12c02-186">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="12c02-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-187">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="12c02-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-188">86</span><span class="sxs-lookup"><span data-stu-id="12c02-188">86</span></span>

<span data-ttu-id="12c02-189">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="12c02-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-190">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-191">87</span><span class="sxs-lookup"><span data-stu-id="12c02-191">87</span></span>

<span data-ttu-id="12c02-192">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-193">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="12c02-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-194">88</span><span class="sxs-lookup"><span data-stu-id="12c02-194">88</span></span>

<span data-ttu-id="12c02-195">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="12c02-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-196">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="12c02-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-197">89</span><span class="sxs-lookup"><span data-stu-id="12c02-197">89</span></span>

<span data-ttu-id="12c02-198">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="12c02-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-199">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="12c02-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-200">90</span><span class="sxs-lookup"><span data-stu-id="12c02-200">90</span></span>

<span data-ttu-id="12c02-201">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="12c02-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-202">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="12c02-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-203">91</span><span class="sxs-lookup"><span data-stu-id="12c02-203">91</span></span>

<span data-ttu-id="12c02-204">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="12c02-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-205">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="12c02-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-206">92</span><span class="sxs-lookup"><span data-stu-id="12c02-206">92</span></span>

<span data-ttu-id="12c02-207">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="12c02-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-208">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="12c02-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-209">93</span><span class="sxs-lookup"><span data-stu-id="12c02-209">93</span></span>

<span data-ttu-id="12c02-210">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="12c02-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-211">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="12c02-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-212">94</span><span class="sxs-lookup"><span data-stu-id="12c02-212">94</span></span>

<span data-ttu-id="12c02-213">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="12c02-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-214">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="12c02-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-215">95</span><span class="sxs-lookup"><span data-stu-id="12c02-215">95</span></span>

<span data-ttu-id="12c02-216">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="12c02-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-217">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="12c02-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-218">96</span><span class="sxs-lookup"><span data-stu-id="12c02-218">96</span></span>

<span data-ttu-id="12c02-219">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="12c02-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-220">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="12c02-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-221">97</span><span class="sxs-lookup"><span data-stu-id="12c02-221">97</span></span>

<span data-ttu-id="12c02-222">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="12c02-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-223">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="12c02-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-224">98</span><span class="sxs-lookup"><span data-stu-id="12c02-224">98</span></span>

<span data-ttu-id="12c02-225">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="12c02-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-226">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="12c02-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-227">100</span><span class="sxs-lookup"><span data-stu-id="12c02-227">100</span></span>

<span data-ttu-id="12c02-228">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="12c02-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="12c02-229">**Autres**</span><span class="sxs-lookup"><span data-stu-id="12c02-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="12c02-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="12c02-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12c02-231">Notes</span><span class="sxs-lookup"><span data-stu-id="12c02-231">Remarks</span></span>

<span data-ttu-id="12c02-232">Un routeur de trou noir ne retourne pas les messages de destination ICMP (Internet Control Message Protocol) inaccessibles lorsqu’il doit fragmenter un datagramme IP avec le bit de non fragment défini.</span><span class="sxs-lookup"><span data-stu-id="12c02-232">A Black Hole router does not return the Internet Control Message Protocol (ICMP) Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="12c02-233">TCP dépend de la réception de ces messages pour effectuer la détection du chemin MTU.</span><span class="sxs-lookup"><span data-stu-id="12c02-233">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span>

<span data-ttu-id="12c02-234">Une fois cette fonctionnalité activée, le protocole TCP essaiera d’envoyer des segments sans le bit de non fragment défini si plusieurs retransmissions d’un segment ne sont pas acquittées.</span><span class="sxs-lookup"><span data-stu-id="12c02-234">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="12c02-235">Si le segment est reconnu par conséquent, la taille maximale du segment (MSS) sera réduite et le bit de non fragment sera défini dans les paquets futurs sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="12c02-235">If the segment is acknowledged as a result, the maximum segment size (MSS) will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="12c02-236">L’activation de la détection de trou noir augmente le nombre maximal de retransmissions effectuées pour un segment donné.</span><span class="sxs-lookup"><span data-stu-id="12c02-236">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span>

## <a name="examples"></a><span data-ttu-id="12c02-237">Exemples</span><span class="sxs-lookup"><span data-stu-id="12c02-237">Examples</span></span>

<span data-ttu-id="12c02-238">La [détection de modification de PMTUBH sur toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) permet la détection automatique des routeurs de trou noir lors de la détermination de l’unité de transmission maximale sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="12c02-238">The [Modify PMTUBH Detection on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) enables the auto-discovery of black hole routers when determining the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="12c02-239">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12c02-239">Requirements</span></span>



| <span data-ttu-id="12c02-240">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12c02-240">Requirement</span></span> | <span data-ttu-id="12c02-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="12c02-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12c02-242">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12c02-242">Minimum supported client</span></span><br/> | <span data-ttu-id="12c02-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12c02-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12c02-244">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12c02-244">Minimum supported server</span></span><br/> | <span data-ttu-id="12c02-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12c02-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12c02-246">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="12c02-246">Namespace</span></span><br/>                | <span data-ttu-id="12c02-247">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="12c02-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12c02-248">MOF</span><span class="sxs-lookup"><span data-stu-id="12c02-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12c02-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12c02-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12c02-250">DLL</span><span class="sxs-lookup"><span data-stu-id="12c02-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12c02-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12c02-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c02-252">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12c02-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c02-253">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="12c02-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="12c02-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="12c02-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="12c02-255">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="12c02-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="12c02-256">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="12c02-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="12c02-257">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="12c02-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

