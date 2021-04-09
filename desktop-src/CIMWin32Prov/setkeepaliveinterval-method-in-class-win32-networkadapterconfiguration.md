---
description: La méthode statique de la classe WMI SetKeepAliveInterval est utilisée pour définir l’intervalle séparant les retransmissions de la fonction Keep Alive jusqu’à la réception d’une réponse.
ms.assetid: 83415000-124a-44a7-93cc-92ce9df143aa
ms.tgt_platform: multiple
title: Méthode SetKeepAliveInterval de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveInterval
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ce6a1491fd9e414f503d0165216794c67db0e97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110943"
---
# <a name="setkeepaliveinterval-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="cd046-103">Méthode SetKeepAliveInterval de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd046-103">SetKeepAliveInterval method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="cd046-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetKeepAliveInterval** est utilisée pour définir l’intervalle séparant les retransmissions de la fonction Keep Alive jusqu’à la réception d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="cd046-104">The **SetKeepAliveInterval** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the interval separating Keep Alive Retransmissions until a response is received.</span></span>

<span data-ttu-id="cd046-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="cd046-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cd046-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cd046-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd046-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd046-107">Syntax</span></span>


```mof
uint32 SetKeepAliveInterval(
  [in] uint32 KeepAliveInterval
);
```



## <a name="parameters"></a><span data-ttu-id="cd046-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd046-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd046-109">*KeepAliveInterval* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd046-109">*KeepAliveInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd046-110">Valeur, en millisecondes, de l’intervalle qui sépare les retransmissions KeepAlive jusqu’à ce qu’une réponse soit reçue.</span><span class="sxs-lookup"><span data-stu-id="cd046-110">Value, in milliseconds, for the interval separating Keep Alive Retransmissions until a response is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd046-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd046-111">Return value</span></span>

<span data-ttu-id="cd046-112">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="cd046-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="cd046-113">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cd046-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cd046-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cd046-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cd046-115">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="cd046-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-116">0</span><span class="sxs-lookup"><span data-stu-id="cd046-116">0</span></span>

<span data-ttu-id="cd046-117">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cd046-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-118">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="cd046-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-119">1</span><span class="sxs-lookup"><span data-stu-id="cd046-119">1</span></span>

<span data-ttu-id="cd046-120">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="cd046-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-121">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="cd046-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-122">64</span><span class="sxs-lookup"><span data-stu-id="cd046-122">64</span></span>

<span data-ttu-id="cd046-123">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="cd046-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-124">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="cd046-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-125">65</span><span class="sxs-lookup"><span data-stu-id="cd046-125">65</span></span>

<span data-ttu-id="cd046-126">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="cd046-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-127">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-128">66</span><span class="sxs-lookup"><span data-stu-id="cd046-128">66</span></span>

<span data-ttu-id="cd046-129">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-130">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="cd046-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-131">67</span><span class="sxs-lookup"><span data-stu-id="cd046-131">67</span></span>

<span data-ttu-id="cd046-132">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="cd046-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-133">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-134">68</span><span class="sxs-lookup"><span data-stu-id="cd046-134">68</span></span>

<span data-ttu-id="cd046-135">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-136">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="cd046-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-137">69</span><span class="sxs-lookup"><span data-stu-id="cd046-137">69</span></span>

<span data-ttu-id="cd046-138">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="cd046-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-139">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-140">70</span><span class="sxs-lookup"><span data-stu-id="cd046-140">70</span></span>

<span data-ttu-id="cd046-141">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-142">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-143">71</span><span class="sxs-lookup"><span data-stu-id="cd046-143">71</span></span>

<span data-ttu-id="cd046-144">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-145">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="cd046-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-146">72</span><span class="sxs-lookup"><span data-stu-id="cd046-146">72</span></span>

<span data-ttu-id="cd046-147">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="cd046-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-148">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-149">73</span><span class="sxs-lookup"><span data-stu-id="cd046-149">73</span></span>

<span data-ttu-id="cd046-150">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-151">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-152">74</span><span class="sxs-lookup"><span data-stu-id="cd046-152">74</span></span>

<span data-ttu-id="cd046-153">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-154">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="cd046-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-155">75</span><span class="sxs-lookup"><span data-stu-id="cd046-155">75</span></span>

<span data-ttu-id="cd046-156">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="cd046-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-157">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-158">76</span><span class="sxs-lookup"><span data-stu-id="cd046-158">76</span></span>

<span data-ttu-id="cd046-159">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-160">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-161">77</span><span class="sxs-lookup"><span data-stu-id="cd046-161">77</span></span>

<span data-ttu-id="cd046-162">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-163">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="cd046-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-164">78</span><span class="sxs-lookup"><span data-stu-id="cd046-164">78</span></span>

<span data-ttu-id="cd046-165">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="cd046-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-166">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-167">79</span><span class="sxs-lookup"><span data-stu-id="cd046-167">79</span></span>

<span data-ttu-id="cd046-168">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-169">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="cd046-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-170">80</span><span class="sxs-lookup"><span data-stu-id="cd046-170">80</span></span>

<span data-ttu-id="cd046-171">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="cd046-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-172">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="cd046-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-173">81</span><span class="sxs-lookup"><span data-stu-id="cd046-173">81</span></span>

<span data-ttu-id="cd046-174">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="cd046-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-175">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="cd046-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-176">82</span><span class="sxs-lookup"><span data-stu-id="cd046-176">82</span></span>

