---
description: La méthode statique de la classe WMI SetTcpMaxConnectRetransmissions est utilisée pour définir le nombre de tentatives que TCP retransmet une demande de connexion avant d’abandonner.
ms.assetid: cb0dfba3-4ef5-4052-94f3-f688a1c55d90
ms.tgt_platform: multiple
title: Méthode SetTcpMaxConnectRetransmissions de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxConnectRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 160d84c2a466bff34070a6dec4a34804d5a3a7fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111615"
---
# <a name="settcpmaxconnectretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8b0ac-103">Méthode SetTcpMaxConnectRetransmissions de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b0ac-103">SetTcpMaxConnectRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8b0ac-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpMaxConnectRetransmissions** est utilisée pour définir le nombre de tentatives que TCP retransmet une demande de connexion avant d’abandonner.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-104">The **SetTcpMaxConnectRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of attempts TCP will retransmit a connect request before aborting.</span></span>

<span data-ttu-id="8b0ac-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8b0ac-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8b0ac-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8b0ac-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0ac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b0ac-107">Syntax</span></span>


```mof
uint32 SetTcpMaxConnectRetransmissions(
  [in] uint32 TcpMaxConnectRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="8b0ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b0ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b0ac-109">*TcpMaxConnectRetransmissions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b0ac-109">*TcpMaxConnectRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-110">Nombre de tentatives que TCP retransmet une demande de connexion avant d’abandonner.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-110">Number of attempts TCP will retransmit a connect request before aborting.</span></span> <span data-ttu-id="8b0ac-111">La plage valide pour les valeurs est 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-111">The valid range for values is 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b0ac-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b0ac-112">Return value</span></span>

<span data-ttu-id="8b0ac-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="8b0ac-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8b0ac-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8b0ac-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8b0ac-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8b0ac-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-117">0</span><span class="sxs-lookup"><span data-stu-id="8b0ac-117">0</span></span>

<span data-ttu-id="8b0ac-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-120">1</span><span class="sxs-lookup"><span data-stu-id="8b0ac-120">1</span></span>

<span data-ttu-id="8b0ac-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-123">64</span><span class="sxs-lookup"><span data-stu-id="8b0ac-123">64</span></span>

<span data-ttu-id="8b0ac-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-126">65</span><span class="sxs-lookup"><span data-stu-id="8b0ac-126">65</span></span>

<span data-ttu-id="8b0ac-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-129">66</span><span class="sxs-lookup"><span data-stu-id="8b0ac-129">66</span></span>

<span data-ttu-id="8b0ac-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-132">67</span><span class="sxs-lookup"><span data-stu-id="8b0ac-132">67</span></span>

<span data-ttu-id="8b0ac-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-135">68</span><span class="sxs-lookup"><span data-stu-id="8b0ac-135">68</span></span>

<span data-ttu-id="8b0ac-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-138">69</span><span class="sxs-lookup"><span data-stu-id="8b0ac-138">69</span></span>

<span data-ttu-id="8b0ac-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-141">70</span><span class="sxs-lookup"><span data-stu-id="8b0ac-141">70</span></span>

<span data-ttu-id="8b0ac-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-144">71</span><span class="sxs-lookup"><span data-stu-id="8b0ac-144">71</span></span>

<span data-ttu-id="8b0ac-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-147">72</span><span class="sxs-lookup"><span data-stu-id="8b0ac-147">72</span></span>

<span data-ttu-id="8b0ac-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-150">73</span><span class="sxs-lookup"><span data-stu-id="8b0ac-150">73</span></span>

<span data-ttu-id="8b0ac-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-153">74</span><span class="sxs-lookup"><span data-stu-id="8b0ac-153">74</span></span>

<span data-ttu-id="8b0ac-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-156">75</span><span class="sxs-lookup"><span data-stu-id="8b0ac-156">75</span></span>

<span data-ttu-id="8b0ac-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-159">76</span><span class="sxs-lookup"><span data-stu-id="8b0ac-159">76</span></span>

<span data-ttu-id="8b0ac-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-162">77</span><span class="sxs-lookup"><span data-stu-id="8b0ac-162">77</span></span>

<span data-ttu-id="8b0ac-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-165">78</span><span class="sxs-lookup"><span data-stu-id="8b0ac-165">78</span></span>

<span data-ttu-id="8b0ac-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-168">79</span><span class="sxs-lookup"><span data-stu-id="8b0ac-168">79</span></span>

<span data-ttu-id="8b0ac-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-171">80</span><span class="sxs-lookup"><span data-stu-id="8b0ac-171">80</span></span>

<span data-ttu-id="8b0ac-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-174">81</span><span class="sxs-lookup"><span data-stu-id="8b0ac-174">81</span></span>

<span data-ttu-id="8b0ac-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-177">82</span><span class="sxs-lookup"><span data-stu-id="8b0ac-177">82</span></span>

<span data-ttu-id="8b0ac-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-180">83</span><span class="sxs-lookup"><span data-stu-id="8b0ac-180">83</span></span>

<span data-ttu-id="8b0ac-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-183">84</span><span class="sxs-lookup"><span data-stu-id="8b0ac-183">84</span></span>

<span data-ttu-id="8b0ac-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-186">85 %</span><span class="sxs-lookup"><span data-stu-id="8b0ac-186">85</span></span>

<span data-ttu-id="8b0ac-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-189">86</span><span class="sxs-lookup"><span data-stu-id="8b0ac-189">86</span></span>

<span data-ttu-id="8b0ac-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-192">87</span><span class="sxs-lookup"><span data-stu-id="8b0ac-192">87</span></span>

<span data-ttu-id="8b0ac-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-195">88</span><span class="sxs-lookup"><span data-stu-id="8b0ac-195">88</span></span>

<span data-ttu-id="8b0ac-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-198">89</span><span class="sxs-lookup"><span data-stu-id="8b0ac-198">89</span></span>

<span data-ttu-id="8b0ac-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-201">90</span><span class="sxs-lookup"><span data-stu-id="8b0ac-201">90</span></span>

<span data-ttu-id="8b0ac-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-204">91</span><span class="sxs-lookup"><span data-stu-id="8b0ac-204">91</span></span>

<span data-ttu-id="8b0ac-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-207">92</span><span class="sxs-lookup"><span data-stu-id="8b0ac-207">92</span></span>

<span data-ttu-id="8b0ac-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-210">93</span><span class="sxs-lookup"><span data-stu-id="8b0ac-210">93</span></span>

<span data-ttu-id="8b0ac-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-213">94</span><span class="sxs-lookup"><span data-stu-id="8b0ac-213">94</span></span>

<span data-ttu-id="8b0ac-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-216">95</span><span class="sxs-lookup"><span data-stu-id="8b0ac-216">95</span></span>

<span data-ttu-id="8b0ac-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-219">96</span><span class="sxs-lookup"><span data-stu-id="8b0ac-219">96</span></span>

<span data-ttu-id="8b0ac-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-222">97</span><span class="sxs-lookup"><span data-stu-id="8b0ac-222">97</span></span>

<span data-ttu-id="8b0ac-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-225">98</span><span class="sxs-lookup"><span data-stu-id="8b0ac-225">98</span></span>

<span data-ttu-id="8b0ac-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-228">100</span><span class="sxs-lookup"><span data-stu-id="8b0ac-228">100</span></span>

<span data-ttu-id="8b0ac-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8b0ac-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8b0ac-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8b0ac-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b0ac-232">Notes</span><span class="sxs-lookup"><span data-stu-id="8b0ac-232">Remarks</span></span>

<span data-ttu-id="8b0ac-233">Le délai de retransmission initial est de trois secondes, et double pour chaque tentative successive.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-233">The initial retransmission timeout is three seconds, and doubles for each successive attempt.</span></span>

## <a name="examples"></a><span data-ttu-id="8b0ac-234">Exemples</span><span class="sxs-lookup"><span data-stu-id="8b0ac-234">Examples</span></span>

<span data-ttu-id="8b0ac-235">L’exemple VBScript de [modification de la connexion TCP maximale autorisée](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) configure le nombre de fois que TCP retransmet une tentative de connexion avant d’abandonner l’effort.</span><span class="sxs-lookup"><span data-stu-id="8b0ac-235">The [Modify the Maximum Allowed TCP Connection Retransmissions](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) VBScript sample configures the number of times TCP will retransmit a connection attempt before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b0ac-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b0ac-236">Requirements</span></span>



| <span data-ttu-id="8b0ac-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b0ac-237">Requirement</span></span> | <span data-ttu-id="8b0ac-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b0ac-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0ac-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b0ac-239">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0ac-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b0ac-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="8b0ac-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b0ac-241">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0ac-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b0ac-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="8b0ac-243">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8b0ac-243">Namespace</span></span><br/>                | <span data-ttu-id="8b0ac-244">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8b0ac-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b0ac-245">MOF</span><span class="sxs-lookup"><span data-stu-id="8b0ac-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b0ac-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b0ac-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b0ac-247">DLL</span><span class="sxs-lookup"><span data-stu-id="8b0ac-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b0ac-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b0ac-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b0ac-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b0ac-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0ac-250">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="8b0ac-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8b0ac-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="8b0ac-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8b0ac-252">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="8b0ac-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8b0ac-253">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="8b0ac-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8b0ac-254">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="8b0ac-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

