---
description: La méthode de classe WMI SetWINSServer définit les serveurs WINS (Windows Internet Service de nommage) principaux et secondaires sur cette carte réseau TCP/IP. Cette méthode est appliquée indépendamment de la carte réseau.
ms.assetid: fa8ce436-b67e-4975-a5c5-1a7d6aab4c8e
ms.tgt_platform: multiple
title: Méthode SetWINSServer de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetWINSServer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49bfb0103a7d9cbbd6ea3faa0e1a868bac7b0196
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515768"
---
# <a name="setwinsserver-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8af5d-104">Méthode SetWINSServer de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="8af5d-104">SetWINSServer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8af5d-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetWINSServer** définit les serveurs WINS (Windows Internet service de nommage) principaux et secondaires sur cette carte réseau TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8af5d-105">The **SetWINSServer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span> <span data-ttu-id="8af5d-106">Cette méthode est appliquée indépendamment de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="8af5d-106">This method is applied independently of the network adapter.</span></span>

<span data-ttu-id="8af5d-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8af5d-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8af5d-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8af5d-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8af5d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8af5d-109">Syntax</span></span>


```mof
uint32 SetWINSServer(
  [in] string WINSPrimaryServer,
  [in] string WINSSecondaryServer
);
```



## <a name="parameters"></a><span data-ttu-id="8af5d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8af5d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af5d-111">*WINSPrimaryServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8af5d-111">*WINSPrimaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-112">Adresse IP du serveur WINS principal.</span><span class="sxs-lookup"><span data-stu-id="8af5d-112">IP address of the primary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="8af5d-113">Vérifiez toujours la validité de cette adresse IP lorsqu’elle provient d’une source inconnue ou d’une source qui n’est pas digne de confiance.</span><span class="sxs-lookup"><span data-stu-id="8af5d-113">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> <dt>

<span data-ttu-id="8af5d-114">*WINSSecondaryServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8af5d-114">*WINSSecondaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-115">Adresse IP du serveur WINS secondaire.</span><span class="sxs-lookup"><span data-stu-id="8af5d-115">IP address of the secondary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="8af5d-116">Vérifiez toujours la validité de cette adresse IP lorsqu’elle provient d’une source inconnue ou d’une source qui n’est pas digne de confiance.</span><span class="sxs-lookup"><span data-stu-id="8af5d-116">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af5d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8af5d-117">Return value</span></span>

<span data-ttu-id="8af5d-118">Retourne une valeur entière égale à 0 (zéro) en cas de réussite de l’opération, ainsi que tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="8af5d-118">Returns an integer value of 0 (zero) on successful completion, and any other number to indicate an error.</span></span> <span data-ttu-id="8af5d-119">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8af5d-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8af5d-120">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8af5d-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8af5d-121">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="8af5d-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-122">0</span><span class="sxs-lookup"><span data-stu-id="8af5d-122">0</span></span>

<span data-ttu-id="8af5d-123">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8af5d-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-124">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="8af5d-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-125">1</span><span class="sxs-lookup"><span data-stu-id="8af5d-125">1</span></span>

<span data-ttu-id="8af5d-126">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="8af5d-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-127">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="8af5d-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-128">64</span><span class="sxs-lookup"><span data-stu-id="8af5d-128">64</span></span>

<span data-ttu-id="8af5d-129">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="8af5d-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-130">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="8af5d-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-131">65</span><span class="sxs-lookup"><span data-stu-id="8af5d-131">65</span></span>

<span data-ttu-id="8af5d-132">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="8af5d-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-133">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-134">66</span><span class="sxs-lookup"><span data-stu-id="8af5d-134">66</span></span>

<span data-ttu-id="8af5d-135">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-136">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="8af5d-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-137">67</span><span class="sxs-lookup"><span data-stu-id="8af5d-137">67</span></span>

<span data-ttu-id="8af5d-138">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="8af5d-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-139">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-140">68</span><span class="sxs-lookup"><span data-stu-id="8af5d-140">68</span></span>

<span data-ttu-id="8af5d-141">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-142">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="8af5d-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-143">69</span><span class="sxs-lookup"><span data-stu-id="8af5d-143">69</span></span>

<span data-ttu-id="8af5d-144">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8af5d-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-145">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-146">70</span><span class="sxs-lookup"><span data-stu-id="8af5d-146">70</span></span>

