---
description: La méthode statique de la classe WMI SetDefaultTTL permet de définir la valeur de durée de vie (TTL) par défaut dans l’en-tête des paquets IP sortants.
ms.assetid: 74b060de-512c-407e-9f93-c3b496f8d09d
ms.tgt_platform: multiple
title: Méthode SetDefaultTTL de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTTL
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 253048b44a836f92646124fb972fe32c135e3b9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846969"
---
# <a name="setdefaultttl-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="892a3-103">Méthode SetDefaultTTL de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="892a3-103">SetDefaultTTL method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="892a3-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultTTL** permet de définir la valeur de durée de vie (TTL) par défaut dans l’en-tête des paquets IP sortants.</span><span class="sxs-lookup"><span data-stu-id="892a3-104">The **SetDefaultTTL** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span>

<span data-ttu-id="892a3-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="892a3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="892a3-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="892a3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="892a3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="892a3-107">Syntax</span></span>


```mof
uint32 SetDefaultTTL(
  [in] uint8 DefaultTTL
);
```



## <a name="parameters"></a><span data-ttu-id="892a3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="892a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="892a3-109">*DefaultTtl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="892a3-109">*DefaultTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="892a3-110">Valeur de durée de vie définie dans l’en-tête des paquets IP sortants.</span><span class="sxs-lookup"><span data-stu-id="892a3-110">Time to Live value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="892a3-111">La valeur par défaut est 32 ; Plage valide : 1-255</span><span class="sxs-lookup"><span data-stu-id="892a3-111">The default value is 32; Valid range: 1 - 255</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="892a3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="892a3-112">Return value</span></span>

<span data-ttu-id="892a3-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="892a3-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="892a3-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="892a3-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="892a3-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="892a3-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="892a3-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="892a3-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-117">0</span><span class="sxs-lookup"><span data-stu-id="892a3-117">0</span></span>

<span data-ttu-id="892a3-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="892a3-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="892a3-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-120">1</span><span class="sxs-lookup"><span data-stu-id="892a3-120">1</span></span>

<span data-ttu-id="892a3-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="892a3-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="892a3-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-123">64</span><span class="sxs-lookup"><span data-stu-id="892a3-123">64</span></span>

<span data-ttu-id="892a3-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="892a3-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="892a3-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-126">65</span><span class="sxs-lookup"><span data-stu-id="892a3-126">65</span></span>

<span data-ttu-id="892a3-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="892a3-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-129">66</span><span class="sxs-lookup"><span data-stu-id="892a3-129">66</span></span>

<span data-ttu-id="892a3-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="892a3-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-132">67</span><span class="sxs-lookup"><span data-stu-id="892a3-132">67</span></span>

<span data-ttu-id="892a3-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="892a3-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-135">68</span><span class="sxs-lookup"><span data-stu-id="892a3-135">68</span></span>

<span data-ttu-id="892a3-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="892a3-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-138">69</span><span class="sxs-lookup"><span data-stu-id="892a3-138">69</span></span>

<span data-ttu-id="892a3-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="892a3-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-141">70</span><span class="sxs-lookup"><span data-stu-id="892a3-141">70</span></span>

<span data-ttu-id="892a3-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-144">71</span><span class="sxs-lookup"><span data-stu-id="892a3-144">71</span></span>

<span data-ttu-id="892a3-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="892a3-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-147">72</span><span class="sxs-lookup"><span data-stu-id="892a3-147">72</span></span>

<span data-ttu-id="892a3-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="892a3-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-150">73</span><span class="sxs-lookup"><span data-stu-id="892a3-150">73</span></span>

<span data-ttu-id="892a3-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-153">74</span><span class="sxs-lookup"><span data-stu-id="892a3-153">74</span></span>

<span data-ttu-id="892a3-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="892a3-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-156">75</span><span class="sxs-lookup"><span data-stu-id="892a3-156">75</span></span>

<span data-ttu-id="892a3-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="892a3-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-159">76</span><span class="sxs-lookup"><span data-stu-id="892a3-159">76</span></span>

<span data-ttu-id="892a3-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-162">77</span><span class="sxs-lookup"><span data-stu-id="892a3-162">77</span></span>

<span data-ttu-id="892a3-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="892a3-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-165">78</span><span class="sxs-lookup"><span data-stu-id="892a3-165">78</span></span>

<span data-ttu-id="892a3-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="892a3-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-168">79</span><span class="sxs-lookup"><span data-stu-id="892a3-168">79</span></span>

<span data-ttu-id="892a3-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="892a3-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-171">80</span><span class="sxs-lookup"><span data-stu-id="892a3-171">80</span></span>

<span data-ttu-id="892a3-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="892a3-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="892a3-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-174">81</span><span class="sxs-lookup"><span data-stu-id="892a3-174">81</span></span>

<span data-ttu-id="892a3-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="892a3-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="892a3-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-177">82</span><span class="sxs-lookup"><span data-stu-id="892a3-177">82</span></span>

<span data-ttu-id="892a3-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="892a3-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="892a3-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-180">83</span><span class="sxs-lookup"><span data-stu-id="892a3-180">83</span></span>

