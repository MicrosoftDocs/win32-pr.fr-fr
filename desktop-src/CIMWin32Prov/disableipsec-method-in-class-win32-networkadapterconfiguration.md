---
description: La méthode de classe WMI DisableIPSec est utilisée pour désactiver la sécurité du protocole Internet (IPsec) sur cette carte réseau compatible TCP/IP.
ms.assetid: 6fff2721-1ee2-42b4-bbf9-fd36b97318e3
ms.tgt_platform: multiple
title: Méthode DisableIPSec de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.DisableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b2a17bbfa0f10c08edb581b4a4bf51173facfea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515927"
---
# <a name="disableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d84d5-103">Méthode DisableIPSec de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="d84d5-103">DisableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d84d5-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DisableIPSec** est utilisée pour désactiver la sécurité du protocole Internet (IPSec) sur cette carte réseau compatible TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d84d5-104">The **DisableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method is used to disable Internet Protocol security (IPsec) on this TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="d84d5-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d84d5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d84d5-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d84d5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d84d5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d84d5-107">Syntax</span></span>


```mof
uint32 DisableIPSec();
```



## <a name="parameters"></a><span data-ttu-id="d84d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d84d5-108">Parameters</span></span>

<span data-ttu-id="d84d5-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d84d5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d84d5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d84d5-110">Return value</span></span>

<span data-ttu-id="d84d5-111">Retourne la valeur 0 (zéro) pour une exécution réussie lorsqu’un redémarrage n’est pas nécessaire, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et tout autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d84d5-111">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="d84d5-112">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d84d5-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d84d5-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d84d5-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d84d5-114">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="d84d5-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-115">0</span><span class="sxs-lookup"><span data-stu-id="d84d5-115">0</span></span>

<span data-ttu-id="d84d5-116">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d84d5-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-117">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="d84d5-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-118">1</span><span class="sxs-lookup"><span data-stu-id="d84d5-118">1</span></span>

<span data-ttu-id="d84d5-119">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="d84d5-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-120">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="d84d5-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-121">64</span><span class="sxs-lookup"><span data-stu-id="d84d5-121">64</span></span>

<span data-ttu-id="d84d5-122">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="d84d5-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-123">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="d84d5-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-124">65</span><span class="sxs-lookup"><span data-stu-id="d84d5-124">65</span></span>

<span data-ttu-id="d84d5-125">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="d84d5-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-126">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-127">66</span><span class="sxs-lookup"><span data-stu-id="d84d5-127">66</span></span>

<span data-ttu-id="d84d5-128">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-129">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="d84d5-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-130">67</span><span class="sxs-lookup"><span data-stu-id="d84d5-130">67</span></span>

<span data-ttu-id="d84d5-131">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="d84d5-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-132">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-133">68</span><span class="sxs-lookup"><span data-stu-id="d84d5-133">68</span></span>

<span data-ttu-id="d84d5-134">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-135">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="d84d5-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-136">69</span><span class="sxs-lookup"><span data-stu-id="d84d5-136">69</span></span>

<span data-ttu-id="d84d5-137">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d84d5-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-138">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-139">70</span><span class="sxs-lookup"><span data-stu-id="d84d5-139">70</span></span>

<span data-ttu-id="d84d5-140">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-141">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-142">71</span><span class="sxs-lookup"><span data-stu-id="d84d5-142">71</span></span>

<span data-ttu-id="d84d5-143">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-144">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="d84d5-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-145">72</span><span class="sxs-lookup"><span data-stu-id="d84d5-145">72</span></span>

<span data-ttu-id="d84d5-146">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="d84d5-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-147">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-148">73</span><span class="sxs-lookup"><span data-stu-id="d84d5-148">73</span></span>

<span data-ttu-id="d84d5-149">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-150">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-151">74</span><span class="sxs-lookup"><span data-stu-id="d84d5-151">74</span></span>

<span data-ttu-id="d84d5-152">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-153">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="d84d5-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-154">75</span><span class="sxs-lookup"><span data-stu-id="d84d5-154">75</span></span>

<span data-ttu-id="d84d5-155">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="d84d5-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-156">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-157">76</span><span class="sxs-lookup"><span data-stu-id="d84d5-157">76</span></span>

<span data-ttu-id="d84d5-158">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-159">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-160">77</span><span class="sxs-lookup"><span data-stu-id="d84d5-160">77</span></span>

<span data-ttu-id="d84d5-161">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-162">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="d84d5-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-163">78</span><span class="sxs-lookup"><span data-stu-id="d84d5-163">78</span></span>

<span data-ttu-id="d84d5-164">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="d84d5-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-165">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-166">79</span><span class="sxs-lookup"><span data-stu-id="d84d5-166">79</span></span>

<span data-ttu-id="d84d5-167">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-168">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="d84d5-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-169">80</span><span class="sxs-lookup"><span data-stu-id="d84d5-169">80</span></span>

<span data-ttu-id="d84d5-170">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d84d5-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-171">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="d84d5-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-172">81</span><span class="sxs-lookup"><span data-stu-id="d84d5-172">81</span></span>

<span data-ttu-id="d84d5-173">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="d84d5-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-174">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="d84d5-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-175">82</span><span class="sxs-lookup"><span data-stu-id="d84d5-175">82</span></span>

<span data-ttu-id="d84d5-176">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="d84d5-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-177">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="d84d5-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-178">83</span><span class="sxs-lookup"><span data-stu-id="d84d5-178">83</span></span>

