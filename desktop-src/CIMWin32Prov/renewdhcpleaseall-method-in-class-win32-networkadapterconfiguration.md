---
description: La méthode statique de la classe WMI RenewDHCPLeaseAll renouvelle les adresses IP sur toutes les cartes réseau compatibles DHCP.
ms.assetid: cbe0a607-cb3b-47c4-ad3a-c4fa03fe688c
ms.tgt_platform: multiple
title: Méthode RenewDHCPLeaseAll de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3ed94b44a629f619617186415ed3822387c6967
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536318"
---
# <a name="renewdhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d48e8-103">Méthode RenewDHCPLeaseAll de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="d48e8-103">RenewDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d48e8-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenewDHCPLeaseAll** renouvelle les adresses IP sur toutes les cartes réseau compatibles DHCP.</span><span class="sxs-lookup"><span data-stu-id="d48e8-104">The **RenewDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method renews the IP addresses on all DHCP-enabled network adapters.</span></span>

<span data-ttu-id="d48e8-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d48e8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d48e8-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d48e8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d48e8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d48e8-107">Syntax</span></span>


```mof
uint32 RenewDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="d48e8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d48e8-108">Parameters</span></span>

<span data-ttu-id="d48e8-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d48e8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d48e8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d48e8-110">Return value</span></span>

<span data-ttu-id="d48e8-111">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d48e8-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="d48e8-112">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d48e8-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d48e8-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d48e8-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d48e8-114">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="d48e8-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-115">0</span><span class="sxs-lookup"><span data-stu-id="d48e8-115">0</span></span>

<span data-ttu-id="d48e8-116">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d48e8-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-117">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="d48e8-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-118">1</span><span class="sxs-lookup"><span data-stu-id="d48e8-118">1</span></span>

<span data-ttu-id="d48e8-119">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="d48e8-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-120">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="d48e8-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-121">64</span><span class="sxs-lookup"><span data-stu-id="d48e8-121">64</span></span>

<span data-ttu-id="d48e8-122">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="d48e8-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-123">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="d48e8-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-124">65</span><span class="sxs-lookup"><span data-stu-id="d48e8-124">65</span></span>

<span data-ttu-id="d48e8-125">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="d48e8-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-126">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-127">66</span><span class="sxs-lookup"><span data-stu-id="d48e8-127">66</span></span>

<span data-ttu-id="d48e8-128">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-129">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="d48e8-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-130">67</span><span class="sxs-lookup"><span data-stu-id="d48e8-130">67</span></span>

<span data-ttu-id="d48e8-131">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="d48e8-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-132">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-133">68</span><span class="sxs-lookup"><span data-stu-id="d48e8-133">68</span></span>

<span data-ttu-id="d48e8-134">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-135">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="d48e8-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-136">69</span><span class="sxs-lookup"><span data-stu-id="d48e8-136">69</span></span>

<span data-ttu-id="d48e8-137">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d48e8-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-138">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-139">70</span><span class="sxs-lookup"><span data-stu-id="d48e8-139">70</span></span>

<span data-ttu-id="d48e8-140">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-141">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-142">71</span><span class="sxs-lookup"><span data-stu-id="d48e8-142">71</span></span>

<span data-ttu-id="d48e8-143">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-144">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="d48e8-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-145">72</span><span class="sxs-lookup"><span data-stu-id="d48e8-145">72</span></span>

<span data-ttu-id="d48e8-146">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="d48e8-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-147">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-148">73</span><span class="sxs-lookup"><span data-stu-id="d48e8-148">73</span></span>

<span data-ttu-id="d48e8-149">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-150">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-151">74</span><span class="sxs-lookup"><span data-stu-id="d48e8-151">74</span></span>

<span data-ttu-id="d48e8-152">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-153">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="d48e8-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-154">75</span><span class="sxs-lookup"><span data-stu-id="d48e8-154">75</span></span>

<span data-ttu-id="d48e8-155">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="d48e8-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-156">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-157">76</span><span class="sxs-lookup"><span data-stu-id="d48e8-157">76</span></span>

<span data-ttu-id="d48e8-158">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-159">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-160">77</span><span class="sxs-lookup"><span data-stu-id="d48e8-160">77</span></span>

<span data-ttu-id="d48e8-161">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-162">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="d48e8-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-163">78</span><span class="sxs-lookup"><span data-stu-id="d48e8-163">78</span></span>

<span data-ttu-id="d48e8-164">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="d48e8-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-165">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-166">79</span><span class="sxs-lookup"><span data-stu-id="d48e8-166">79</span></span>

<span data-ttu-id="d48e8-167">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-168">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="d48e8-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-169">80</span><span class="sxs-lookup"><span data-stu-id="d48e8-169">80</span></span>

<span data-ttu-id="d48e8-170">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d48e8-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-171">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="d48e8-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-172">81</span><span class="sxs-lookup"><span data-stu-id="d48e8-172">81</span></span>

<span data-ttu-id="d48e8-173">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="d48e8-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-174">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="d48e8-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-175">82</span><span class="sxs-lookup"><span data-stu-id="d48e8-175">82</span></span>

<span data-ttu-id="d48e8-176">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="d48e8-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-177">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="d48e8-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-178">83</span><span class="sxs-lookup"><span data-stu-id="d48e8-178">83</span></span>

<span data-ttu-id="d48e8-179">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="d48e8-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-180">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="d48e8-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-181">84</span><span class="sxs-lookup"><span data-stu-id="d48e8-181">84</span></span>

<span data-ttu-id="d48e8-182">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d48e8-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-183">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="d48e8-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-184">85 %</span><span class="sxs-lookup"><span data-stu-id="d48e8-184">85</span></span>

<span data-ttu-id="d48e8-185">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d48e8-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-186">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="d48e8-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-187">86</span><span class="sxs-lookup"><span data-stu-id="d48e8-187">86</span></span>

<span data-ttu-id="d48e8-188">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="d48e8-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-189">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-190">87</span><span class="sxs-lookup"><span data-stu-id="d48e8-190">87</span></span>

<span data-ttu-id="d48e8-191">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-192">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="d48e8-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-193">88</span><span class="sxs-lookup"><span data-stu-id="d48e8-193">88</span></span>

<span data-ttu-id="d48e8-194">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="d48e8-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-195">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="d48e8-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-196">89</span><span class="sxs-lookup"><span data-stu-id="d48e8-196">89</span></span>

<span data-ttu-id="d48e8-197">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="d48e8-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-198">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="d48e8-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-199">90</span><span class="sxs-lookup"><span data-stu-id="d48e8-199">90</span></span>

<span data-ttu-id="d48e8-200">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="d48e8-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-201">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="d48e8-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-202">91</span><span class="sxs-lookup"><span data-stu-id="d48e8-202">91</span></span>

<span data-ttu-id="d48e8-203">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="d48e8-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-204">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="d48e8-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-205">92</span><span class="sxs-lookup"><span data-stu-id="d48e8-205">92</span></span>

<span data-ttu-id="d48e8-206">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d48e8-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-207">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="d48e8-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-208">93</span><span class="sxs-lookup"><span data-stu-id="d48e8-208">93</span></span>

<span data-ttu-id="d48e8-209">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d48e8-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-210">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="d48e8-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-211">94</span><span class="sxs-lookup"><span data-stu-id="d48e8-211">94</span></span>

<span data-ttu-id="d48e8-212">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="d48e8-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-213">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="d48e8-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-214">95</span><span class="sxs-lookup"><span data-stu-id="d48e8-214">95</span></span>

<span data-ttu-id="d48e8-215">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="d48e8-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-216">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="d48e8-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-217">96</span><span class="sxs-lookup"><span data-stu-id="d48e8-217">96</span></span>

<span data-ttu-id="d48e8-218">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="d48e8-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-219">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="d48e8-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-220">97</span><span class="sxs-lookup"><span data-stu-id="d48e8-220">97</span></span>

<span data-ttu-id="d48e8-221">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="d48e8-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-222">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="d48e8-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-223">98</span><span class="sxs-lookup"><span data-stu-id="d48e8-223">98</span></span>

<span data-ttu-id="d48e8-224">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="d48e8-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-225">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="d48e8-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-226">100</span><span class="sxs-lookup"><span data-stu-id="d48e8-226">100</span></span>

<span data-ttu-id="d48e8-227">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d48e8-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d48e8-228">**Autres**</span><span class="sxs-lookup"><span data-stu-id="d48e8-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d48e8-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d48e8-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d48e8-230">Notes</span><span class="sxs-lookup"><span data-stu-id="d48e8-230">Remarks</span></span>

<span data-ttu-id="d48e8-231">Le bail de l’adresse IP attribuée par un serveur DHCP a une date d’expiration que le client doit renouveler s’il a l’intention de continuer à utiliser l’adresse IP attribuée.</span><span class="sxs-lookup"><span data-stu-id="d48e8-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="d48e8-232">Exemples</span><span class="sxs-lookup"><span data-stu-id="d48e8-232">Examples</span></span>

<span data-ttu-id="d48e8-233">L’exemple de [renouvellement de tous les baux DHCP](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) dans la Galerie TechNet renouvelle tous les baux DHCP en cours d’utilisation sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d48e8-233">The [Renew All DHCP Leases](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) VBScript example on TechNet Gallery renews all the DHCP leases currently in use on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d48e8-234">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d48e8-234">Requirements</span></span>



| <span data-ttu-id="d48e8-235">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d48e8-235">Requirement</span></span> | <span data-ttu-id="d48e8-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="d48e8-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d48e8-237">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d48e8-237">Minimum supported client</span></span><br/> | <span data-ttu-id="d48e8-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d48e8-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d48e8-239">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d48e8-239">Minimum supported server</span></span><br/> | <span data-ttu-id="d48e8-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d48e8-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d48e8-241">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d48e8-241">Namespace</span></span><br/>                | <span data-ttu-id="d48e8-242">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d48e8-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d48e8-243">MOF</span><span class="sxs-lookup"><span data-stu-id="d48e8-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d48e8-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d48e8-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d48e8-245">DLL</span><span class="sxs-lookup"><span data-stu-id="d48e8-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48e8-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48e8-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48e8-247">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d48e8-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48e8-248">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="d48e8-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d48e8-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="d48e8-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d48e8-250">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="d48e8-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d48e8-251">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="d48e8-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d48e8-252">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="d48e8-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