<span data-ttu-id="892a3-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="892a3-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="892a3-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-183">84</span><span class="sxs-lookup"><span data-stu-id="892a3-183">84</span></span>

<span data-ttu-id="892a3-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="892a3-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="892a3-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-186">85 %</span><span class="sxs-lookup"><span data-stu-id="892a3-186">85</span></span>

<span data-ttu-id="892a3-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="892a3-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="892a3-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-189">86</span><span class="sxs-lookup"><span data-stu-id="892a3-189">86</span></span>

<span data-ttu-id="892a3-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="892a3-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-192">87</span><span class="sxs-lookup"><span data-stu-id="892a3-192">87</span></span>

<span data-ttu-id="892a3-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="892a3-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-195">88</span><span class="sxs-lookup"><span data-stu-id="892a3-195">88</span></span>

<span data-ttu-id="892a3-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="892a3-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="892a3-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-198">89</span><span class="sxs-lookup"><span data-stu-id="892a3-198">89</span></span>

<span data-ttu-id="892a3-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="892a3-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="892a3-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-201">90</span><span class="sxs-lookup"><span data-stu-id="892a3-201">90</span></span>

<span data-ttu-id="892a3-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="892a3-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="892a3-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-204">91</span><span class="sxs-lookup"><span data-stu-id="892a3-204">91</span></span>

<span data-ttu-id="892a3-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="892a3-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="892a3-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-207">92</span><span class="sxs-lookup"><span data-stu-id="892a3-207">92</span></span>

<span data-ttu-id="892a3-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="892a3-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="892a3-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-210">93</span><span class="sxs-lookup"><span data-stu-id="892a3-210">93</span></span>

<span data-ttu-id="892a3-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="892a3-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="892a3-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-213">94</span><span class="sxs-lookup"><span data-stu-id="892a3-213">94</span></span>

<span data-ttu-id="892a3-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="892a3-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="892a3-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-216">95</span><span class="sxs-lookup"><span data-stu-id="892a3-216">95</span></span>

<span data-ttu-id="892a3-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="892a3-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="892a3-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-219">96</span><span class="sxs-lookup"><span data-stu-id="892a3-219">96</span></span>

<span data-ttu-id="892a3-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="892a3-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="892a3-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-222">97</span><span class="sxs-lookup"><span data-stu-id="892a3-222">97</span></span>

<span data-ttu-id="892a3-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="892a3-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="892a3-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-225">98</span><span class="sxs-lookup"><span data-stu-id="892a3-225">98</span></span>

<span data-ttu-id="892a3-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="892a3-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="892a3-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-228">100</span><span class="sxs-lookup"><span data-stu-id="892a3-228">100</span></span>

<span data-ttu-id="892a3-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="892a3-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="892a3-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="892a3-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="892a3-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="892a3-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="892a3-232">Notes</span><span class="sxs-lookup"><span data-stu-id="892a3-232">Remarks</span></span>

<span data-ttu-id="892a3-233">La durée de vie spécifie le nombre de routeurs qu’un paquet IP peut traverser pour atteindre sa destination avant d’être ignoré.</span><span class="sxs-lookup"><span data-stu-id="892a3-233">The TTL specifies the number of routers an IP packet may pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="892a3-234">Chaque routeur décrémente le nombre de TTL d’un paquet d’un et rejette les paquets dont la durée de vie est égale à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="892a3-234">Each router decrements the TTL count of a packet by one and discards the packets with a TTL of 0 (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="892a3-235">Exemples</span><span class="sxs-lookup"><span data-stu-id="892a3-235">Examples</span></span>

<span data-ttu-id="892a3-236">L’exemple VBScript de [modification de la durée de vie par défaut pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) utilise **SetDefaultTTL** pour définir la valeur par défaut de la durée de vie dans l’en-tête des paquets IP sortants sur 64</span><span class="sxs-lookup"><span data-stu-id="892a3-236">The [Modify the Default Time-to-Live for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript sample uses **SetDefaultTTL** to set the default time-to-live value in the header of outgoing IP packets to 64</span></span>

## <a name="requirements"></a><span data-ttu-id="892a3-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="892a3-237">Requirements</span></span>



| <span data-ttu-id="892a3-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="892a3-238">Requirement</span></span> | <span data-ttu-id="892a3-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="892a3-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="892a3-240">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="892a3-240">Minimum supported client</span></span><br/> | <span data-ttu-id="892a3-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="892a3-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="892a3-242">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="892a3-242">Minimum supported server</span></span><br/> | <span data-ttu-id="892a3-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="892a3-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="892a3-244">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="892a3-244">Namespace</span></span><br/>                | <span data-ttu-id="892a3-245">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="892a3-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="892a3-246">MOF</span><span class="sxs-lookup"><span data-stu-id="892a3-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="892a3-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="892a3-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="892a3-248">DLL</span><span class="sxs-lookup"><span data-stu-id="892a3-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="892a3-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="892a3-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="892a3-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="892a3-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="892a3-251">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="892a3-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="892a3-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="892a3-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="892a3-253">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="892a3-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="892a3-254">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="892a3-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="892a3-255">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="892a3-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