<span data-ttu-id="8af5d-147">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-148">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-149">71</span><span class="sxs-lookup"><span data-stu-id="8af5d-149">71</span></span>

<span data-ttu-id="8af5d-150">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-151">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="8af5d-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-152">72</span><span class="sxs-lookup"><span data-stu-id="8af5d-152">72</span></span>

<span data-ttu-id="8af5d-153">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="8af5d-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-154">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-155">73</span><span class="sxs-lookup"><span data-stu-id="8af5d-155">73</span></span>

<span data-ttu-id="8af5d-156">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-157">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-158">74</span><span class="sxs-lookup"><span data-stu-id="8af5d-158">74</span></span>

<span data-ttu-id="8af5d-159">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-160">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="8af5d-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-161">75</span><span class="sxs-lookup"><span data-stu-id="8af5d-161">75</span></span>

<span data-ttu-id="8af5d-162">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="8af5d-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-163">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-164">76</span><span class="sxs-lookup"><span data-stu-id="8af5d-164">76</span></span>

<span data-ttu-id="8af5d-165">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-166">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-167">77</span><span class="sxs-lookup"><span data-stu-id="8af5d-167">77</span></span>

<span data-ttu-id="8af5d-168">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-169">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="8af5d-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-170">78</span><span class="sxs-lookup"><span data-stu-id="8af5d-170">78</span></span>

<span data-ttu-id="8af5d-171">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="8af5d-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-172">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-173">79</span><span class="sxs-lookup"><span data-stu-id="8af5d-173">79</span></span>

<span data-ttu-id="8af5d-174">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-175">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8af5d-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-176">80</span><span class="sxs-lookup"><span data-stu-id="8af5d-176">80</span></span>

<span data-ttu-id="8af5d-177">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8af5d-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-178">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="8af5d-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-179">81</span><span class="sxs-lookup"><span data-stu-id="8af5d-179">81</span></span>

<span data-ttu-id="8af5d-180">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="8af5d-180">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-181">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="8af5d-181">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-182">82</span><span class="sxs-lookup"><span data-stu-id="8af5d-182">82</span></span>

<span data-ttu-id="8af5d-183">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="8af5d-183">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-184">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="8af5d-184">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-185">83</span><span class="sxs-lookup"><span data-stu-id="8af5d-185">83</span></span>

<span data-ttu-id="8af5d-186">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="8af5d-186">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-187">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="8af5d-187">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-188">84</span><span class="sxs-lookup"><span data-stu-id="8af5d-188">84</span></span>

<span data-ttu-id="8af5d-189">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8af5d-189">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-190">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="8af5d-190">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-191">85 %</span><span class="sxs-lookup"><span data-stu-id="8af5d-191">85</span></span>

<span data-ttu-id="8af5d-192">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8af5d-192">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-193">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="8af5d-193">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-194">86</span><span class="sxs-lookup"><span data-stu-id="8af5d-194">86</span></span>

<span data-ttu-id="8af5d-195">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="8af5d-195">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-196">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-196">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-197">87</span><span class="sxs-lookup"><span data-stu-id="8af5d-197">87</span></span>

<span data-ttu-id="8af5d-198">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-198">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-199">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="8af5d-199">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-200">88</span><span class="sxs-lookup"><span data-stu-id="8af5d-200">88</span></span>

<span data-ttu-id="8af5d-201">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="8af5d-201">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-202">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="8af5d-202">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-203">89</span><span class="sxs-lookup"><span data-stu-id="8af5d-203">89</span></span>

<span data-ttu-id="8af5d-204">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="8af5d-204">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-205">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="8af5d-205">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-206">90</span><span class="sxs-lookup"><span data-stu-id="8af5d-206">90</span></span>

<span data-ttu-id="8af5d-207">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="8af5d-207">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-208">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="8af5d-208">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-209">91</span><span class="sxs-lookup"><span data-stu-id="8af5d-209">91</span></span>

<span data-ttu-id="8af5d-210">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="8af5d-210">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-211">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="8af5d-211">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-212">92</span><span class="sxs-lookup"><span data-stu-id="8af5d-212">92</span></span>

