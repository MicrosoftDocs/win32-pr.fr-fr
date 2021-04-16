---
description: La méthode statique de la classe WMI SetDatabasePath définit le chemin d’accès aux fichiers de base de données Internet standard (hôtes, LMHOSTS, réseaux et protocoles).
ms.assetid: 373fef0f-9cdf-4785-8d73-3f00bbd60ae2
ms.tgt_platform: multiple
title: Méthode SetDatabasePath de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDatabasePath
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b66a9979ec97d4ceda16acad6488d3b84d5d3a54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524247"
---
# <a name="setdatabasepath-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="29445-103">Méthode SetDatabasePath de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="29445-103">SetDatabasePath method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="29445-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDatabasePath** définit le chemin d’accès aux fichiers de base de données Internet standard (hôtes, LMHOSTS, réseaux et protocoles).</span><span class="sxs-lookup"><span data-stu-id="29445-104">The **SetDatabasePath** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span>

<span data-ttu-id="29445-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="29445-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="29445-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="29445-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="29445-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29445-107">Syntax</span></span>


```mof
uint32 SetDatabasePath(
  [in] string DatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="29445-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29445-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29445-109">*DatabasePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29445-109">*DatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29445-110">Chemin d’accès de fichier valide aux fichiers de base de données Internet standard (hôtes, LMHOSTS, réseaux et protocoles) utilisé par l’interface Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="29445-110">Valid file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS) used by the Windows Sockets interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29445-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29445-111">Return value</span></span>

<span data-ttu-id="29445-112">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="29445-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, a different number if there is an error.</span></span> <span data-ttu-id="29445-113">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="29445-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="29445-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="29445-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="29445-115">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="29445-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="29445-116">0</span><span class="sxs-lookup"><span data-stu-id="29445-116">0</span></span>

<span data-ttu-id="29445-117">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="29445-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="29445-118">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="29445-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="29445-119">1</span><span class="sxs-lookup"><span data-stu-id="29445-119">1</span></span>

<span data-ttu-id="29445-120">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="29445-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="29445-121">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="29445-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="29445-122">64</span><span class="sxs-lookup"><span data-stu-id="29445-122">64</span></span>

<span data-ttu-id="29445-123">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="29445-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="29445-124">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="29445-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="29445-125">65</span><span class="sxs-lookup"><span data-stu-id="29445-125">65</span></span>

<span data-ttu-id="29445-126">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="29445-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="29445-127">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="29445-128">66</span><span class="sxs-lookup"><span data-stu-id="29445-128">66</span></span>

<span data-ttu-id="29445-129">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="29445-130">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="29445-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="29445-131">67</span><span class="sxs-lookup"><span data-stu-id="29445-131">67</span></span>

<span data-ttu-id="29445-132">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="29445-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="29445-133">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="29445-134">68</span><span class="sxs-lookup"><span data-stu-id="29445-134">68</span></span>

<span data-ttu-id="29445-135">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="29445-136">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="29445-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="29445-137">69</span><span class="sxs-lookup"><span data-stu-id="29445-137">69</span></span>

<span data-ttu-id="29445-138">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="29445-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="29445-139">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="29445-140">70</span><span class="sxs-lookup"><span data-stu-id="29445-140">70</span></span>

<span data-ttu-id="29445-141">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="29445-142">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="29445-143">71</span><span class="sxs-lookup"><span data-stu-id="29445-143">71</span></span>

<span data-ttu-id="29445-144">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="29445-145">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="29445-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="29445-146">72</span><span class="sxs-lookup"><span data-stu-id="29445-146">72</span></span>

<span data-ttu-id="29445-147">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="29445-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="29445-148">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="29445-149">73</span><span class="sxs-lookup"><span data-stu-id="29445-149">73</span></span>

<span data-ttu-id="29445-150">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="29445-151">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="29445-152">74</span><span class="sxs-lookup"><span data-stu-id="29445-152">74</span></span>

<span data-ttu-id="29445-153">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="29445-154">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="29445-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="29445-155">75</span><span class="sxs-lookup"><span data-stu-id="29445-155">75</span></span>

<span data-ttu-id="29445-156">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="29445-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="29445-157">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="29445-158">76</span><span class="sxs-lookup"><span data-stu-id="29445-158">76</span></span>

<span data-ttu-id="29445-159">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="29445-160">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="29445-161">77</span><span class="sxs-lookup"><span data-stu-id="29445-161">77</span></span>

<span data-ttu-id="29445-162">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="29445-163">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="29445-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="29445-164">78</span><span class="sxs-lookup"><span data-stu-id="29445-164">78</span></span>

<span data-ttu-id="29445-165">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="29445-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="29445-166">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="29445-167">79</span><span class="sxs-lookup"><span data-stu-id="29445-167">79</span></span>

<span data-ttu-id="29445-168">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="29445-169">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="29445-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="29445-170">80</span><span class="sxs-lookup"><span data-stu-id="29445-170">80</span></span>

<span data-ttu-id="29445-171">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="29445-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="29445-172">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="29445-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="29445-173">81</span><span class="sxs-lookup"><span data-stu-id="29445-173">81</span></span>

<span data-ttu-id="29445-174">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="29445-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="29445-175">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="29445-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="29445-176">82</span><span class="sxs-lookup"><span data-stu-id="29445-176">82</span></span>

<span data-ttu-id="29445-177">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="29445-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="29445-178">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="29445-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="29445-179">83</span><span class="sxs-lookup"><span data-stu-id="29445-179">83</span></span>

<span data-ttu-id="29445-180">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="29445-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="29445-181">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="29445-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="29445-182">84</span><span class="sxs-lookup"><span data-stu-id="29445-182">84</span></span>

<span data-ttu-id="29445-183">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="29445-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="29445-184">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="29445-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="29445-185">85 %</span><span class="sxs-lookup"><span data-stu-id="29445-185">85</span></span>

<span data-ttu-id="29445-186">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="29445-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="29445-187">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="29445-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="29445-188">86</span><span class="sxs-lookup"><span data-stu-id="29445-188">86</span></span>

<span data-ttu-id="29445-189">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="29445-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="29445-190">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="29445-191">87</span><span class="sxs-lookup"><span data-stu-id="29445-191">87</span></span>

<span data-ttu-id="29445-192">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="29445-193">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="29445-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="29445-194">88</span><span class="sxs-lookup"><span data-stu-id="29445-194">88</span></span>

<span data-ttu-id="29445-195">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="29445-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="29445-196">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="29445-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="29445-197">89</span><span class="sxs-lookup"><span data-stu-id="29445-197">89</span></span>

<span data-ttu-id="29445-198">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="29445-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="29445-199">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="29445-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="29445-200">90</span><span class="sxs-lookup"><span data-stu-id="29445-200">90</span></span>

<span data-ttu-id="29445-201">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="29445-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="29445-202">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="29445-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="29445-203">91</span><span class="sxs-lookup"><span data-stu-id="29445-203">91</span></span>

<span data-ttu-id="29445-204">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="29445-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="29445-205">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="29445-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="29445-206">92</span><span class="sxs-lookup"><span data-stu-id="29445-206">92</span></span>

<span data-ttu-id="29445-207">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="29445-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="29445-208">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="29445-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="29445-209">93</span><span class="sxs-lookup"><span data-stu-id="29445-209">93</span></span>

<span data-ttu-id="29445-210">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="29445-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="29445-211">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="29445-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="29445-212">94</span><span class="sxs-lookup"><span data-stu-id="29445-212">94</span></span>

<span data-ttu-id="29445-213">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="29445-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="29445-214">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="29445-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="29445-215">95</span><span class="sxs-lookup"><span data-stu-id="29445-215">95</span></span>

<span data-ttu-id="29445-216">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="29445-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="29445-217">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="29445-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="29445-218">96</span><span class="sxs-lookup"><span data-stu-id="29445-218">96</span></span>

<span data-ttu-id="29445-219">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="29445-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="29445-220">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="29445-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="29445-221">97</span><span class="sxs-lookup"><span data-stu-id="29445-221">97</span></span>

<span data-ttu-id="29445-222">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="29445-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="29445-223">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="29445-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="29445-224">98</span><span class="sxs-lookup"><span data-stu-id="29445-224">98</span></span>

<span data-ttu-id="29445-225">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="29445-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="29445-226">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="29445-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="29445-227">100</span><span class="sxs-lookup"><span data-stu-id="29445-227">100</span></span>

<span data-ttu-id="29445-228">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="29445-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="29445-229">**Autres**</span><span class="sxs-lookup"><span data-stu-id="29445-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="29445-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="29445-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29445-231">Notes</span><span class="sxs-lookup"><span data-stu-id="29445-231">Remarks</span></span>

<span data-ttu-id="29445-232">Cette méthode est utilisée par l’interface Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="29445-232">This method is used by the Windows Sockets interface.</span></span> <span data-ttu-id="29445-233">Le chemin d’accès par défaut est% SystemRoot% \\ system32 \\ drivers \\ .</span><span class="sxs-lookup"><span data-stu-id="29445-233">The default path is %SystemRoot%\\system32\\drivers\\ .</span></span>

## <a name="examples"></a><span data-ttu-id="29445-234">Exemples</span><span class="sxs-lookup"><span data-stu-id="29445-234">Examples</span></span>

<span data-ttu-id="29445-235">L’exemple VBScript [modifier le chemin d’accès de la base de données pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) de la Galerie TechNet utilise **SetDatabasePath** pour définir le chemin d’accès aux fichiers de base de données Internet standard (hôtes, LMHOSTS, réseaux, protocoles) utilisés par l’interface Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="29445-235">The [Modify the Database Path for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) VBScript sample on TechNet Gallery uses **SetDatabasePath** to set the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, PROTOCOLS) used by the Windows Sockets interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="29445-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29445-236">Requirements</span></span>



| <span data-ttu-id="29445-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29445-237">Requirement</span></span> | <span data-ttu-id="29445-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="29445-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29445-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29445-239">Minimum supported client</span></span><br/> | <span data-ttu-id="29445-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29445-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29445-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29445-241">Minimum supported server</span></span><br/> | <span data-ttu-id="29445-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29445-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29445-243">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29445-243">Namespace</span></span><br/>                | <span data-ttu-id="29445-244">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="29445-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="29445-245">MOF</span><span class="sxs-lookup"><span data-stu-id="29445-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29445-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29445-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="29445-247">DLL</span><span class="sxs-lookup"><span data-stu-id="29445-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29445-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29445-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29445-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29445-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29445-250">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="29445-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="29445-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="29445-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="29445-252">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="29445-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="29445-253">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="29445-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="29445-254">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="29445-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

