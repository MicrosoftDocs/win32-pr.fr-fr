---
description: La méthode statique de la classe WMI ReleaseDHCPLeaseAll libère les adresses IP liées à toutes les cartes réseau compatibles DHCP.
ms.assetid: d9f83953-f3da-419d-8c84-649c39b4945e
ms.tgt_platform: multiple
title: Méthode ReleaseDHCPLeaseAll de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e7b1f7cf2f09fa20f7bf19b15e82f536ca0aa50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543444"
---
# <a name="releasedhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="12e77-103">Méthode ReleaseDHCPLeaseAll de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="12e77-103">ReleaseDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="12e77-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ReleaseDHCPLeaseAll** libère les adresses IP liées à toutes les cartes réseau compatibles DHCP.</span><span class="sxs-lookup"><span data-stu-id="12e77-104">The **ReleaseDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method releases the IP addresses bound to all DHCP-enabled network adapters.</span></span>

> [!Note]  
> <span data-ttu-id="12e77-105">AVERTISSEMENT Si le protocole DHCP est activé sur le système de l’ordinateur local, l’option met fin à toutes les connexions TCP/IP DHCP.</span><span class="sxs-lookup"><span data-stu-id="12e77-105">Warning If DHCP is enabled on the local computer system, the option will terminate all DHCP TCP/IP connections.</span></span>

 

<span data-ttu-id="12e77-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="12e77-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="12e77-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="12e77-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="12e77-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12e77-108">Syntax</span></span>


