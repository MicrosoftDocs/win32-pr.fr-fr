---
description: La méthode statique de la classe WMI SetMTU permet de définir l’unité de transmission maximale (MTU) par défaut pour une interface réseau.
ms.assetid: 262c8bd7-1057-4204-80ab-725c60fc9c52
ms.tgt_platform: multiple
title: Méthode SetMTU de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetMTU
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 466c344892f2c4bf4a1e979ac9c1f50cd709325a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748572"
---
# <a name="setmtu-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2913c-103">Méthode SetMTU de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="2913c-103">SetMTU method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2913c-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetMTU** permet de définir l’unité de transmission maximale (MTU) par défaut pour une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="2913c-104">The **SetMTU** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Maximum Transmission Unit (MTU) for a network interface.</span></span>

<span data-ttu-id="2913c-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2913c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2913c-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2913c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2913c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2913c-107">Syntax</span></span>


```mof
uint32 SetMTU(
  [in] uint32 MTU
);
```



## <a name="parameters"></a><span data-ttu-id="2913c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2913c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2913c-109">*Unité MTU* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2913c-109">*MTU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2913c-110">Unité de transmission maximale (MTU) par défaut pour une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="2913c-110">Default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="2913c-111">La plage de cette valeur s’étend sur la taille minimale des paquets (68) au MTU pris en charge par le réseau sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2913c-111">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2913c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2913c-112">Return value</span></span>

<span data-ttu-id="2913c-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2913c-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="2913c-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2913c-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2913c-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2913c-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2913c-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="2913c-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-117">0</span><span class="sxs-lookup"><span data-stu-id="2913c-117">0</span></span>

<span data-ttu-id="2913c-118">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="2913c-118">Successful completion.</span></span> <span data-ttu-id="2913c-119">Aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2913c-119">No reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-120">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="2913c-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-121">1</span><span class="sxs-lookup"><span data-stu-id="2913c-121">1</span></span>

<span data-ttu-id="2913c-122">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="2913c-122">Successful completion.</span></span> <span data-ttu-id="2913c-123">Le redémarrage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2913c-123">Reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-124">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="2913c-124">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-125">64</span><span class="sxs-lookup"><span data-stu-id="2913c-125">64</span></span>

<span data-ttu-id="2913c-126">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="2913c-126">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-127">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="2913c-127">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-128">65</span><span class="sxs-lookup"><span data-stu-id="2913c-128">65</span></span>

<span data-ttu-id="2913c-129">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="2913c-129">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-130">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-130">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-131">66</span><span class="sxs-lookup"><span data-stu-id="2913c-131">66</span></span>

<span data-ttu-id="2913c-132">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-132">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-133">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="2913c-133">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-134">67</span><span class="sxs-lookup"><span data-stu-id="2913c-134">67</span></span>

<span data-ttu-id="2913c-135">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="2913c-135">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-136">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-136">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-137">68</span><span class="sxs-lookup"><span data-stu-id="2913c-137">68</span></span>

<span data-ttu-id="2913c-138">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-138">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-139">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="2913c-139">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-140">69</span><span class="sxs-lookup"><span data-stu-id="2913c-140">69</span></span>

<span data-ttu-id="2913c-141">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2913c-141">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-142">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-142">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-143">70</span><span class="sxs-lookup"><span data-stu-id="2913c-143">70</span></span>

<span data-ttu-id="2913c-144">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-144">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-145">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-145">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-146">71</span><span class="sxs-lookup"><span data-stu-id="2913c-146">71</span></span>

<span data-ttu-id="2913c-147">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-147">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-148">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="2913c-148">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-149">72</span><span class="sxs-lookup"><span data-stu-id="2913c-149">72</span></span>

<span data-ttu-id="2913c-150">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="2913c-150">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-151">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-151">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-152">73</span><span class="sxs-lookup"><span data-stu-id="2913c-152">73</span></span>

<span data-ttu-id="2913c-153">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-153">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-154">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-154">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-155">74</span><span class="sxs-lookup"><span data-stu-id="2913c-155">74</span></span>

