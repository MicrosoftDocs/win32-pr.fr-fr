---
description: La méthode statique de la classe WMI SetIPUseZeroBroadcast est utilisée pour définir l’utilisation de la diffusion à zéro IP.
ms.assetid: d20ac6fc-a5d5-4ad9-a2a5-65142b4c7d02
ms.tgt_platform: multiple
title: Méthode SetIPUseZeroBroadcast de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPUseZeroBroadcast
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 564f122242407f4d6f5dd28da9fd4d151ab6b47f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110947"
---
# <a name="setipusezerobroadcast-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="3fa4f-103">Méthode SetIPUseZeroBroadcast de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fa4f-103">SetIPUseZeroBroadcast method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="3fa4f-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetIPUseZeroBroadcast** est utilisée pour définir l’utilisation de la diffusion à zéro IP.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-104">The **SetIPUseZeroBroadcast** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set IP zero broadcast usage.</span></span>

<span data-ttu-id="3fa4f-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3fa4f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3fa4f-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3fa4f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa4f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fa4f-107">Syntax</span></span>


```mof
uint32 SetIPUseZeroBroadcast(
  [in] boolean IPUseZeroBroadcast
);
```



## <a name="parameters"></a><span data-ttu-id="3fa4f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fa4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fa4f-109">*IPUseZeroBroadcast* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fa4f-109">*IPUseZeroBroadcast* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-110">Si la **valeur est true**, la diffusion de zéro IP est utilisée.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-110">If **true**, IP zero broadcast is used.</span></span> <span data-ttu-id="3fa4f-111">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-111">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fa4f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fa4f-112">Return value</span></span>

<span data-ttu-id="3fa4f-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="3fa4f-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3fa4f-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3fa4f-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3fa4f-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3fa4f-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-117">0</span><span class="sxs-lookup"><span data-stu-id="3fa4f-117">0</span></span>

<span data-ttu-id="3fa4f-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-120">1</span><span class="sxs-lookup"><span data-stu-id="3fa4f-120">1</span></span>

<span data-ttu-id="3fa4f-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-123">64</span><span class="sxs-lookup"><span data-stu-id="3fa4f-123">64</span></span>

<span data-ttu-id="3fa4f-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-126">65</span><span class="sxs-lookup"><span data-stu-id="3fa4f-126">65</span></span>

<span data-ttu-id="3fa4f-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-129">66</span><span class="sxs-lookup"><span data-stu-id="3fa4f-129">66</span></span>

<span data-ttu-id="3fa4f-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-132">67</span><span class="sxs-lookup"><span data-stu-id="3fa4f-132">67</span></span>

<span data-ttu-id="3fa4f-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-135">68</span><span class="sxs-lookup"><span data-stu-id="3fa4f-135">68</span></span>

<span data-ttu-id="3fa4f-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-138">69</span><span class="sxs-lookup"><span data-stu-id="3fa4f-138">69</span></span>

<span data-ttu-id="3fa4f-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-141">70</span><span class="sxs-lookup"><span data-stu-id="3fa4f-141">70</span></span>

<span data-ttu-id="3fa4f-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-144">71</span><span class="sxs-lookup"><span data-stu-id="3fa4f-144">71</span></span>

<span data-ttu-id="3fa4f-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-147">72</span><span class="sxs-lookup"><span data-stu-id="3fa4f-147">72</span></span>

<span data-ttu-id="3fa4f-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-150">73</span><span class="sxs-lookup"><span data-stu-id="3fa4f-150">73</span></span>

<span data-ttu-id="3fa4f-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-153">74</span><span class="sxs-lookup"><span data-stu-id="3fa4f-153">74</span></span>

<span data-ttu-id="3fa4f-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-156">75</span><span class="sxs-lookup"><span data-stu-id="3fa4f-156">75</span></span>

<span data-ttu-id="3fa4f-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-159">76</span><span class="sxs-lookup"><span data-stu-id="3fa4f-159">76</span></span>

<span data-ttu-id="3fa4f-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-162">77</span><span class="sxs-lookup"><span data-stu-id="3fa4f-162">77</span></span>

<span data-ttu-id="3fa4f-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-165">78</span><span class="sxs-lookup"><span data-stu-id="3fa4f-165">78</span></span>

<span data-ttu-id="3fa4f-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-168">79</span><span class="sxs-lookup"><span data-stu-id="3fa4f-168">79</span></span>

<span data-ttu-id="3fa4f-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-171">80</span><span class="sxs-lookup"><span data-stu-id="3fa4f-171">80</span></span>

<span data-ttu-id="3fa4f-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-174">81</span><span class="sxs-lookup"><span data-stu-id="3fa4f-174">81</span></span>

<span data-ttu-id="3fa4f-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-177">82</span><span class="sxs-lookup"><span data-stu-id="3fa4f-177">82</span></span>

<span data-ttu-id="3fa4f-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-180">83</span><span class="sxs-lookup"><span data-stu-id="3fa4f-180">83</span></span>

<span data-ttu-id="3fa4f-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-183">84</span><span class="sxs-lookup"><span data-stu-id="3fa4f-183">84</span></span>

