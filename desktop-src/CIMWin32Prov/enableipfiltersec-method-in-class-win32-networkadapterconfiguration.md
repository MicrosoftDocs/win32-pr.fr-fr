---
description: La méthode statique de la classe WMI EnableIPFilterSec permet d’activer le protocole IPsec (Internet Protocol Security) de manière globale sur toutes les cartes réseau liées à IP.
ms.assetid: 565acc18-61e7-473e-b2cc-41f0e8c29193
ms.tgt_platform: multiple
title: Méthode EnableIPFilterSec de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPFilterSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3429e2c2ba78e013da9195961b76ff84ffda9b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860958"
---
# <a name="enableipfiltersec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="0e252-103">Méthode EnableIPFilterSec de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e252-103">EnableIPFilterSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="0e252-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableIPFilterSec** permet d’activer le protocole IPSec (Internet Protocol Security) de manière globale sur toutes les cartes réseau liées à IP.</span><span class="sxs-lookup"><span data-stu-id="0e252-104">The **EnableIPFilterSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Internet Protocol security (IPsec) globally across all IP-bound network adapters.</span></span>

<span data-ttu-id="0e252-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0e252-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0e252-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0e252-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e252-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e252-107">Syntax</span></span>


```mof
uint32 EnableIPFilterSec(
  [in] boolean IPFilterSecurityEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="0e252-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e252-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e252-109">*IPFilterSecurityEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e252-109">*IPFilterSecurityEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e252-110">Si la **valeur est true**, IPSec est activé globalement pour toutes les cartes réseau liées à IP.</span><span class="sxs-lookup"><span data-stu-id="0e252-110">If **true**, IPsec is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="0e252-111">Si la **valeur est false**, tout le trafic de protocole et de port est autorisé à passer non filtré.</span><span class="sxs-lookup"><span data-stu-id="0e252-111">If **false**, all port and protocol traffic is allowed to flow unfiltered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e252-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e252-112">Return value</span></span>

<span data-ttu-id="0e252-113">Retourne la valeur 0 (zéro) pour une exécution réussie lorsqu’un redémarrage n’est pas nécessaire, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et tout autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0e252-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="0e252-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0e252-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0e252-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0e252-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0e252-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="0e252-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-117">0</span><span class="sxs-lookup"><span data-stu-id="0e252-117">0</span></span>

<span data-ttu-id="0e252-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0e252-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="0e252-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-120">1</span><span class="sxs-lookup"><span data-stu-id="0e252-120">1</span></span>

<span data-ttu-id="0e252-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="0e252-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="0e252-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-123">64</span><span class="sxs-lookup"><span data-stu-id="0e252-123">64</span></span>

<span data-ttu-id="0e252-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="0e252-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="0e252-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-126">65</span><span class="sxs-lookup"><span data-stu-id="0e252-126">65</span></span>

<span data-ttu-id="0e252-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="0e252-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-129">66</span><span class="sxs-lookup"><span data-stu-id="0e252-129">66</span></span>

<span data-ttu-id="0e252-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="0e252-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-132">67</span><span class="sxs-lookup"><span data-stu-id="0e252-132">67</span></span>

<span data-ttu-id="0e252-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="0e252-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-135">68</span><span class="sxs-lookup"><span data-stu-id="0e252-135">68</span></span>

<span data-ttu-id="0e252-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="0e252-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-138">69</span><span class="sxs-lookup"><span data-stu-id="0e252-138">69</span></span>

<span data-ttu-id="0e252-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0e252-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-141">70</span><span class="sxs-lookup"><span data-stu-id="0e252-141">70</span></span>

<span data-ttu-id="0e252-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-144">71</span><span class="sxs-lookup"><span data-stu-id="0e252-144">71</span></span>

<span data-ttu-id="0e252-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="0e252-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-147">72</span><span class="sxs-lookup"><span data-stu-id="0e252-147">72</span></span>

<span data-ttu-id="0e252-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="0e252-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-150">73</span><span class="sxs-lookup"><span data-stu-id="0e252-150">73</span></span>

<span data-ttu-id="0e252-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-153">74</span><span class="sxs-lookup"><span data-stu-id="0e252-153">74</span></span>

<span data-ttu-id="0e252-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="0e252-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-156">75</span><span class="sxs-lookup"><span data-stu-id="0e252-156">75</span></span>

<span data-ttu-id="0e252-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="0e252-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-159">76</span><span class="sxs-lookup"><span data-stu-id="0e252-159">76</span></span>

<span data-ttu-id="0e252-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-162">77</span><span class="sxs-lookup"><span data-stu-id="0e252-162">77</span></span>

<span data-ttu-id="0e252-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="0e252-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-165">78</span><span class="sxs-lookup"><span data-stu-id="0e252-165">78</span></span>

<span data-ttu-id="0e252-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="0e252-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-168">79</span><span class="sxs-lookup"><span data-stu-id="0e252-168">79</span></span>

<span data-ttu-id="0e252-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="0e252-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-171">80</span><span class="sxs-lookup"><span data-stu-id="0e252-171">80</span></span>

<span data-ttu-id="0e252-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0e252-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="0e252-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-174">81</span><span class="sxs-lookup"><span data-stu-id="0e252-174">81</span></span>

<span data-ttu-id="0e252-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="0e252-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="0e252-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-177">82</span><span class="sxs-lookup"><span data-stu-id="0e252-177">82</span></span>

<span data-ttu-id="0e252-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="0e252-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="0e252-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-180">83</span><span class="sxs-lookup"><span data-stu-id="0e252-180">83</span></span>

<span data-ttu-id="0e252-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="0e252-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="0e252-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-183">84</span><span class="sxs-lookup"><span data-stu-id="0e252-183">84</span></span>

<span data-ttu-id="0e252-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="0e252-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="0e252-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-186">85 %</span><span class="sxs-lookup"><span data-stu-id="0e252-186">85</span></span>

<span data-ttu-id="0e252-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="0e252-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="0e252-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-189">86</span><span class="sxs-lookup"><span data-stu-id="0e252-189">86</span></span>

<span data-ttu-id="0e252-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="0e252-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-192">87</span><span class="sxs-lookup"><span data-stu-id="0e252-192">87</span></span>

<span data-ttu-id="0e252-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="0e252-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-195">88</span><span class="sxs-lookup"><span data-stu-id="0e252-195">88</span></span>

<span data-ttu-id="0e252-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="0e252-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="0e252-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-198">89</span><span class="sxs-lookup"><span data-stu-id="0e252-198">89</span></span>

<span data-ttu-id="0e252-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="0e252-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="0e252-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-201">90</span><span class="sxs-lookup"><span data-stu-id="0e252-201">90</span></span>

<span data-ttu-id="0e252-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="0e252-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="0e252-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-204">91</span><span class="sxs-lookup"><span data-stu-id="0e252-204">91</span></span>

<span data-ttu-id="0e252-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0e252-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="0e252-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-207">92</span><span class="sxs-lookup"><span data-stu-id="0e252-207">92</span></span>

<span data-ttu-id="0e252-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="0e252-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="0e252-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-210">93</span><span class="sxs-lookup"><span data-stu-id="0e252-210">93</span></span>

<span data-ttu-id="0e252-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0e252-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="0e252-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-213">94</span><span class="sxs-lookup"><span data-stu-id="0e252-213">94</span></span>

<span data-ttu-id="0e252-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="0e252-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="0e252-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-216">95</span><span class="sxs-lookup"><span data-stu-id="0e252-216">95</span></span>

<span data-ttu-id="0e252-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="0e252-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="0e252-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-219">96</span><span class="sxs-lookup"><span data-stu-id="0e252-219">96</span></span>

<span data-ttu-id="0e252-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="0e252-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="0e252-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-222">97</span><span class="sxs-lookup"><span data-stu-id="0e252-222">97</span></span>

<span data-ttu-id="0e252-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="0e252-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="0e252-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-225">98</span><span class="sxs-lookup"><span data-stu-id="0e252-225">98</span></span>

<span data-ttu-id="0e252-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="0e252-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="0e252-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-228">100</span><span class="sxs-lookup"><span data-stu-id="0e252-228">100</span></span>

<span data-ttu-id="0e252-229">DHCP n’est pas activé sur la carte.</span><span class="sxs-lookup"><span data-stu-id="0e252-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0e252-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="0e252-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="0e252-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="0e252-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e252-232">Notes</span><span class="sxs-lookup"><span data-stu-id="0e252-232">Remarks</span></span>

<span data-ttu-id="0e252-233">Lorsque la sécurité est activée, les caractéristiques de sécurité opérationnelles d’une carte réseau peuvent être contrôlées à l’aide de la méthode [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) spécifique à la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="0e252-233">With security enabled, the operational security characteristics for any one network adapter can be controlled by using the network adapter-specific [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="0e252-234">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e252-234">Examples</span></span>

<span data-ttu-id="0e252-235">Le code suivant, extrait de l’exemple [activer la sécurité IPFilter sur toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) de la Galerie TechNet, active la sécurité de filtre IP pour toutes les cartes réseau installées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0e252-235">The following code, taken from the [Enable IPFilter Security on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) sample on TechNet Gallery, enables IP filter security for all the network adapters installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.EnableIPFilterSec(True)
```



## <a name="requirements"></a><span data-ttu-id="0e252-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e252-236">Requirements</span></span>



| <span data-ttu-id="0e252-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e252-237">Requirement</span></span> | <span data-ttu-id="0e252-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e252-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e252-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e252-239">Minimum supported client</span></span><br/> | <span data-ttu-id="0e252-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e252-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e252-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e252-241">Minimum supported server</span></span><br/> | <span data-ttu-id="0e252-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e252-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e252-243">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e252-243">Namespace</span></span><br/>                | <span data-ttu-id="0e252-244">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0e252-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e252-245">MOF</span><span class="sxs-lookup"><span data-stu-id="0e252-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e252-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e252-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e252-247">DLL</span><span class="sxs-lookup"><span data-stu-id="0e252-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e252-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e252-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e252-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e252-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e252-250">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="0e252-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0e252-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="0e252-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="0e252-252">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="0e252-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="0e252-253">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="0e252-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="0e252-254">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="0e252-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