```mof
uint32 ReleaseDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="12e77-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12e77-109">Parameters</span></span>

<span data-ttu-id="12e77-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="12e77-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12e77-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12e77-111">Return value</span></span>

<span data-ttu-id="12e77-112">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="12e77-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="12e77-113">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="12e77-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="12e77-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="12e77-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="12e77-115">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="12e77-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-116">0</span><span class="sxs-lookup"><span data-stu-id="12e77-116">0</span></span>

<span data-ttu-id="12e77-117">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="12e77-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-118">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="12e77-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-119">1</span><span class="sxs-lookup"><span data-stu-id="12e77-119">1</span></span>

<span data-ttu-id="12e77-120">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="12e77-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-121">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="12e77-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-122">64</span><span class="sxs-lookup"><span data-stu-id="12e77-122">64</span></span>

<span data-ttu-id="12e77-123">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="12e77-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-124">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="12e77-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-125">65</span><span class="sxs-lookup"><span data-stu-id="12e77-125">65</span></span>

<span data-ttu-id="12e77-126">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="12e77-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-127">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-128">66</span><span class="sxs-lookup"><span data-stu-id="12e77-128">66</span></span>

<span data-ttu-id="12e77-129">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-130">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="12e77-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-131">67</span><span class="sxs-lookup"><span data-stu-id="12e77-131">67</span></span>

<span data-ttu-id="12e77-132">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="12e77-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-133">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-134">68</span><span class="sxs-lookup"><span data-stu-id="12e77-134">68</span></span>

<span data-ttu-id="12e77-135">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-136">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="12e77-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-137">69</span><span class="sxs-lookup"><span data-stu-id="12e77-137">69</span></span>

<span data-ttu-id="12e77-138">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="12e77-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-139">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-140">70</span><span class="sxs-lookup"><span data-stu-id="12e77-140">70</span></span>

<span data-ttu-id="12e77-141">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-142">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-143">71</span><span class="sxs-lookup"><span data-stu-id="12e77-143">71</span></span>

<span data-ttu-id="12e77-144">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-145">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="12e77-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-146">72</span><span class="sxs-lookup"><span data-stu-id="12e77-146">72</span></span>

<span data-ttu-id="12e77-147">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="12e77-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-148">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-149">73</span><span class="sxs-lookup"><span data-stu-id="12e77-149">73</span></span>

<span data-ttu-id="12e77-150">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-151">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-152">74</span><span class="sxs-lookup"><span data-stu-id="12e77-152">74</span></span>

<span data-ttu-id="12e77-153">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-154">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="12e77-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-155">75</span><span class="sxs-lookup"><span data-stu-id="12e77-155">75</span></span>

<span data-ttu-id="12e77-156">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="12e77-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-157">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-158">76</span><span class="sxs-lookup"><span data-stu-id="12e77-158">76</span></span>

<span data-ttu-id="12e77-159">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-160">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-161">77</span><span class="sxs-lookup"><span data-stu-id="12e77-161">77</span></span>

<span data-ttu-id="12e77-162">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-163">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="12e77-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-164">78</span><span class="sxs-lookup"><span data-stu-id="12e77-164">78</span></span>

<span data-ttu-id="12e77-165">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="12e77-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-166">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-167">79</span><span class="sxs-lookup"><span data-stu-id="12e77-167">79</span></span>

<span data-ttu-id="12e77-168">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-169">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="12e77-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-170">80</span><span class="sxs-lookup"><span data-stu-id="12e77-170">80</span></span>

<span data-ttu-id="12e77-171">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="12e77-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-172">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="12e77-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-173">81</span><span class="sxs-lookup"><span data-stu-id="12e77-173">81</span></span>

<span data-ttu-id="12e77-174">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="12e77-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-175">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="12e77-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-176">82</span><span class="sxs-lookup"><span data-stu-id="12e77-176">82</span></span>

<span data-ttu-id="12e77-177">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="12e77-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-178">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="12e77-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-179">83</span><span class="sxs-lookup"><span data-stu-id="12e77-179">83</span></span>

<span data-ttu-id="12e77-180">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="12e77-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-181">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="12e77-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-182">84</span><span class="sxs-lookup"><span data-stu-id="12e77-182">84</span></span>

<span data-ttu-id="12e77-183">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="12e77-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-184">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="12e77-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-185">85 %</span><span class="sxs-lookup"><span data-stu-id="12e77-185">85</span></span>

<span data-ttu-id="12e77-186">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="12e77-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-187">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="12e77-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-188">86</span><span class="sxs-lookup"><span data-stu-id="12e77-188">86</span></span>

<span data-ttu-id="12e77-189">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="12e77-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-190">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-191">87</span><span class="sxs-lookup"><span data-stu-id="12e77-191">87</span></span>

<span data-ttu-id="12e77-192">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-193">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="12e77-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-194">88</span><span class="sxs-lookup"><span data-stu-id="12e77-194">88</span></span>

<span data-ttu-id="12e77-195">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="12e77-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-196">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="12e77-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-197">89</span><span class="sxs-lookup"><span data-stu-id="12e77-197">89</span></span>

<span data-ttu-id="12e77-198">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="12e77-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-199">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="12e77-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-200">90</span><span class="sxs-lookup"><span data-stu-id="12e77-200">90</span></span>

<span data-ttu-id="12e77-201">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="12e77-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-202">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="12e77-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-203">91</span><span class="sxs-lookup"><span data-stu-id="12e77-203">91</span></span>

<span data-ttu-id="12e77-204">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="12e77-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-205">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="12e77-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-206">92</span><span class="sxs-lookup"><span data-stu-id="12e77-206">92</span></span>

<span data-ttu-id="12e77-207">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="12e77-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-208">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="12e77-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-209">93</span><span class="sxs-lookup"><span data-stu-id="12e77-209">93</span></span>

<span data-ttu-id="12e77-210">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="12e77-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-211">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="12e77-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-212">94</span><span class="sxs-lookup"><span data-stu-id="12e77-212">94</span></span>

<span data-ttu-id="12e77-213">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="12e77-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-214">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="12e77-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-215">95</span><span class="sxs-lookup"><span data-stu-id="12e77-215">95</span></span>

<span data-ttu-id="12e77-216">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="12e77-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-217">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="12e77-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-218">96</span><span class="sxs-lookup"><span data-stu-id="12e77-218">96</span></span>

<span data-ttu-id="12e77-219">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="12e77-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-220">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="12e77-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-221">97</span><span class="sxs-lookup"><span data-stu-id="12e77-221">97</span></span>

<span data-ttu-id="12e77-222">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="12e77-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-223">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="12e77-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-224">98</span><span class="sxs-lookup"><span data-stu-id="12e77-224">98</span></span>

<span data-ttu-id="12e77-225">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="12e77-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-226">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="12e77-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-227">100</span><span class="sxs-lookup"><span data-stu-id="12e77-227">100</span></span>

<span data-ttu-id="12e77-228">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="12e77-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="12e77-229">**Autres**</span><span class="sxs-lookup"><span data-stu-id="12e77-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="12e77-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="12e77-230">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="12e77-231">Exemples</span><span class="sxs-lookup"><span data-stu-id="12e77-231">Examples</span></span>

<span data-ttu-id="12e77-232">L’exemple de code VBScript suivant libère tous les baux DHCP actuellement utilisés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="12e77-232">The following VBScript code sample releases all the DHCP leases currently in use on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.ReleaseDHCPLeaseAll() 
```



## <a name="requirements"></a><span data-ttu-id="12e77-233">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12e77-233">Requirements</span></span>



| <span data-ttu-id="12e77-234">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12e77-234">Requirement</span></span> | <span data-ttu-id="12e77-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="12e77-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12e77-236">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12e77-236">Minimum supported client</span></span><br/> | <span data-ttu-id="12e77-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12e77-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12e77-238">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12e77-238">Minimum supported server</span></span><br/> | <span data-ttu-id="12e77-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12e77-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12e77-240">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="12e77-240">Namespace</span></span><br/>                | <span data-ttu-id="12e77-241">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="12e77-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12e77-242">MOF</span><span class="sxs-lookup"><span data-stu-id="12e77-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12e77-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12e77-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12e77-244">DLL</span><span class="sxs-lookup"><span data-stu-id="12e77-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12e77-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12e77-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e77-246">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12e77-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e77-247">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="12e77-247">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="12e77-248">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="12e77-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="12e77-249">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="12e77-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="12e77-250">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="12e77-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="12e77-251">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="12e77-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