<span data-ttu-id="d84d5-179">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="d84d5-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-180">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="d84d5-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-181">84</span><span class="sxs-lookup"><span data-stu-id="d84d5-181">84</span></span>

<span data-ttu-id="d84d5-182">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d84d5-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-183">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="d84d5-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-184">85 %</span><span class="sxs-lookup"><span data-stu-id="d84d5-184">85</span></span>

<span data-ttu-id="d84d5-185">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d84d5-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-186">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="d84d5-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-187">86</span><span class="sxs-lookup"><span data-stu-id="d84d5-187">86</span></span>

<span data-ttu-id="d84d5-188">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="d84d5-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-189">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-190">87</span><span class="sxs-lookup"><span data-stu-id="d84d5-190">87</span></span>

<span data-ttu-id="d84d5-191">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-192">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="d84d5-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-193">88</span><span class="sxs-lookup"><span data-stu-id="d84d5-193">88</span></span>

<span data-ttu-id="d84d5-194">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="d84d5-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-195">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="d84d5-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-196">89</span><span class="sxs-lookup"><span data-stu-id="d84d5-196">89</span></span>

<span data-ttu-id="d84d5-197">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="d84d5-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-198">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="d84d5-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-199">90</span><span class="sxs-lookup"><span data-stu-id="d84d5-199">90</span></span>

<span data-ttu-id="d84d5-200">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="d84d5-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-201">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="d84d5-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-202">91</span><span class="sxs-lookup"><span data-stu-id="d84d5-202">91</span></span>

<span data-ttu-id="d84d5-203">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="d84d5-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-204">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="d84d5-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-205">92</span><span class="sxs-lookup"><span data-stu-id="d84d5-205">92</span></span>

<span data-ttu-id="d84d5-206">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d84d5-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-207">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="d84d5-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-208">93</span><span class="sxs-lookup"><span data-stu-id="d84d5-208">93</span></span>

<span data-ttu-id="d84d5-209">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d84d5-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-210">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="d84d5-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-211">94</span><span class="sxs-lookup"><span data-stu-id="d84d5-211">94</span></span>

<span data-ttu-id="d84d5-212">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="d84d5-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-213">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="d84d5-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-214">95</span><span class="sxs-lookup"><span data-stu-id="d84d5-214">95</span></span>

<span data-ttu-id="d84d5-215">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="d84d5-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-216">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="d84d5-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-217">96</span><span class="sxs-lookup"><span data-stu-id="d84d5-217">96</span></span>

<span data-ttu-id="d84d5-218">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="d84d5-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-219">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="d84d5-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-220">97</span><span class="sxs-lookup"><span data-stu-id="d84d5-220">97</span></span>

<span data-ttu-id="d84d5-221">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="d84d5-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-222">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="d84d5-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-223">98</span><span class="sxs-lookup"><span data-stu-id="d84d5-223">98</span></span>

<span data-ttu-id="d84d5-224">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="d84d5-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-225">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="d84d5-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-226">100</span><span class="sxs-lookup"><span data-stu-id="d84d5-226">100</span></span>

<span data-ttu-id="d84d5-227">DHCP n’est pas activé sur la carte.</span><span class="sxs-lookup"><span data-stu-id="d84d5-227">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d84d5-228">**Autres**</span><span class="sxs-lookup"><span data-stu-id="d84d5-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d84d5-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d84d5-229">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d84d5-230">Exemples</span><span class="sxs-lookup"><span data-stu-id="d84d5-230">Examples</span></span>

<span data-ttu-id="d84d5-231">L’exemple VBScript suivant désactive la sécurité IP sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d84d5-231">The following VBScript sample disables the IP Security on a computer.</span></span> <span data-ttu-id="d84d5-232">Notez que l’appel réel à DisableIPSec est commenté, à des fins de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d84d5-232">Note that the actual call to DisableIPSec is commented out, for safety purposes.</span></span>


```VB
strServer = "."

Set objWMI = GetObject("winmgmts:\\" & strServer & "\root\cimv2")

strWQL = "select * from Win32_NetworkAdapterConfiguration"
Set objInstances = objWMI.ExecQuery(strWQL,,48)

For Each objInstance in objInstances

 ' Uncomment next line to disable security
 ' intResult = objInstance.DisableIPSec

Next
```



## <a name="requirements"></a><span data-ttu-id="d84d5-233">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d84d5-233">Requirements</span></span>



| <span data-ttu-id="d84d5-234">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d84d5-234">Requirement</span></span> | <span data-ttu-id="d84d5-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="d84d5-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d84d5-236">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d84d5-236">Minimum supported client</span></span><br/> | <span data-ttu-id="d84d5-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d84d5-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d84d5-238">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d84d5-238">Minimum supported server</span></span><br/> | <span data-ttu-id="d84d5-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d84d5-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d84d5-240">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d84d5-240">Namespace</span></span><br/>                | <span data-ttu-id="d84d5-241">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d84d5-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d84d5-242">MOF</span><span class="sxs-lookup"><span data-stu-id="d84d5-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d84d5-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d84d5-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d84d5-244">DLL</span><span class="sxs-lookup"><span data-stu-id="d84d5-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d84d5-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d84d5-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d84d5-246">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d84d5-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d84d5-247">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="d84d5-247">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d84d5-248">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="d84d5-248">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d84d5-249">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="d84d5-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d84d5-250">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="d84d5-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d84d5-251">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="d84d5-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

