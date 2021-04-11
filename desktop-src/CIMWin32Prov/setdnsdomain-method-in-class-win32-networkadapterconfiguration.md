---
description: La méthode de classe WMI SetDNSDomain permet de définir le domaine DNS.
ms.assetid: a531133e-1b7c-4d85-979d-63bf4f7c9bed
ms.tgt_platform: multiple
title: Méthode SetDNSDomain de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSDomain
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c440d8cb5c720bf6922707f04bc75e2383755c1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201088"
---
# <a name="setdnsdomain-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="29fbf-103">Méthode SetDNSDomain de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="29fbf-103">SetDNSDomain method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="29fbf-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSDomain** permet de définir le domaine DNS.</span><span class="sxs-lookup"><span data-stu-id="29fbf-104">The **SetDNSDomain** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows for the setting of the DNS domain.</span></span>

<span data-ttu-id="29fbf-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="29fbf-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="29fbf-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="29fbf-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="29fbf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29fbf-107">Syntax</span></span>


```mof
uint32 SetDNSDomain(
  [in] string DNSDomain
);
```



## <a name="parameters"></a><span data-ttu-id="29fbf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29fbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29fbf-109">*Dnsdomain* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29fbf-109">*DNSDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-110">Domaine auquel le DNS est associé, représenté par un nom d’organisation suivi d’un point et d’une extension qui indique le type d’organisation.</span><span class="sxs-lookup"><span data-stu-id="29fbf-110">Domain with which the DNS is associated, represented by an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="29fbf-111">Exemple : « microsoft.com »</span><span class="sxs-lookup"><span data-stu-id="29fbf-111">Example: "microsoft.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29fbf-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29fbf-112">Return value</span></span>

<span data-ttu-id="29fbf-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="29fbf-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required and a different number if there is an error.</span></span> <span data-ttu-id="29fbf-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="29fbf-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="29fbf-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="29fbf-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="29fbf-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="29fbf-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-117">0</span><span class="sxs-lookup"><span data-stu-id="29fbf-117">0</span></span>

<span data-ttu-id="29fbf-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="29fbf-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="29fbf-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-120">1</span><span class="sxs-lookup"><span data-stu-id="29fbf-120">1</span></span>

<span data-ttu-id="29fbf-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="29fbf-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="29fbf-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-123">64</span><span class="sxs-lookup"><span data-stu-id="29fbf-123">64</span></span>

<span data-ttu-id="29fbf-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="29fbf-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="29fbf-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-126">65</span><span class="sxs-lookup"><span data-stu-id="29fbf-126">65</span></span>

<span data-ttu-id="29fbf-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="29fbf-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-129">66</span><span class="sxs-lookup"><span data-stu-id="29fbf-129">66</span></span>

<span data-ttu-id="29fbf-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="29fbf-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-132">67</span><span class="sxs-lookup"><span data-stu-id="29fbf-132">67</span></span>

<span data-ttu-id="29fbf-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="29fbf-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-135">68</span><span class="sxs-lookup"><span data-stu-id="29fbf-135">68</span></span>

<span data-ttu-id="29fbf-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="29fbf-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-138">69</span><span class="sxs-lookup"><span data-stu-id="29fbf-138">69</span></span>

<span data-ttu-id="29fbf-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="29fbf-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-141">70</span><span class="sxs-lookup"><span data-stu-id="29fbf-141">70</span></span>

<span data-ttu-id="29fbf-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-144">71</span><span class="sxs-lookup"><span data-stu-id="29fbf-144">71</span></span>

<span data-ttu-id="29fbf-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="29fbf-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-147">72</span><span class="sxs-lookup"><span data-stu-id="29fbf-147">72</span></span>

<span data-ttu-id="29fbf-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="29fbf-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-150">73</span><span class="sxs-lookup"><span data-stu-id="29fbf-150">73</span></span>

