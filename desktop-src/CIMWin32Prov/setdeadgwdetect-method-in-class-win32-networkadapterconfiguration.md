---
description: La méthode statique de la classe WMI SetDeadGWDetect est utilisée pour activer la détection de passerelle inactive.
ms.assetid: c813aaef-7215-4759-b68f-7808fd203d9c
ms.tgt_platform: multiple
title: Méthode SetDeadGWDetect de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDeadGWDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83f62d84af193be99850f1a82b720a2983ca77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482985"
---
# <a name="setdeadgwdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1aa0f-103">Méthode SetDeadGWDetect de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="1aa0f-103">SetDeadGWDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1aa0f-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDeadGWDetect** est utilisée pour activer la détection de passerelle inactive.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-104">The **SetDeadGWDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable dead gateway detection.</span></span>

<span data-ttu-id="1aa0f-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1aa0f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1aa0f-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1aa0f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa0f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1aa0f-107">Syntax</span></span>


```mof
uint32 SetDeadGWDetect(
  [in] boolean DeadGWDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="1aa0f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1aa0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa0f-109">*DeadGWDetectEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1aa0f-109">*DeadGWDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-110">Si la **valeur est true**, la détection de passerelle inactive doit être activée.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-110">If **true**, dead gateway detection should be enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa0f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1aa0f-111">Return value</span></span>

<span data-ttu-id="1aa0f-112">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="1aa0f-113">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1aa0f-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1aa0f-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1aa0f-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1aa0f-115">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-116">0</span><span class="sxs-lookup"><span data-stu-id="1aa0f-116">0</span></span>

<span data-ttu-id="1aa0f-117">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-118">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-119">1</span><span class="sxs-lookup"><span data-stu-id="1aa0f-119">1</span></span>

<span data-ttu-id="1aa0f-120">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-121">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-122">64</span><span class="sxs-lookup"><span data-stu-id="1aa0f-122">64</span></span>

<span data-ttu-id="1aa0f-123">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-124">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-125">65</span><span class="sxs-lookup"><span data-stu-id="1aa0f-125">65</span></span>

<span data-ttu-id="1aa0f-126">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-127">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-128">66</span><span class="sxs-lookup"><span data-stu-id="1aa0f-128">66</span></span>

<span data-ttu-id="1aa0f-129">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-130">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-131">67</span><span class="sxs-lookup"><span data-stu-id="1aa0f-131">67</span></span>

<span data-ttu-id="1aa0f-132">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-133">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-134">68</span><span class="sxs-lookup"><span data-stu-id="1aa0f-134">68</span></span>

<span data-ttu-id="1aa0f-135">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-136">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-137">69</span><span class="sxs-lookup"><span data-stu-id="1aa0f-137">69</span></span>

<span data-ttu-id="1aa0f-138">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-139">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-140">70</span><span class="sxs-lookup"><span data-stu-id="1aa0f-140">70</span></span>

<span data-ttu-id="1aa0f-141">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-142">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-143">71</span><span class="sxs-lookup"><span data-stu-id="1aa0f-143">71</span></span>

<span data-ttu-id="1aa0f-144">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-145">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-146">72</span><span class="sxs-lookup"><span data-stu-id="1aa0f-146">72</span></span>

<span data-ttu-id="1aa0f-147">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-148">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-149">73</span><span class="sxs-lookup"><span data-stu-id="1aa0f-149">73</span></span>

<span data-ttu-id="1aa0f-150">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-151">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-152">74</span><span class="sxs-lookup"><span data-stu-id="1aa0f-152">74</span></span>

<span data-ttu-id="1aa0f-153">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-154">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-155">75</span><span class="sxs-lookup"><span data-stu-id="1aa0f-155">75</span></span>

<span data-ttu-id="1aa0f-156">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-157">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-158">76</span><span class="sxs-lookup"><span data-stu-id="1aa0f-158">76</span></span>

<span data-ttu-id="1aa0f-159">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-160">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-161">77</span><span class="sxs-lookup"><span data-stu-id="1aa0f-161">77</span></span>

<span data-ttu-id="1aa0f-162">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-163">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-164">78</span><span class="sxs-lookup"><span data-stu-id="1aa0f-164">78</span></span>

<span data-ttu-id="1aa0f-165">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-166">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-167">79</span><span class="sxs-lookup"><span data-stu-id="1aa0f-167">79</span></span>

<span data-ttu-id="1aa0f-168">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-169">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-170">80</span><span class="sxs-lookup"><span data-stu-id="1aa0f-170">80</span></span>

<span data-ttu-id="1aa0f-171">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-172">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-173">81</span><span class="sxs-lookup"><span data-stu-id="1aa0f-173">81</span></span>

<span data-ttu-id="1aa0f-174">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-175">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-176">82</span><span class="sxs-lookup"><span data-stu-id="1aa0f-176">82</span></span>

<span data-ttu-id="1aa0f-177">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-178">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-179">83</span><span class="sxs-lookup"><span data-stu-id="1aa0f-179">83</span></span>

<span data-ttu-id="1aa0f-180">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-181">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-182">84</span><span class="sxs-lookup"><span data-stu-id="1aa0f-182">84</span></span>

<span data-ttu-id="1aa0f-183">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-184">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-185">85 %</span><span class="sxs-lookup"><span data-stu-id="1aa0f-185">85</span></span>

<span data-ttu-id="1aa0f-186">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-187">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-188">86</span><span class="sxs-lookup"><span data-stu-id="1aa0f-188">86</span></span>

<span data-ttu-id="1aa0f-189">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-190">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-191">87</span><span class="sxs-lookup"><span data-stu-id="1aa0f-191">87</span></span>

<span data-ttu-id="1aa0f-192">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-193">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-194">88</span><span class="sxs-lookup"><span data-stu-id="1aa0f-194">88</span></span>

<span data-ttu-id="1aa0f-195">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-196">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-197">89</span><span class="sxs-lookup"><span data-stu-id="1aa0f-197">89</span></span>

<span data-ttu-id="1aa0f-198">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-199">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-200">90</span><span class="sxs-lookup"><span data-stu-id="1aa0f-200">90</span></span>

<span data-ttu-id="1aa0f-201">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-202">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-203">91</span><span class="sxs-lookup"><span data-stu-id="1aa0f-203">91</span></span>

<span data-ttu-id="1aa0f-204">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-205">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-206">92</span><span class="sxs-lookup"><span data-stu-id="1aa0f-206">92</span></span>

<span data-ttu-id="1aa0f-207">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-208">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-209">93</span><span class="sxs-lookup"><span data-stu-id="1aa0f-209">93</span></span>

<span data-ttu-id="1aa0f-210">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-211">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-212">94</span><span class="sxs-lookup"><span data-stu-id="1aa0f-212">94</span></span>

<span data-ttu-id="1aa0f-213">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-214">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-215">95</span><span class="sxs-lookup"><span data-stu-id="1aa0f-215">95</span></span>

<span data-ttu-id="1aa0f-216">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-217">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-218">96</span><span class="sxs-lookup"><span data-stu-id="1aa0f-218">96</span></span>

<span data-ttu-id="1aa0f-219">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-220">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-221">97</span><span class="sxs-lookup"><span data-stu-id="1aa0f-221">97</span></span>

<span data-ttu-id="1aa0f-222">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-223">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-224">98</span><span class="sxs-lookup"><span data-stu-id="1aa0f-224">98</span></span>

<span data-ttu-id="1aa0f-225">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-226">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-227">100</span><span class="sxs-lookup"><span data-stu-id="1aa0f-227">100</span></span>

<span data-ttu-id="1aa0f-228">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1aa0f-229">**Autres**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1aa0f-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="1aa0f-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1aa0f-231">Notes</span><span class="sxs-lookup"><span data-stu-id="1aa0f-231">Remarks</span></span>

<span data-ttu-id="1aa0f-232">Lorsque cette fonctionnalité est activée, TCP demande à l’adresse IP de passer à une passerelle de sauvegarde si elle retransmet un segment plusieurs fois sans recevoir de réponse.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-232">With this feature enabled, TCP asks IP to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

## <a name="examples"></a><span data-ttu-id="1aa0f-233">Exemples</span><span class="sxs-lookup"><span data-stu-id="1aa0f-233">Examples</span></span>

<span data-ttu-id="1aa0f-234">L’exemple VBScript [activer la détection de passerelle inactive pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) de la Galerie TechNet utilise **SetDeadGWDetect** pour configurer toutes les cartes réseau sur un ordinateur afin de détecter automatiquement les passerelles inactives.</span><span class="sxs-lookup"><span data-stu-id="1aa0f-234">The [Enable Dead Gateway Detection for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) VBScript sample on TechNet Gallery uses **SetDeadGWDetect** to configure all network adapters on a computer to automatically detect dead gateways.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa0f-235">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1aa0f-235">Requirements</span></span>



| <span data-ttu-id="1aa0f-236">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1aa0f-236">Requirement</span></span> | <span data-ttu-id="1aa0f-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="1aa0f-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa0f-238">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1aa0f-238">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa0f-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1aa0f-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1aa0f-240">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1aa0f-240">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa0f-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1aa0f-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1aa0f-242">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1aa0f-242">Namespace</span></span><br/>                | <span data-ttu-id="1aa0f-243">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1aa0f-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1aa0f-244">MOF</span><span class="sxs-lookup"><span data-stu-id="1aa0f-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1aa0f-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0f-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1aa0f-246">DLL</span><span class="sxs-lookup"><span data-stu-id="1aa0f-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aa0f-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0f-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa0f-248">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1aa0f-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa0f-249">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="1aa0f-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1aa0f-250">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1aa0f-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="1aa0f-251">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="1aa0f-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="1aa0f-252">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="1aa0f-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="1aa0f-253">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="1aa0f-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