<span data-ttu-id="8af5d-213">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="8af5d-213">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-214">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="8af5d-214">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-215">93</span><span class="sxs-lookup"><span data-stu-id="8af5d-215">93</span></span>

<span data-ttu-id="8af5d-216">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="8af5d-216">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-217">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="8af5d-217">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-218">94</span><span class="sxs-lookup"><span data-stu-id="8af5d-218">94</span></span>

<span data-ttu-id="8af5d-219">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="8af5d-219">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-220">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="8af5d-220">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-221">95</span><span class="sxs-lookup"><span data-stu-id="8af5d-221">95</span></span>

<span data-ttu-id="8af5d-222">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="8af5d-222">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-223">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="8af5d-223">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-224">96</span><span class="sxs-lookup"><span data-stu-id="8af5d-224">96</span></span>

<span data-ttu-id="8af5d-225">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="8af5d-225">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-226">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="8af5d-226">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-227">97</span><span class="sxs-lookup"><span data-stu-id="8af5d-227">97</span></span>

<span data-ttu-id="8af5d-228">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="8af5d-228">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-229">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="8af5d-229">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-230">98</span><span class="sxs-lookup"><span data-stu-id="8af5d-230">98</span></span>

<span data-ttu-id="8af5d-231">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="8af5d-231">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-232">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="8af5d-232">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-233">100</span><span class="sxs-lookup"><span data-stu-id="8af5d-233">100</span></span>

<span data-ttu-id="8af5d-234">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8af5d-234">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8af5d-235">**Autres**</span><span class="sxs-lookup"><span data-stu-id="8af5d-235">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8af5d-236">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8af5d-236">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8af5d-237">Notes</span><span class="sxs-lookup"><span data-stu-id="8af5d-237">Remarks</span></span>

<span data-ttu-id="8af5d-238">Si *WINSPrimaryServer* et *WINSSecondaryServer* sont tous les deux définis sur «» (une chaîne vide), les serveurs WINS explicites reviennent à DHCP.</span><span class="sxs-lookup"><span data-stu-id="8af5d-238">If both *WINSPrimaryServer* and *WINSSecondaryServer* are set to "" (an empty string), then explicit WINS servers revert back to DHCP.</span></span>

## <a name="examples"></a><span data-ttu-id="8af5d-239">Exemples</span><span class="sxs-lookup"><span data-stu-id="8af5d-239">Examples</span></span>

<span data-ttu-id="8af5d-240">[L’affectation d’une adresse IP extraite d’une base de données](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) L’exemple de code VBScript recherche un ordinateur dans une base de données et lui attribue l’adresse IP spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8af5d-240">[The Assign an IP Address Retrieved from a Database](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) VBScript code sample looks up a computer in a database and assigns that computer the specified IP address.</span></span>

<span data-ttu-id="8af5d-241">L’exemple de code VBScript suivant définit le serveur WINS principal et secondaire pour une carte réseau TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8af5d-241">The following VBScript code sample sets the primary and secondary WINS server for a TCP/IP-bound network adapter.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    strPrimaryServer = "192.168.1.100" 
    strSecondaryServer = "192.168.1.200" 
    objNetCard.SetWINSServer strPrimaryServer, strSecondaryServer 
Next 
```



## <a name="requirements"></a><span data-ttu-id="8af5d-242">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8af5d-242">Requirements</span></span>



| <span data-ttu-id="8af5d-243">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8af5d-243">Requirement</span></span> | <span data-ttu-id="8af5d-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="8af5d-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8af5d-245">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8af5d-245">Minimum supported client</span></span><br/> | <span data-ttu-id="8af5d-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8af5d-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8af5d-247">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8af5d-247">Minimum supported server</span></span><br/> | <span data-ttu-id="8af5d-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8af5d-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8af5d-249">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8af5d-249">Namespace</span></span><br/>                | <span data-ttu-id="8af5d-250">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8af5d-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8af5d-251">MOF</span><span class="sxs-lookup"><span data-stu-id="8af5d-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8af5d-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8af5d-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8af5d-253">DLL</span><span class="sxs-lookup"><span data-stu-id="8af5d-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8af5d-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8af5d-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af5d-255">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8af5d-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af5d-256">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="8af5d-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8af5d-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="8af5d-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8af5d-258">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="8af5d-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8af5d-259">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="8af5d-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8af5d-260">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="8af5d-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