<span data-ttu-id="29fbf-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-153">74</span><span class="sxs-lookup"><span data-stu-id="29fbf-153">74</span></span>

<span data-ttu-id="29fbf-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="29fbf-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-156">75</span><span class="sxs-lookup"><span data-stu-id="29fbf-156">75</span></span>

<span data-ttu-id="29fbf-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="29fbf-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-159">76</span><span class="sxs-lookup"><span data-stu-id="29fbf-159">76</span></span>

<span data-ttu-id="29fbf-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-162">77</span><span class="sxs-lookup"><span data-stu-id="29fbf-162">77</span></span>

<span data-ttu-id="29fbf-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="29fbf-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-165">78</span><span class="sxs-lookup"><span data-stu-id="29fbf-165">78</span></span>

<span data-ttu-id="29fbf-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="29fbf-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-168">79</span><span class="sxs-lookup"><span data-stu-id="29fbf-168">79</span></span>

<span data-ttu-id="29fbf-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="29fbf-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-171">80</span><span class="sxs-lookup"><span data-stu-id="29fbf-171">80</span></span>

<span data-ttu-id="29fbf-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="29fbf-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="29fbf-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-174">81</span><span class="sxs-lookup"><span data-stu-id="29fbf-174">81</span></span>

<span data-ttu-id="29fbf-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="29fbf-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="29fbf-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-177">82</span><span class="sxs-lookup"><span data-stu-id="29fbf-177">82</span></span>

<span data-ttu-id="29fbf-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="29fbf-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="29fbf-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-180">83</span><span class="sxs-lookup"><span data-stu-id="29fbf-180">83</span></span>

<span data-ttu-id="29fbf-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="29fbf-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="29fbf-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-183">84</span><span class="sxs-lookup"><span data-stu-id="29fbf-183">84</span></span>

<span data-ttu-id="29fbf-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="29fbf-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="29fbf-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-186">85 %</span><span class="sxs-lookup"><span data-stu-id="29fbf-186">85</span></span>

<span data-ttu-id="29fbf-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="29fbf-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="29fbf-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-189">86</span><span class="sxs-lookup"><span data-stu-id="29fbf-189">86</span></span>

<span data-ttu-id="29fbf-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="29fbf-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-192">87</span><span class="sxs-lookup"><span data-stu-id="29fbf-192">87</span></span>

<span data-ttu-id="29fbf-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="29fbf-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-195">88</span><span class="sxs-lookup"><span data-stu-id="29fbf-195">88</span></span>

<span data-ttu-id="29fbf-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="29fbf-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="29fbf-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-198">89</span><span class="sxs-lookup"><span data-stu-id="29fbf-198">89</span></span>

<span data-ttu-id="29fbf-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="29fbf-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="29fbf-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-201">90</span><span class="sxs-lookup"><span data-stu-id="29fbf-201">90</span></span>

<span data-ttu-id="29fbf-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="29fbf-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="29fbf-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-204">91</span><span class="sxs-lookup"><span data-stu-id="29fbf-204">91</span></span>

<span data-ttu-id="29fbf-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="29fbf-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="29fbf-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-207">92</span><span class="sxs-lookup"><span data-stu-id="29fbf-207">92</span></span>

<span data-ttu-id="29fbf-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="29fbf-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="29fbf-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-210">93</span><span class="sxs-lookup"><span data-stu-id="29fbf-210">93</span></span>

<span data-ttu-id="29fbf-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="29fbf-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="29fbf-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-213">94</span><span class="sxs-lookup"><span data-stu-id="29fbf-213">94</span></span>

<span data-ttu-id="29fbf-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="29fbf-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="29fbf-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-216">95</span><span class="sxs-lookup"><span data-stu-id="29fbf-216">95</span></span>

<span data-ttu-id="29fbf-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="29fbf-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="29fbf-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-219">96</span><span class="sxs-lookup"><span data-stu-id="29fbf-219">96</span></span>

