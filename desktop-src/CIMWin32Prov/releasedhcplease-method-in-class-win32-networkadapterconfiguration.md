---
description: La méthode de classe WMI dispose ReleaseDHCPLease libère l’adresse IP liée à une carte réseau DHCP spécifique.
ms.assetid: 0cf4b531-8626-4388-bffa-e16a4aa8c794
ms.tgt_platform: multiple
title: Méthode dispose ReleaseDHCPLease de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5520a6b2d0960c1d4258b19f8cd4d600c9b8fe34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514945"
---
# <a name="releasedhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="26ba0-103">Méthode dispose ReleaseDHCPLease de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="26ba0-103">ReleaseDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="26ba0-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **dispose ReleaseDHCPLease** libère l’adresse IP liée à une carte réseau DHCP spécifique.</span><span class="sxs-lookup"><span data-stu-id="26ba0-104">The **ReleaseDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method releases the IP address bound to a specific DHCP-enabled network adapter.</span></span>

<span data-ttu-id="26ba0-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="26ba0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="26ba0-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="26ba0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="26ba0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26ba0-107">Syntax</span></span>


```mof
uint32 ReleaseDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="26ba0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26ba0-108">Parameters</span></span>

<span data-ttu-id="26ba0-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="26ba0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26ba0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26ba0-110">Return value</span></span>

<span data-ttu-id="26ba0-111">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="26ba0-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="26ba0-112">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="26ba0-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="26ba0-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="26ba0-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="26ba0-114">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="26ba0-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-115">0</span><span class="sxs-lookup"><span data-stu-id="26ba0-115">0</span></span>

<span data-ttu-id="26ba0-116">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="26ba0-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-117">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="26ba0-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-118">1</span><span class="sxs-lookup"><span data-stu-id="26ba0-118">1</span></span>

<span data-ttu-id="26ba0-119">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="26ba0-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-120">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="26ba0-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-121">64</span><span class="sxs-lookup"><span data-stu-id="26ba0-121">64</span></span>

<span data-ttu-id="26ba0-122">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="26ba0-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-123">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="26ba0-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-124">65</span><span class="sxs-lookup"><span data-stu-id="26ba0-124">65</span></span>

<span data-ttu-id="26ba0-125">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="26ba0-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-126">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-127">66</span><span class="sxs-lookup"><span data-stu-id="26ba0-127">66</span></span>

<span data-ttu-id="26ba0-128">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-129">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="26ba0-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-130">67</span><span class="sxs-lookup"><span data-stu-id="26ba0-130">67</span></span>

<span data-ttu-id="26ba0-131">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="26ba0-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-132">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-133">68</span><span class="sxs-lookup"><span data-stu-id="26ba0-133">68</span></span>

<span data-ttu-id="26ba0-134">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-135">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="26ba0-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-136">69</span><span class="sxs-lookup"><span data-stu-id="26ba0-136">69</span></span>

<span data-ttu-id="26ba0-137">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="26ba0-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-138">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-139">70</span><span class="sxs-lookup"><span data-stu-id="26ba0-139">70</span></span>

<span data-ttu-id="26ba0-140">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-141">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-142">71</span><span class="sxs-lookup"><span data-stu-id="26ba0-142">71</span></span>

<span data-ttu-id="26ba0-143">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-144">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="26ba0-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-145">72</span><span class="sxs-lookup"><span data-stu-id="26ba0-145">72</span></span>

<span data-ttu-id="26ba0-146">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="26ba0-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-147">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-148">73</span><span class="sxs-lookup"><span data-stu-id="26ba0-148">73</span></span>

<span data-ttu-id="26ba0-149">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-150">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-151">74</span><span class="sxs-lookup"><span data-stu-id="26ba0-151">74</span></span>

<span data-ttu-id="26ba0-152">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-153">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="26ba0-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-154">75</span><span class="sxs-lookup"><span data-stu-id="26ba0-154">75</span></span>

<span data-ttu-id="26ba0-155">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="26ba0-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-156">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-157">76</span><span class="sxs-lookup"><span data-stu-id="26ba0-157">76</span></span>

<span data-ttu-id="26ba0-158">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-159">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-160">77</span><span class="sxs-lookup"><span data-stu-id="26ba0-160">77</span></span>

<span data-ttu-id="26ba0-161">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-162">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="26ba0-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-163">78</span><span class="sxs-lookup"><span data-stu-id="26ba0-163">78</span></span>

<span data-ttu-id="26ba0-164">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="26ba0-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-165">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-166">79</span><span class="sxs-lookup"><span data-stu-id="26ba0-166">79</span></span>

<span data-ttu-id="26ba0-167">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-168">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="26ba0-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-169">80</span><span class="sxs-lookup"><span data-stu-id="26ba0-169">80</span></span>

<span data-ttu-id="26ba0-170">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="26ba0-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-171">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="26ba0-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-172">81</span><span class="sxs-lookup"><span data-stu-id="26ba0-172">81</span></span>

<span data-ttu-id="26ba0-173">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="26ba0-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-174">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="26ba0-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-175">82</span><span class="sxs-lookup"><span data-stu-id="26ba0-175">82</span></span>

<span data-ttu-id="26ba0-176">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="26ba0-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-177">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="26ba0-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-178">83</span><span class="sxs-lookup"><span data-stu-id="26ba0-178">83</span></span>

<span data-ttu-id="26ba0-179">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="26ba0-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-180">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="26ba0-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-181">84</span><span class="sxs-lookup"><span data-stu-id="26ba0-181">84</span></span>

<span data-ttu-id="26ba0-182">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="26ba0-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-183">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="26ba0-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-184">85 %</span><span class="sxs-lookup"><span data-stu-id="26ba0-184">85</span></span>

<span data-ttu-id="26ba0-185">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="26ba0-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-186">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="26ba0-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-187">86</span><span class="sxs-lookup"><span data-stu-id="26ba0-187">86</span></span>

<span data-ttu-id="26ba0-188">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="26ba0-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-189">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-190">87</span><span class="sxs-lookup"><span data-stu-id="26ba0-190">87</span></span>

<span data-ttu-id="26ba0-191">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-192">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="26ba0-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-193">88</span><span class="sxs-lookup"><span data-stu-id="26ba0-193">88</span></span>

<span data-ttu-id="26ba0-194">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="26ba0-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-195">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="26ba0-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-196">89</span><span class="sxs-lookup"><span data-stu-id="26ba0-196">89</span></span>

<span data-ttu-id="26ba0-197">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="26ba0-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-198">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="26ba0-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-199">90</span><span class="sxs-lookup"><span data-stu-id="26ba0-199">90</span></span>

<span data-ttu-id="26ba0-200">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="26ba0-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-201">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="26ba0-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-202">91</span><span class="sxs-lookup"><span data-stu-id="26ba0-202">91</span></span>

<span data-ttu-id="26ba0-203">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="26ba0-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-204">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="26ba0-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-205">92</span><span class="sxs-lookup"><span data-stu-id="26ba0-205">92</span></span>

<span data-ttu-id="26ba0-206">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="26ba0-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-207">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="26ba0-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-208">93</span><span class="sxs-lookup"><span data-stu-id="26ba0-208">93</span></span>

<span data-ttu-id="26ba0-209">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="26ba0-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-210">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="26ba0-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-211">94</span><span class="sxs-lookup"><span data-stu-id="26ba0-211">94</span></span>

<span data-ttu-id="26ba0-212">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="26ba0-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-213">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="26ba0-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-214">95</span><span class="sxs-lookup"><span data-stu-id="26ba0-214">95</span></span>

<span data-ttu-id="26ba0-215">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="26ba0-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-216">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="26ba0-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-217">96</span><span class="sxs-lookup"><span data-stu-id="26ba0-217">96</span></span>

<span data-ttu-id="26ba0-218">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="26ba0-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-219">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="26ba0-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-220">97</span><span class="sxs-lookup"><span data-stu-id="26ba0-220">97</span></span>

<span data-ttu-id="26ba0-221">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="26ba0-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-222">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="26ba0-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-223">98</span><span class="sxs-lookup"><span data-stu-id="26ba0-223">98</span></span>

<span data-ttu-id="26ba0-224">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="26ba0-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-225">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="26ba0-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-226">100</span><span class="sxs-lookup"><span data-stu-id="26ba0-226">100</span></span>

<span data-ttu-id="26ba0-227">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="26ba0-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="26ba0-228">**Autres**</span><span class="sxs-lookup"><span data-stu-id="26ba0-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="26ba0-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="26ba0-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26ba0-230">Notes</span><span class="sxs-lookup"><span data-stu-id="26ba0-230">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="26ba0-231">Si le protocole DHCP est activé sur le système de l’ordinateur local, l’option désactive TCP/IP sur cette carte réseau spécifique.</span><span class="sxs-lookup"><span data-stu-id="26ba0-231">If DHCP is enabled on the local computer system, the option disables TCP/IP on this specific network adapter.</span></span> <span data-ttu-id="26ba0-232">À moins que vous ne disposiez d’un autre chemin d’accès au système cible, autrement dit, une autre carte réseau TCP/IP, toutes les communications TCP/IP seront perdues.</span><span class="sxs-lookup"><span data-stu-id="26ba0-232">Unless you have an alternate path to the target system, that is, another TCP/IP bound network adapter, all TCP/IP communications will be lost.</span></span>

 

## <a name="examples"></a><span data-ttu-id="26ba0-233">Exemples</span><span class="sxs-lookup"><span data-stu-id="26ba0-233">Examples</span></span>

<span data-ttu-id="26ba0-234">La [version renouveler les adresses IP à l’aide](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) de PowerShell PowerShell dans la Galerie TechNet utilise **dispose ReleaseDHCPLease** pour publier et renouveler une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="26ba0-234">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **ReleaseDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="26ba0-235">Le code VBScript suivant libère les baux DHCP pour toutes les cartes réseau liées à TCP/IP sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="26ba0-235">The following VBScript code releases the DHCP leases for all TCP/IP-bound network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    objNetCard.ReleaseDHCPLease() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="26ba0-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26ba0-236">Requirements</span></span>



| <span data-ttu-id="26ba0-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26ba0-237">Requirement</span></span> | <span data-ttu-id="26ba0-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="26ba0-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26ba0-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ba0-239">Minimum supported client</span></span><br/> | <span data-ttu-id="26ba0-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26ba0-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26ba0-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ba0-241">Minimum supported server</span></span><br/> | <span data-ttu-id="26ba0-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26ba0-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26ba0-243">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="26ba0-243">Namespace</span></span><br/>                | <span data-ttu-id="26ba0-244">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="26ba0-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26ba0-245">MOF</span><span class="sxs-lookup"><span data-stu-id="26ba0-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26ba0-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26ba0-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26ba0-247">DLL</span><span class="sxs-lookup"><span data-stu-id="26ba0-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26ba0-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26ba0-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ba0-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26ba0-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ba0-250">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="26ba0-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="26ba0-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="26ba0-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="26ba0-252">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="26ba0-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="26ba0-253">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="26ba0-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="26ba0-254">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="26ba0-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