<span data-ttu-id="3fa4f-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-186">85 %</span><span class="sxs-lookup"><span data-stu-id="3fa4f-186">85</span></span>

<span data-ttu-id="3fa4f-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-189">86</span><span class="sxs-lookup"><span data-stu-id="3fa4f-189">86</span></span>

<span data-ttu-id="3fa4f-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-192">87</span><span class="sxs-lookup"><span data-stu-id="3fa4f-192">87</span></span>

<span data-ttu-id="3fa4f-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-195">88</span><span class="sxs-lookup"><span data-stu-id="3fa4f-195">88</span></span>

<span data-ttu-id="3fa4f-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-198">89</span><span class="sxs-lookup"><span data-stu-id="3fa4f-198">89</span></span>

<span data-ttu-id="3fa4f-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-201">90</span><span class="sxs-lookup"><span data-stu-id="3fa4f-201">90</span></span>

<span data-ttu-id="3fa4f-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-204">91</span><span class="sxs-lookup"><span data-stu-id="3fa4f-204">91</span></span>

<span data-ttu-id="3fa4f-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-207">92</span><span class="sxs-lookup"><span data-stu-id="3fa4f-207">92</span></span>

<span data-ttu-id="3fa4f-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-210">93</span><span class="sxs-lookup"><span data-stu-id="3fa4f-210">93</span></span>

<span data-ttu-id="3fa4f-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-213">94</span><span class="sxs-lookup"><span data-stu-id="3fa4f-213">94</span></span>

<span data-ttu-id="3fa4f-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-216">95</span><span class="sxs-lookup"><span data-stu-id="3fa4f-216">95</span></span>

<span data-ttu-id="3fa4f-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-219">96</span><span class="sxs-lookup"><span data-stu-id="3fa4f-219">96</span></span>

<span data-ttu-id="3fa4f-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-222">97</span><span class="sxs-lookup"><span data-stu-id="3fa4f-222">97</span></span>

<span data-ttu-id="3fa4f-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-225">98</span><span class="sxs-lookup"><span data-stu-id="3fa4f-225">98</span></span>

<span data-ttu-id="3fa4f-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-228">100</span><span class="sxs-lookup"><span data-stu-id="3fa4f-228">100</span></span>

<span data-ttu-id="3fa4f-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3fa4f-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3fa4f-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="3fa4f-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fa4f-232">Notes</span><span class="sxs-lookup"><span data-stu-id="3fa4f-232">Remarks</span></span>

<span data-ttu-id="3fa4f-233">Si le paramètre *IPUseZeroBroadcast* est défini sur **true**, l’adresse IP utilise des diffusions sans diffusion (0.0.0.0) au lieu de diffusions unidirectionnelles (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="3fa4f-233">If the *IPUseZeroBroadcast* parameter is set to **TRUE**, then IP will use zero-broadcasts (0.0.0.0) instead of one-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="3fa4f-234">La plupart des systèmes utilisent une seule diffusion, mais les systèmes dérivés des implémentations BSD utilisent des diffusions sans diffusion.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-234">Most systems use one-broadcasts, but systems derived from BSD implementations use zero-broadcasts.</span></span> <span data-ttu-id="3fa4f-235">Les systèmes qui utilisent des diffusions différentes n’interagissent pas sur le même réseau.</span><span class="sxs-lookup"><span data-stu-id="3fa4f-235">Systems that use different broadcasts will not interoperate on the same network.</span></span>

## <a name="examples"></a><span data-ttu-id="3fa4f-236">Exemples</span><span class="sxs-lookup"><span data-stu-id="3fa4f-236">Examples</span></span>

<span data-ttu-id="3fa4f-237">L’exemple VBScript [modifier Zero-Broadcast utiliser pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) configure un ordinateur pour qu’il utilise des diffusions sans diffusion (0.0.0.0) au lieu d’une diffusion (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="3fa4f-237">The [Modify Zero-Broadcast Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript sample configures a computer to use zero-broadcasts (0.0.0.0) rather than one-broadcasts (255.255.255.255).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa4f-238">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fa4f-238">Requirements</span></span>



| <span data-ttu-id="3fa4f-239">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fa4f-239">Requirement</span></span> | <span data-ttu-id="3fa4f-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fa4f-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa4f-241">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fa4f-241">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa4f-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fa4f-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3fa4f-243">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fa4f-243">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa4f-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fa4f-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3fa4f-245">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3fa4f-245">Namespace</span></span><br/>                | <span data-ttu-id="3fa4f-246">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3fa4f-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3fa4f-247">MOF</span><span class="sxs-lookup"><span data-stu-id="3fa4f-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fa4f-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fa4f-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fa4f-249">DLL</span><span class="sxs-lookup"><span data-stu-id="3fa4f-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fa4f-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fa4f-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fa4f-251">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fa4f-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa4f-252">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="3fa4f-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3fa4f-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="3fa4f-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="3fa4f-254">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="3fa4f-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="3fa4f-255">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="3fa4f-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="3fa4f-256">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="3fa4f-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