<span data-ttu-id="cd046-177">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="cd046-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-178">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="cd046-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-179">83</span><span class="sxs-lookup"><span data-stu-id="cd046-179">83</span></span>

<span data-ttu-id="cd046-180">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="cd046-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-181">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="cd046-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-182">84</span><span class="sxs-lookup"><span data-stu-id="cd046-182">84</span></span>

<span data-ttu-id="cd046-183">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="cd046-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-184">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="cd046-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-185">85 %</span><span class="sxs-lookup"><span data-stu-id="cd046-185">85</span></span>

<span data-ttu-id="cd046-186">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="cd046-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-187">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="cd046-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-188">86</span><span class="sxs-lookup"><span data-stu-id="cd046-188">86</span></span>

<span data-ttu-id="cd046-189">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="cd046-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-190">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-191">87</span><span class="sxs-lookup"><span data-stu-id="cd046-191">87</span></span>

<span data-ttu-id="cd046-192">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-193">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="cd046-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-194">88</span><span class="sxs-lookup"><span data-stu-id="cd046-194">88</span></span>

<span data-ttu-id="cd046-195">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="cd046-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-196">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="cd046-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-197">89</span><span class="sxs-lookup"><span data-stu-id="cd046-197">89</span></span>

<span data-ttu-id="cd046-198">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="cd046-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-199">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="cd046-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-200">90</span><span class="sxs-lookup"><span data-stu-id="cd046-200">90</span></span>

<span data-ttu-id="cd046-201">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="cd046-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-202">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="cd046-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-203">91</span><span class="sxs-lookup"><span data-stu-id="cd046-203">91</span></span>

<span data-ttu-id="cd046-204">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="cd046-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-205">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="cd046-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-206">92</span><span class="sxs-lookup"><span data-stu-id="cd046-206">92</span></span>

<span data-ttu-id="cd046-207">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="cd046-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-208">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="cd046-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-209">93</span><span class="sxs-lookup"><span data-stu-id="cd046-209">93</span></span>

<span data-ttu-id="cd046-210">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="cd046-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-211">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="cd046-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-212">94</span><span class="sxs-lookup"><span data-stu-id="cd046-212">94</span></span>

<span data-ttu-id="cd046-213">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="cd046-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-214">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="cd046-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-215">95</span><span class="sxs-lookup"><span data-stu-id="cd046-215">95</span></span>

<span data-ttu-id="cd046-216">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="cd046-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-217">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="cd046-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-218">96</span><span class="sxs-lookup"><span data-stu-id="cd046-218">96</span></span>

<span data-ttu-id="cd046-219">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="cd046-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-220">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="cd046-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-221">97</span><span class="sxs-lookup"><span data-stu-id="cd046-221">97</span></span>

<span data-ttu-id="cd046-222">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="cd046-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-223">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="cd046-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-224">98</span><span class="sxs-lookup"><span data-stu-id="cd046-224">98</span></span>

<span data-ttu-id="cd046-225">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="cd046-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-226">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="cd046-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-227">100</span><span class="sxs-lookup"><span data-stu-id="cd046-227">100</span></span>

<span data-ttu-id="cd046-228">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="cd046-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cd046-229">**Autres**</span><span class="sxs-lookup"><span data-stu-id="cd046-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="cd046-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="cd046-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd046-231">Notes</span><span class="sxs-lookup"><span data-stu-id="cd046-231">Remarks</span></span>

<span data-ttu-id="cd046-232">Après la réception d’une réponse, le délai jusqu’à ce que la transmission Keep Alive suivante soit de nouveau contrôlé par la valeur de la propriété [**keepAliveTime**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="cd046-232">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of the [**KeepAliveTime**](win32-networkadapterconfiguration.md) property.</span></span> <span data-ttu-id="cd046-233">La connexion est terminée une fois que le nombre de retransmissions spécifié par la propriété **TcpMaxDataRetransmissions** n’a pas répondu.</span><span class="sxs-lookup"><span data-stu-id="cd046-233">The connection is terminated after the number of retransmissions specified by the **TcpMaxDataRetransmissions** property have gone unanswered</span></span>

## <a name="examples"></a><span data-ttu-id="cd046-234">Exemples</span><span class="sxs-lookup"><span data-stu-id="cd046-234">Examples</span></span>

<span data-ttu-id="cd046-235">L’exemple de [modification de l’intervalle de maintien de la connexion pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) configure l’intervalle de maintien de l’activité pour toutes les cartes réseau d’un ordinateur à 300 millisecondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="cd046-235">The [Modify the Keep Alive Interval for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) VBScript sample configures the keep alive interval for all network adapters on a computer to 300,00 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd046-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd046-236">Requirements</span></span>



| <span data-ttu-id="cd046-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd046-237">Requirement</span></span> | <span data-ttu-id="cd046-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd046-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd046-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd046-239">Minimum supported client</span></span><br/> | <span data-ttu-id="cd046-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd046-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd046-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd046-241">Minimum supported server</span></span><br/> | <span data-ttu-id="cd046-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd046-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd046-243">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cd046-243">Namespace</span></span><br/>                | <span data-ttu-id="cd046-244">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="cd046-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd046-245">MOF</span><span class="sxs-lookup"><span data-stu-id="cd046-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd046-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd046-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd046-247">DLL</span><span class="sxs-lookup"><span data-stu-id="cd046-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd046-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd046-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd046-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd046-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd046-250">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="cd046-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="cd046-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="cd046-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="cd046-252">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="cd046-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="cd046-253">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="cd046-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="cd046-254">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="cd046-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

