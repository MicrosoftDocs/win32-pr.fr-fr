---
description: La méthode statique de la classe WMI SetArpUseEtherSNAP permet d’activer les paquets Ethernet pour utiliser l’encodage de l’alignement 802,3.
ms.assetid: 437954c0-ea6b-4559-a4cb-1f66630e70fe
ms.tgt_platform: multiple
title: Méthode SetArpUseEtherSNAP de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpUseEtherSNAP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52e3ce42948d5c40bbde3329b37ee3fa506c47ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861669"
---
# <a name="setarpuseethersnap-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="86d9e-103">Méthode SetArpUseEtherSNAP de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="86d9e-103">SetArpUseEtherSNAP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="86d9e-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetArpUseEtherSNAP** permet d’activer les paquets Ethernet pour utiliser l’encodage de l’alignement 802,3.</span><span class="sxs-lookup"><span data-stu-id="86d9e-104">The **SetArpUseEtherSNAP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable ethernet packets to use 802.3 SNAP encoding.</span></span>

<span data-ttu-id="86d9e-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="86d9e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="86d9e-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="86d9e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="86d9e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86d9e-107">Syntax</span></span>


```mof
uint32 SetArpUseEtherSNAP(
  [in] boolean ArpUseEtherSNAP
);
```



## <a name="parameters"></a><span data-ttu-id="86d9e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86d9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86d9e-109">*ArpUseEtherSNAP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86d9e-109">*ArpUseEtherSNAP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-110">Si la **valeur est true** , TCP/IP transmet les paquets Ethernet à l’aide de l’encodage Snap 802,3.</span><span class="sxs-lookup"><span data-stu-id="86d9e-110">If **true** enables TCP/IP to transmit Ethernet packets using 802.3 SNAP encoding.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86d9e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86d9e-111">Return value</span></span>

<span data-ttu-id="86d9e-112">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="86d9e-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="86d9e-113">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="86d9e-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="86d9e-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="86d9e-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="86d9e-115">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="86d9e-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-116">0</span><span class="sxs-lookup"><span data-stu-id="86d9e-116">0</span></span>

<span data-ttu-id="86d9e-117">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="86d9e-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-118">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="86d9e-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-119">1</span><span class="sxs-lookup"><span data-stu-id="86d9e-119">1</span></span>

<span data-ttu-id="86d9e-120">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="86d9e-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-121">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="86d9e-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-122">64</span><span class="sxs-lookup"><span data-stu-id="86d9e-122">64</span></span>

<span data-ttu-id="86d9e-123">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="86d9e-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-124">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="86d9e-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-125">65</span><span class="sxs-lookup"><span data-stu-id="86d9e-125">65</span></span>

<span data-ttu-id="86d9e-126">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="86d9e-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-127">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-128">66</span><span class="sxs-lookup"><span data-stu-id="86d9e-128">66</span></span>

<span data-ttu-id="86d9e-129">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-130">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="86d9e-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-131">67</span><span class="sxs-lookup"><span data-stu-id="86d9e-131">67</span></span>

<span data-ttu-id="86d9e-132">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="86d9e-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-133">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-134">68</span><span class="sxs-lookup"><span data-stu-id="86d9e-134">68</span></span>

<span data-ttu-id="86d9e-135">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-136">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="86d9e-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-137">69</span><span class="sxs-lookup"><span data-stu-id="86d9e-137">69</span></span>

<span data-ttu-id="86d9e-138">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="86d9e-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-139">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-140">70</span><span class="sxs-lookup"><span data-stu-id="86d9e-140">70</span></span>

<span data-ttu-id="86d9e-141">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-142">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-143">71</span><span class="sxs-lookup"><span data-stu-id="86d9e-143">71</span></span>

<span data-ttu-id="86d9e-144">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-145">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="86d9e-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-146">72</span><span class="sxs-lookup"><span data-stu-id="86d9e-146">72</span></span>

