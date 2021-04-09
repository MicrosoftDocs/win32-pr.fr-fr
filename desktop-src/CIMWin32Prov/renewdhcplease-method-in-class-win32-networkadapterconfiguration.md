---
description: La méthode de classe WMI RenewDHCPLease renouvelle l’adresse IP sur des cartes réseau compatibles DHCP spécifiques.
ms.assetid: b6e5d1fb-db3f-4491-bbac-46b1f2e7206e
ms.tgt_platform: multiple
title: Méthode RenewDHCPLease de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4603f013c6b4c2c80edd555608b5f59325b6a6d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033784"
---
# <a name="renewdhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8a494-103">Méthode RenewDHCPLease de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a494-103">RenewDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8a494-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenewDHCPLease** renouvelle l’adresse IP sur des cartes réseau compatibles DHCP spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8a494-104">The **RenewDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renews the IP address on specific DHCP-enabled network adapters.</span></span>

<span data-ttu-id="8a494-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8a494-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8a494-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8a494-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a494-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a494-107">Syntax</span></span>


```mof
uint32 RenewDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="8a494-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a494-108">Parameters</span></span>

<span data-ttu-id="8a494-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8a494-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a494-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a494-110">Return value</span></span>

<span data-ttu-id="8a494-111">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8a494-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="8a494-112">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8a494-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8a494-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8a494-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8a494-114">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="8a494-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-115">0</span><span class="sxs-lookup"><span data-stu-id="8a494-115">0</span></span>

<span data-ttu-id="8a494-116">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8a494-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-117">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="8a494-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-118">1</span><span class="sxs-lookup"><span data-stu-id="8a494-118">1</span></span>

<span data-ttu-id="8a494-119">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="8a494-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-120">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="8a494-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-121">64</span><span class="sxs-lookup"><span data-stu-id="8a494-121">64</span></span>

<span data-ttu-id="8a494-122">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="8a494-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-123">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="8a494-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-124">65</span><span class="sxs-lookup"><span data-stu-id="8a494-124">65</span></span>

<span data-ttu-id="8a494-125">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="8a494-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-126">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-127">66</span><span class="sxs-lookup"><span data-stu-id="8a494-127">66</span></span>

<span data-ttu-id="8a494-128">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-129">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="8a494-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-130">67</span><span class="sxs-lookup"><span data-stu-id="8a494-130">67</span></span>

<span data-ttu-id="8a494-131">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="8a494-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-132">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-133">68</span><span class="sxs-lookup"><span data-stu-id="8a494-133">68</span></span>

<span data-ttu-id="8a494-134">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-135">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="8a494-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-136">69</span><span class="sxs-lookup"><span data-stu-id="8a494-136">69</span></span>

<span data-ttu-id="8a494-137">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8a494-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-138">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-139">70</span><span class="sxs-lookup"><span data-stu-id="8a494-139">70</span></span>

<span data-ttu-id="8a494-140">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-141">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-142">71</span><span class="sxs-lookup"><span data-stu-id="8a494-142">71</span></span>

<span data-ttu-id="8a494-143">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-144">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="8a494-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-145">72</span><span class="sxs-lookup"><span data-stu-id="8a494-145">72</span></span>

<span data-ttu-id="8a494-146">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="8a494-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-147">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-148">73</span><span class="sxs-lookup"><span data-stu-id="8a494-148">73</span></span>

<span data-ttu-id="8a494-149">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-150">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-151">74</span><span class="sxs-lookup"><span data-stu-id="8a494-151">74</span></span>

<span data-ttu-id="8a494-152">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-153">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="8a494-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-154">75</span><span class="sxs-lookup"><span data-stu-id="8a494-154">75</span></span>

<span data-ttu-id="8a494-155">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="8a494-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-156">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-157">76</span><span class="sxs-lookup"><span data-stu-id="8a494-157">76</span></span>

<span data-ttu-id="8a494-158">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-159">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-160">77</span><span class="sxs-lookup"><span data-stu-id="8a494-160">77</span></span>

<span data-ttu-id="8a494-161">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-162">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="8a494-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-163">78</span><span class="sxs-lookup"><span data-stu-id="8a494-163">78</span></span>

<span data-ttu-id="8a494-164">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="8a494-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-165">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-166">79</span><span class="sxs-lookup"><span data-stu-id="8a494-166">79</span></span>

<span data-ttu-id="8a494-167">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-168">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8a494-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-169">80</span><span class="sxs-lookup"><span data-stu-id="8a494-169">80</span></span>

<span data-ttu-id="8a494-170">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8a494-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-171">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="8a494-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-172">81</span><span class="sxs-lookup"><span data-stu-id="8a494-172">81</span></span>

<span data-ttu-id="8a494-173">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="8a494-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-174">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="8a494-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-175">82</span><span class="sxs-lookup"><span data-stu-id="8a494-175">82</span></span>

<span data-ttu-id="8a494-176">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="8a494-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-177">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="8a494-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-178">83</span><span class="sxs-lookup"><span data-stu-id="8a494-178">83</span></span>

<span data-ttu-id="8a494-179">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="8a494-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-180">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="8a494-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-181">84</span><span class="sxs-lookup"><span data-stu-id="8a494-181">84</span></span>

<span data-ttu-id="8a494-182">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8a494-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-183">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="8a494-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-184">85 %</span><span class="sxs-lookup"><span data-stu-id="8a494-184">85</span></span>

<span data-ttu-id="8a494-185">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8a494-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-186">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="8a494-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-187">86</span><span class="sxs-lookup"><span data-stu-id="8a494-187">86</span></span>

<span data-ttu-id="8a494-188">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="8a494-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-189">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-190">87</span><span class="sxs-lookup"><span data-stu-id="8a494-190">87</span></span>

<span data-ttu-id="8a494-191">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-192">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="8a494-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-193">88</span><span class="sxs-lookup"><span data-stu-id="8a494-193">88</span></span>

<span data-ttu-id="8a494-194">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="8a494-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-195">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="8a494-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-196">89</span><span class="sxs-lookup"><span data-stu-id="8a494-196">89</span></span>

<span data-ttu-id="8a494-197">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="8a494-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-198">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="8a494-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-199">90</span><span class="sxs-lookup"><span data-stu-id="8a494-199">90</span></span>

<span data-ttu-id="8a494-200">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="8a494-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-201">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="8a494-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-202">91</span><span class="sxs-lookup"><span data-stu-id="8a494-202">91</span></span>

<span data-ttu-id="8a494-203">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="8a494-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-204">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="8a494-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-205">92</span><span class="sxs-lookup"><span data-stu-id="8a494-205">92</span></span>

<span data-ttu-id="8a494-206">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="8a494-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-207">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="8a494-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-208">93</span><span class="sxs-lookup"><span data-stu-id="8a494-208">93</span></span>

<span data-ttu-id="8a494-209">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="8a494-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-210">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="8a494-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-211">94</span><span class="sxs-lookup"><span data-stu-id="8a494-211">94</span></span>

<span data-ttu-id="8a494-212">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="8a494-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-213">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="8a494-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-214">95</span><span class="sxs-lookup"><span data-stu-id="8a494-214">95</span></span>

<span data-ttu-id="8a494-215">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="8a494-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-216">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="8a494-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-217">96</span><span class="sxs-lookup"><span data-stu-id="8a494-217">96</span></span>

<span data-ttu-id="8a494-218">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="8a494-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-219">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="8a494-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-220">97</span><span class="sxs-lookup"><span data-stu-id="8a494-220">97</span></span>

<span data-ttu-id="8a494-221">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="8a494-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-222">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="8a494-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-223">98</span><span class="sxs-lookup"><span data-stu-id="8a494-223">98</span></span>

<span data-ttu-id="8a494-224">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="8a494-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-225">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="8a494-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-226">100</span><span class="sxs-lookup"><span data-stu-id="8a494-226">100</span></span>

<span data-ttu-id="8a494-227">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8a494-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8a494-228">**Autres**</span><span class="sxs-lookup"><span data-stu-id="8a494-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8a494-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8a494-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a494-230">Notes</span><span class="sxs-lookup"><span data-stu-id="8a494-230">Remarks</span></span>

<span data-ttu-id="8a494-231">Le bail de l’adresse IP attribuée par un serveur DHCP a une date d’expiration que le client doit renouveler s’il a l’intention de continuer à utiliser l’adresse IP attribuée.</span><span class="sxs-lookup"><span data-stu-id="8a494-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="8a494-232">Exemples</span><span class="sxs-lookup"><span data-stu-id="8a494-232">Examples</span></span>

<span data-ttu-id="8a494-233">La [version renouveler les adresses IP à l’aide](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) de PowerShell PowerShell dans la Galerie TechNet utilise **RenewDHCPLease** pour publier et renouveler une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="8a494-233">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **RenewDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="8a494-234">L’exemple de [renouvellement de bail DHCP pour une carte réseau](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) dans la Galerie TechNet utilise **RenewDHCPLease** pour renouveler le bail DHCP pour chaque carte réseau TCP/IP d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8a494-234">The [Renew the DHCP Lease for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) VBScript sample on TechNet Gallery uses **RenewDHCPLease** to renew the DHCP lease for each TCP/IP-bound network adapter in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a494-235">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a494-235">Requirements</span></span>



| <span data-ttu-id="8a494-236">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a494-236">Requirement</span></span> | <span data-ttu-id="8a494-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a494-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a494-238">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a494-238">Minimum supported client</span></span><br/> | <span data-ttu-id="8a494-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a494-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a494-240">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a494-240">Minimum supported server</span></span><br/> | <span data-ttu-id="8a494-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a494-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a494-242">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8a494-242">Namespace</span></span><br/>                | <span data-ttu-id="8a494-243">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8a494-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8a494-244">MOF</span><span class="sxs-lookup"><span data-stu-id="8a494-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a494-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a494-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a494-246">DLL</span><span class="sxs-lookup"><span data-stu-id="8a494-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a494-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a494-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a494-248">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a494-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a494-249">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="8a494-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8a494-250">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="8a494-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8a494-251">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="8a494-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8a494-252">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="8a494-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8a494-253">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="8a494-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