<span data-ttu-id="29fbf-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="29fbf-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="29fbf-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-222">97</span><span class="sxs-lookup"><span data-stu-id="29fbf-222">97</span></span>

<span data-ttu-id="29fbf-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="29fbf-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="29fbf-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-225">98</span><span class="sxs-lookup"><span data-stu-id="29fbf-225">98</span></span>

<span data-ttu-id="29fbf-226">Tous les baux DHCP ne peuvent pas être libérés ni renouvelés.</span><span class="sxs-lookup"><span data-stu-id="29fbf-226">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="29fbf-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-228">100</span><span class="sxs-lookup"><span data-stu-id="29fbf-228">100</span></span>

<span data-ttu-id="29fbf-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="29fbf-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="29fbf-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="29fbf-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="29fbf-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="29fbf-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29fbf-232">Notes</span><span class="sxs-lookup"><span data-stu-id="29fbf-232">Remarks</span></span>

<span data-ttu-id="29fbf-233">Il s’agit d’un appel de méthode dépendant de l’instance qui s’applique sur la base de chaque adaptateur.</span><span class="sxs-lookup"><span data-stu-id="29fbf-233">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="29fbf-234">Le paramètre s’applique à l’adaptateur ciblé.</span><span class="sxs-lookup"><span data-stu-id="29fbf-234">The setting applies to the targeted adapter.</span></span>

## <a name="examples"></a><span data-ttu-id="29fbf-235">Exemples</span><span class="sxs-lookup"><span data-stu-id="29fbf-235">Examples</span></span>

<span data-ttu-id="29fbf-236">L’exemple de code [attribuer le domaine DNS pour une carte réseau](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript dans la Galerie TechNet utilise **SetDNSDomain** pour définir le domaine DNS pour une carte réseau TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="29fbf-236">The [Assign the DNS Domain for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript code sample on TechNet gallery uses **SetDNSDomain** to set the DNS domain for a TCP/IP-bound network adapter.</span></span>

<span data-ttu-id="29fbf-237">L’exemple de code [modifier la configuration TCP/IP pour un ordinateur](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript dans la Galerie TechNet utilise **SetDNSDomain** pour modifier les paramètres TCP/IP d’une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="29fbf-237">The [Modify the TCP/IP Configuration for a Computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript code sample on TechNet Gallery uses **SetDNSDomain** to modify TCP/IP settings for a network adapter.</span></span>

<span data-ttu-id="29fbf-238">L’exemple d' [activation de paramètres DHCP sur un ordinateur](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) en VBScript sur la Galerie TechNet utilise **SetDNSDomain** pour configurer tous les paramètres généralement requis pour activer DHCP sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="29fbf-238">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample on TechNet Gallery uses **SetDNSDomain** to configure all the settings typically required to enable DHCP on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="29fbf-239">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29fbf-239">Requirements</span></span>



| <span data-ttu-id="29fbf-240">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29fbf-240">Requirement</span></span> | <span data-ttu-id="29fbf-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="29fbf-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29fbf-242">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29fbf-242">Minimum supported client</span></span><br/> | <span data-ttu-id="29fbf-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29fbf-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29fbf-244">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29fbf-244">Minimum supported server</span></span><br/> | <span data-ttu-id="29fbf-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29fbf-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29fbf-246">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29fbf-246">Namespace</span></span><br/>                | <span data-ttu-id="29fbf-247">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="29fbf-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="29fbf-248">MOF</span><span class="sxs-lookup"><span data-stu-id="29fbf-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29fbf-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29fbf-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="29fbf-250">DLL</span><span class="sxs-lookup"><span data-stu-id="29fbf-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29fbf-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29fbf-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29fbf-252">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29fbf-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29fbf-253">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="29fbf-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="29fbf-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="29fbf-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="29fbf-255">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="29fbf-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="29fbf-256">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="29fbf-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="29fbf-257">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="29fbf-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