<span data-ttu-id="2913c-156">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-156">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-157">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="2913c-157">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-158">75</span><span class="sxs-lookup"><span data-stu-id="2913c-158">75</span></span>

<span data-ttu-id="2913c-159">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="2913c-159">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-160">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-160">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-161">76</span><span class="sxs-lookup"><span data-stu-id="2913c-161">76</span></span>

<span data-ttu-id="2913c-162">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-162">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-163">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-163">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-164">77</span><span class="sxs-lookup"><span data-stu-id="2913c-164">77</span></span>

<span data-ttu-id="2913c-165">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-165">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-166">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="2913c-166">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-167">78</span><span class="sxs-lookup"><span data-stu-id="2913c-167">78</span></span>

<span data-ttu-id="2913c-168">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="2913c-168">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-169">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-169">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-170">79</span><span class="sxs-lookup"><span data-stu-id="2913c-170">79</span></span>

<span data-ttu-id="2913c-171">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-171">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-172">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="2913c-172">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-173">80</span><span class="sxs-lookup"><span data-stu-id="2913c-173">80</span></span>

<span data-ttu-id="2913c-174">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2913c-174">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-175">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="2913c-175">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-176">81</span><span class="sxs-lookup"><span data-stu-id="2913c-176">81</span></span>

<span data-ttu-id="2913c-177">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="2913c-177">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-178">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="2913c-178">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-179">82</span><span class="sxs-lookup"><span data-stu-id="2913c-179">82</span></span>

<span data-ttu-id="2913c-180">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="2913c-180">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-181">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="2913c-181">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-182">83</span><span class="sxs-lookup"><span data-stu-id="2913c-182">83</span></span>

<span data-ttu-id="2913c-183">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="2913c-183">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-184">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="2913c-184">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-185">84</span><span class="sxs-lookup"><span data-stu-id="2913c-185">84</span></span>

<span data-ttu-id="2913c-186">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="2913c-186">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-187">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="2913c-187">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-188">85 %</span><span class="sxs-lookup"><span data-stu-id="2913c-188">85</span></span>

<span data-ttu-id="2913c-189">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="2913c-189">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-190">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="2913c-190">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-191">86</span><span class="sxs-lookup"><span data-stu-id="2913c-191">86</span></span>

<span data-ttu-id="2913c-192">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="2913c-192">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-193">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-193">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-194">87</span><span class="sxs-lookup"><span data-stu-id="2913c-194">87</span></span>

<span data-ttu-id="2913c-195">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-195">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-196">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="2913c-196">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-197">88</span><span class="sxs-lookup"><span data-stu-id="2913c-197">88</span></span>

<span data-ttu-id="2913c-198">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="2913c-198">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-199">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="2913c-199">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-200">89</span><span class="sxs-lookup"><span data-stu-id="2913c-200">89</span></span>

<span data-ttu-id="2913c-201">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="2913c-201">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-202">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="2913c-202">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-203">90</span><span class="sxs-lookup"><span data-stu-id="2913c-203">90</span></span>

<span data-ttu-id="2913c-204">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="2913c-204">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-205">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="2913c-205">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-206">91</span><span class="sxs-lookup"><span data-stu-id="2913c-206">91</span></span>

<span data-ttu-id="2913c-207">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="2913c-207">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-208">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="2913c-208">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-209">92</span><span class="sxs-lookup"><span data-stu-id="2913c-209">92</span></span>

<span data-ttu-id="2913c-210">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="2913c-210">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-211">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="2913c-211">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-212">93</span><span class="sxs-lookup"><span data-stu-id="2913c-212">93</span></span>

<span data-ttu-id="2913c-213">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2913c-213">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-214">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="2913c-214">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-215">94</span><span class="sxs-lookup"><span data-stu-id="2913c-215">94</span></span>

<span data-ttu-id="2913c-216">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="2913c-216">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-217">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="2913c-217">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-218">95</span><span class="sxs-lookup"><span data-stu-id="2913c-218">95</span></span>