<span data-ttu-id="86d9e-147">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="86d9e-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-148">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-149">73</span><span class="sxs-lookup"><span data-stu-id="86d9e-149">73</span></span>

<span data-ttu-id="86d9e-150">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-151">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-152">74</span><span class="sxs-lookup"><span data-stu-id="86d9e-152">74</span></span>

<span data-ttu-id="86d9e-153">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-154">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="86d9e-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-155">75</span><span class="sxs-lookup"><span data-stu-id="86d9e-155">75</span></span>

<span data-ttu-id="86d9e-156">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="86d9e-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-157">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-158">76</span><span class="sxs-lookup"><span data-stu-id="86d9e-158">76</span></span>

<span data-ttu-id="86d9e-159">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-160">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-161">77</span><span class="sxs-lookup"><span data-stu-id="86d9e-161">77</span></span>

<span data-ttu-id="86d9e-162">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-163">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="86d9e-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-164">78</span><span class="sxs-lookup"><span data-stu-id="86d9e-164">78</span></span>

<span data-ttu-id="86d9e-165">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="86d9e-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-166">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-167">79</span><span class="sxs-lookup"><span data-stu-id="86d9e-167">79</span></span>

<span data-ttu-id="86d9e-168">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-169">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="86d9e-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-170">80</span><span class="sxs-lookup"><span data-stu-id="86d9e-170">80</span></span>

<span data-ttu-id="86d9e-171">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="86d9e-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-172">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="86d9e-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-173">81</span><span class="sxs-lookup"><span data-stu-id="86d9e-173">81</span></span>

<span data-ttu-id="86d9e-174">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="86d9e-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-175">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="86d9e-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-176">82</span><span class="sxs-lookup"><span data-stu-id="86d9e-176">82</span></span>

<span data-ttu-id="86d9e-177">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="86d9e-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-178">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="86d9e-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-179">83</span><span class="sxs-lookup"><span data-stu-id="86d9e-179">83</span></span>

<span data-ttu-id="86d9e-180">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="86d9e-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-181">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="86d9e-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-182">84</span><span class="sxs-lookup"><span data-stu-id="86d9e-182">84</span></span>

<span data-ttu-id="86d9e-183">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="86d9e-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-184">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="86d9e-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-185">85 %</span><span class="sxs-lookup"><span data-stu-id="86d9e-185">85</span></span>

<span data-ttu-id="86d9e-186">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="86d9e-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-187">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="86d9e-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-188">86</span><span class="sxs-lookup"><span data-stu-id="86d9e-188">86</span></span>

<span data-ttu-id="86d9e-189">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="86d9e-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-190">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-191">87</span><span class="sxs-lookup"><span data-stu-id="86d9e-191">87</span></span>

<span data-ttu-id="86d9e-192">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-193">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="86d9e-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-194">88</span><span class="sxs-lookup"><span data-stu-id="86d9e-194">88</span></span>

<span data-ttu-id="86d9e-195">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="86d9e-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-196">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="86d9e-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-197">89</span><span class="sxs-lookup"><span data-stu-id="86d9e-197">89</span></span>

<span data-ttu-id="86d9e-198">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="86d9e-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-199">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="86d9e-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-200">90</span><span class="sxs-lookup"><span data-stu-id="86d9e-200">90</span></span>

<span data-ttu-id="86d9e-201">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="86d9e-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-202">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="86d9e-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-203">91</span><span class="sxs-lookup"><span data-stu-id="86d9e-203">91</span></span>

<span data-ttu-id="86d9e-204">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="86d9e-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-205">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="86d9e-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-206">92</span><span class="sxs-lookup"><span data-stu-id="86d9e-206">92</span></span>

<span data-ttu-id="86d9e-207">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="86d9e-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-208">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="86d9e-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-209">93</span><span class="sxs-lookup"><span data-stu-id="86d9e-209">93</span></span>

