---
description: La méthode statique de la classe WMI SetTcpMaxDataRetransmissions est utilisée pour définir le nombre de fois que le protocole TCP retransmet un segment de données individuel avant d’abandonner la connexion.
ms.assetid: 1b5407ee-8e2b-4aed-a17a-58d960f976f2
ms.tgt_platform: multiple
title: Méthode SetTcpMaxDataRetransmissions de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxDataRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59998888eb2aed170b626fb4cb61780cbe0cb6e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111614"
---
# <a name="settcpmaxdataretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="7854b-103">Méthode SetTcpMaxDataRetransmissions de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="7854b-103">SetTcpMaxDataRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="7854b-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpMaxDataRetransmissions** est utilisée pour définir le nombre de fois que le protocole TCP retransmet un segment de données individuel avant d’abandonner la connexion.</span><span class="sxs-lookup"><span data-stu-id="7854b-104">The **SetTcpMaxDataRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of times TCP retransmits an individual data segment before aborting the connection.</span></span>

<span data-ttu-id="7854b-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="7854b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7854b-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7854b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7854b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7854b-107">Syntax</span></span>


```mof
uint32 SetTcpMaxDataRetransmissions(
  [in] uint32 TcpMaxDataRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="7854b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7854b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7854b-109">*TcpMaxDataRetransmissions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7854b-109">*TcpMaxDataRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7854b-110">Nombre de retransmissions d’un segment de données par TCP avant l’abandon de la connexion.</span><span class="sxs-lookup"><span data-stu-id="7854b-110">Number of times TCP retransmits an individual data segment before aborting the connection.</span></span> <span data-ttu-id="7854b-111">Plage valide : 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="7854b-111">Valid range: 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7854b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7854b-112">Return value</span></span>

<span data-ttu-id="7854b-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7854b-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="7854b-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7854b-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7854b-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7854b-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7854b-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="7854b-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-117">0</span><span class="sxs-lookup"><span data-stu-id="7854b-117">0</span></span>

<span data-ttu-id="7854b-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7854b-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="7854b-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-120">1</span><span class="sxs-lookup"><span data-stu-id="7854b-120">1</span></span>

<span data-ttu-id="7854b-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="7854b-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="7854b-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-123">64</span><span class="sxs-lookup"><span data-stu-id="7854b-123">64</span></span>

<span data-ttu-id="7854b-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="7854b-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="7854b-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-126">65</span><span class="sxs-lookup"><span data-stu-id="7854b-126">65</span></span>

<span data-ttu-id="7854b-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="7854b-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-129">66</span><span class="sxs-lookup"><span data-stu-id="7854b-129">66</span></span>

<span data-ttu-id="7854b-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="7854b-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-132">67</span><span class="sxs-lookup"><span data-stu-id="7854b-132">67</span></span>

<span data-ttu-id="7854b-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="7854b-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-135">68</span><span class="sxs-lookup"><span data-stu-id="7854b-135">68</span></span>

<span data-ttu-id="7854b-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="7854b-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-138">69</span><span class="sxs-lookup"><span data-stu-id="7854b-138">69</span></span>

<span data-ttu-id="7854b-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="7854b-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-141">70</span><span class="sxs-lookup"><span data-stu-id="7854b-141">70</span></span>

<span data-ttu-id="7854b-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-144">71</span><span class="sxs-lookup"><span data-stu-id="7854b-144">71</span></span>

<span data-ttu-id="7854b-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="7854b-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-147">72</span><span class="sxs-lookup"><span data-stu-id="7854b-147">72</span></span>

<span data-ttu-id="7854b-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="7854b-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-150">73</span><span class="sxs-lookup"><span data-stu-id="7854b-150">73</span></span>

<span data-ttu-id="7854b-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-153">74</span><span class="sxs-lookup"><span data-stu-id="7854b-153">74</span></span>

<span data-ttu-id="7854b-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="7854b-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-156">75</span><span class="sxs-lookup"><span data-stu-id="7854b-156">75</span></span>

<span data-ttu-id="7854b-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="7854b-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-159">76</span><span class="sxs-lookup"><span data-stu-id="7854b-159">76</span></span>

<span data-ttu-id="7854b-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-162">77</span><span class="sxs-lookup"><span data-stu-id="7854b-162">77</span></span>

<span data-ttu-id="7854b-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="7854b-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-165">78</span><span class="sxs-lookup"><span data-stu-id="7854b-165">78</span></span>

<span data-ttu-id="7854b-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="7854b-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-168">79</span><span class="sxs-lookup"><span data-stu-id="7854b-168">79</span></span>

<span data-ttu-id="7854b-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="7854b-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-171">80</span><span class="sxs-lookup"><span data-stu-id="7854b-171">80</span></span>

<span data-ttu-id="7854b-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7854b-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="7854b-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-174">81</span><span class="sxs-lookup"><span data-stu-id="7854b-174">81</span></span>

<span data-ttu-id="7854b-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="7854b-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="7854b-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-177">82</span><span class="sxs-lookup"><span data-stu-id="7854b-177">82</span></span>

<span data-ttu-id="7854b-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="7854b-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="7854b-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-180">83</span><span class="sxs-lookup"><span data-stu-id="7854b-180">83</span></span>

<span data-ttu-id="7854b-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="7854b-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="7854b-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-183">84</span><span class="sxs-lookup"><span data-stu-id="7854b-183">84</span></span>

<span data-ttu-id="7854b-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="7854b-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="7854b-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-186">85 %</span><span class="sxs-lookup"><span data-stu-id="7854b-186">85</span></span>

<span data-ttu-id="7854b-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="7854b-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="7854b-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-189">86</span><span class="sxs-lookup"><span data-stu-id="7854b-189">86</span></span>

<span data-ttu-id="7854b-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="7854b-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-192">87</span><span class="sxs-lookup"><span data-stu-id="7854b-192">87</span></span>

<span data-ttu-id="7854b-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="7854b-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-195">88</span><span class="sxs-lookup"><span data-stu-id="7854b-195">88</span></span>

<span data-ttu-id="7854b-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="7854b-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="7854b-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-198">89</span><span class="sxs-lookup"><span data-stu-id="7854b-198">89</span></span>

<span data-ttu-id="7854b-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="7854b-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="7854b-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-201">90</span><span class="sxs-lookup"><span data-stu-id="7854b-201">90</span></span>

<span data-ttu-id="7854b-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="7854b-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="7854b-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-204">91</span><span class="sxs-lookup"><span data-stu-id="7854b-204">91</span></span>

<span data-ttu-id="7854b-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="7854b-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="7854b-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-207">92</span><span class="sxs-lookup"><span data-stu-id="7854b-207">92</span></span>

<span data-ttu-id="7854b-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="7854b-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="7854b-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-210">93</span><span class="sxs-lookup"><span data-stu-id="7854b-210">93</span></span>

<span data-ttu-id="7854b-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="7854b-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="7854b-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-213">94</span><span class="sxs-lookup"><span data-stu-id="7854b-213">94</span></span>

<span data-ttu-id="7854b-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="7854b-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="7854b-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-216">95</span><span class="sxs-lookup"><span data-stu-id="7854b-216">95</span></span>

<span data-ttu-id="7854b-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="7854b-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="7854b-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-219">96</span><span class="sxs-lookup"><span data-stu-id="7854b-219">96</span></span>

<span data-ttu-id="7854b-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="7854b-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="7854b-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-222">97</span><span class="sxs-lookup"><span data-stu-id="7854b-222">97</span></span>

<span data-ttu-id="7854b-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="7854b-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="7854b-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-225">98</span><span class="sxs-lookup"><span data-stu-id="7854b-225">98</span></span>

<span data-ttu-id="7854b-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="7854b-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="7854b-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-228">100</span><span class="sxs-lookup"><span data-stu-id="7854b-228">100</span></span>

<span data-ttu-id="7854b-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="7854b-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7854b-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="7854b-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="7854b-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="7854b-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7854b-232">Notes</span><span class="sxs-lookup"><span data-stu-id="7854b-232">Remarks</span></span>

<span data-ttu-id="7854b-233">Le délai de retransmission double à chaque retransmission successive sur une connexion.</span><span class="sxs-lookup"><span data-stu-id="7854b-233">The retransmission timeout doubles with each successive retransmission on a connection.</span></span>

## <a name="examples"></a><span data-ttu-id="7854b-234">Exemples</span><span class="sxs-lookup"><span data-stu-id="7854b-234">Examples</span></span>

<span data-ttu-id="7854b-235">L’exemple VBScript de [modification de la taille maximale autorisée de retransmission de données TCP](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) configure le nombre de tentatives de retransmission d’un segment de données individuel par TCP, avant d’abandonner l’effort.</span><span class="sxs-lookup"><span data-stu-id="7854b-235">The [Modify the Maximum Allowed TCP Data Retransmissions](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) VBScript sample configures the number of times TCP will attempt to retransmit an individual data segment before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="7854b-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7854b-236">Requirements</span></span>



| <span data-ttu-id="7854b-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7854b-237">Requirement</span></span> | <span data-ttu-id="7854b-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="7854b-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7854b-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7854b-239">Minimum supported client</span></span><br/> | <span data-ttu-id="7854b-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7854b-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="7854b-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7854b-241">Minimum supported server</span></span><br/> | <span data-ttu-id="7854b-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7854b-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="7854b-243">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7854b-243">Namespace</span></span><br/>                | <span data-ttu-id="7854b-244">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7854b-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7854b-245">MOF</span><span class="sxs-lookup"><span data-stu-id="7854b-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7854b-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7854b-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7854b-247">DLL</span><span class="sxs-lookup"><span data-stu-id="7854b-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7854b-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7854b-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7854b-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7854b-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7854b-250">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="7854b-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7854b-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="7854b-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="7854b-252">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="7854b-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="7854b-253">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="7854b-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="7854b-254">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="7854b-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