<span data-ttu-id="2913c-219">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="2913c-219">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-220">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="2913c-220">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-221">96</span><span class="sxs-lookup"><span data-stu-id="2913c-221">96</span></span>

<span data-ttu-id="2913c-222">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="2913c-222">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-223">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="2913c-223">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-224">97</span><span class="sxs-lookup"><span data-stu-id="2913c-224">97</span></span>

<span data-ttu-id="2913c-225">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="2913c-225">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-226">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="2913c-226">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-227">98</span><span class="sxs-lookup"><span data-stu-id="2913c-227">98</span></span>

<span data-ttu-id="2913c-228">Tous les baux DHCP ne peuvent pas être libérés ni renouvelés.</span><span class="sxs-lookup"><span data-stu-id="2913c-228">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-229">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="2913c-229">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-230">100</span><span class="sxs-lookup"><span data-stu-id="2913c-230">100</span></span>

<span data-ttu-id="2913c-231">DHCP n’est pas activé sur la carte.</span><span class="sxs-lookup"><span data-stu-id="2913c-231">DHCP is not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2913c-232">**Autres**</span><span class="sxs-lookup"><span data-stu-id="2913c-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2913c-233">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2913c-233">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2913c-234">Notes</span><span class="sxs-lookup"><span data-stu-id="2913c-234">Remarks</span></span>

<span data-ttu-id="2913c-235">L’unité MTU correspond à la taille maximale (en octets) du paquet qu’un transport transmet sur le réseau sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2913c-235">The MTU is the maximum packet size (in bytes) that a transport will transmit over the underlying network.</span></span> <span data-ttu-id="2913c-236">La taille comprend l’en-tête de transport.</span><span class="sxs-lookup"><span data-stu-id="2913c-236">The size includes the transport header.</span></span>

<span data-ttu-id="2913c-237">Notez qu’un datagramme IP peut s’étendre sur plusieurs paquets.</span><span class="sxs-lookup"><span data-stu-id="2913c-237">Note that an IP datagram can span multiple packets.</span></span> <span data-ttu-id="2913c-238">Les valeurs supérieures à la valeur par défaut pour le réseau sous-jacent entraînent le transport à l’aide de l’unité MTU par défaut du réseau.</span><span class="sxs-lookup"><span data-stu-id="2913c-238">Values larger than the default for the underlying network result in the transport using the network default MTU.</span></span> <span data-ttu-id="2913c-239">Les valeurs inférieures à 68 entraînent le transport à l’aide d’une valeur MTU de 68.</span><span class="sxs-lookup"><span data-stu-id="2913c-239">Values smaller than 68 result in the transport using an MTU of 68.</span></span>

## <a name="examples"></a><span data-ttu-id="2913c-240">Exemples</span><span class="sxs-lookup"><span data-stu-id="2913c-240">Examples</span></span>

<span data-ttu-id="2913c-241">L’exemple VBScript [de modification de l’unité MTU pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) configure l’unité de transmission maximale pour toutes les cartes réseau installées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2913c-241">The [Modify the MTU for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) VBScript sample configures the maximum transmission unit for all network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2913c-242">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2913c-242">Requirements</span></span>



| <span data-ttu-id="2913c-243">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2913c-243">Requirement</span></span> | <span data-ttu-id="2913c-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="2913c-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2913c-245">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2913c-245">Minimum supported client</span></span><br/> | <span data-ttu-id="2913c-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2913c-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2913c-247">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2913c-247">Minimum supported server</span></span><br/> | <span data-ttu-id="2913c-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2913c-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2913c-249">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2913c-249">Namespace</span></span><br/>                | <span data-ttu-id="2913c-250">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2913c-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2913c-251">MOF</span><span class="sxs-lookup"><span data-stu-id="2913c-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2913c-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2913c-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2913c-253">DLL</span><span class="sxs-lookup"><span data-stu-id="2913c-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2913c-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2913c-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2913c-255">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2913c-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2913c-256">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="2913c-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2913c-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="2913c-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2913c-258">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="2913c-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2913c-259">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="2913c-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2913c-260">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="2913c-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