<span data-ttu-id="86d9e-210">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="86d9e-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-211">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="86d9e-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-212">94</span><span class="sxs-lookup"><span data-stu-id="86d9e-212">94</span></span>

<span data-ttu-id="86d9e-213">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="86d9e-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-214">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="86d9e-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-215">95</span><span class="sxs-lookup"><span data-stu-id="86d9e-215">95</span></span>

<span data-ttu-id="86d9e-216">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="86d9e-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-217">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="86d9e-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-218">96</span><span class="sxs-lookup"><span data-stu-id="86d9e-218">96</span></span>

<span data-ttu-id="86d9e-219">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="86d9e-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-220">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="86d9e-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-221">97</span><span class="sxs-lookup"><span data-stu-id="86d9e-221">97</span></span>

<span data-ttu-id="86d9e-222">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="86d9e-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-223">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="86d9e-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-224">98</span><span class="sxs-lookup"><span data-stu-id="86d9e-224">98</span></span>

<span data-ttu-id="86d9e-225">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="86d9e-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-226">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="86d9e-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-227">100</span><span class="sxs-lookup"><span data-stu-id="86d9e-227">100</span></span>

<span data-ttu-id="86d9e-228">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="86d9e-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="86d9e-229">**Autres**</span><span class="sxs-lookup"><span data-stu-id="86d9e-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="86d9e-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="86d9e-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86d9e-231">Notes</span><span class="sxs-lookup"><span data-stu-id="86d9e-231">Remarks</span></span>

<span data-ttu-id="86d9e-232">Par défaut, la pile transmet les paquets au format Digital, Intel, Xerox (DIX) Ethernet.</span><span class="sxs-lookup"><span data-stu-id="86d9e-232">By default, the stack transmits packets in Digital, Intel, Xerox (DIX) Ethernet format.</span></span> <span data-ttu-id="86d9e-233">Elle reçoit toujours les deux formats.</span><span class="sxs-lookup"><span data-stu-id="86d9e-233">It always receives both formats.</span></span>

## <a name="examples"></a><span data-ttu-id="86d9e-234">Exemples</span><span class="sxs-lookup"><span data-stu-id="86d9e-234">Examples</span></span>

<span data-ttu-id="86d9e-235">L’exemple de code [modifier les requêtes ARP à utiliser EtherSNAP](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript sur la Galerie TechNet utilise **SetArpUseEtherSNAP** pour configurer les cartes réseau sur un ordinateur afin d’utiliser l’ENcodage de l’accrochage 802,3 pour les paquets Ethernet.</span><span class="sxs-lookup"><span data-stu-id="86d9e-235">The [Modify ARP Queries to Use EtherSNAP](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript code sample on TechNet Gallery uses **SetArpUseEtherSNAP** to configure the network adapters on a computer to use 802.3 SNAP encoding for Ethernet packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="86d9e-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86d9e-236">Requirements</span></span>



| <span data-ttu-id="86d9e-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86d9e-237">Requirement</span></span> | <span data-ttu-id="86d9e-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="86d9e-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86d9e-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86d9e-239">Minimum supported client</span></span><br/> | <span data-ttu-id="86d9e-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86d9e-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86d9e-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86d9e-241">Minimum supported server</span></span><br/> | <span data-ttu-id="86d9e-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86d9e-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86d9e-243">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="86d9e-243">Namespace</span></span><br/>                | <span data-ttu-id="86d9e-244">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="86d9e-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86d9e-245">MOF</span><span class="sxs-lookup"><span data-stu-id="86d9e-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86d9e-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86d9e-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86d9e-247">DLL</span><span class="sxs-lookup"><span data-stu-id="86d9e-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86d9e-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86d9e-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86d9e-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86d9e-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d9e-250">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="86d9e-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="86d9e-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="86d9e-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="86d9e-252">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="86d9e-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="86d9e-253">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="86d9e-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="86d9e-254">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="86d9e-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

