---
description: La méthode statique de la classe WMI SetTcpNumConnections permet de définir le nombre maximal de connexions ouvertes simultanément par TCP.
ms.assetid: 50458161-1f28-47f9-b395-09586e859d5d
ms.tgt_platform: multiple
title: Méthode SetTcpNumConnections de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpNumConnections
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5708c7ce80930c0924b560cc7b84e5af45ad7962
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110742"
---
# <a name="settcpnumconnections-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1d56a-103">Méthode SetTcpNumConnections de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d56a-103">SetTcpNumConnections method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1d56a-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpNumConnections** permet de définir le nombre maximal de connexions ouvertes simultanément par TCP.</span><span class="sxs-lookup"><span data-stu-id="1d56a-104">The **SetTcpNumConnections** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum number of connections that TCP may have open simultaneously.</span></span>

<span data-ttu-id="1d56a-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1d56a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1d56a-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1d56a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d56a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d56a-107">Syntax</span></span>


```mof
uint32 SetTcpNumConnections(
  [in] uint32 TcpNumConnections
);
```



## <a name="parameters"></a><span data-ttu-id="1d56a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d56a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d56a-109">*TcpNumConnections* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d56a-109">*TcpNumConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-110">Nombre maximal de connexions ouvertes simultanément par TCP.</span><span class="sxs-lookup"><span data-stu-id="1d56a-110">Maximum number of connections that TCP may have open simultaneously.</span></span> <span data-ttu-id="1d56a-111">La plage de valeurs valide est 0-0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="1d56a-111">The valid range of values is 0 - 0xFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d56a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d56a-112">Return value</span></span>

<span data-ttu-id="1d56a-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1d56a-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="1d56a-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1d56a-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1d56a-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1d56a-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1d56a-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="1d56a-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-117">0</span><span class="sxs-lookup"><span data-stu-id="1d56a-117">0</span></span>

<span data-ttu-id="1d56a-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1d56a-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="1d56a-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-120">1</span><span class="sxs-lookup"><span data-stu-id="1d56a-120">1</span></span>

<span data-ttu-id="1d56a-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="1d56a-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="1d56a-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-123">64</span><span class="sxs-lookup"><span data-stu-id="1d56a-123">64</span></span>

<span data-ttu-id="1d56a-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="1d56a-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="1d56a-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-126">65</span><span class="sxs-lookup"><span data-stu-id="1d56a-126">65</span></span>

<span data-ttu-id="1d56a-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="1d56a-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-129">66</span><span class="sxs-lookup"><span data-stu-id="1d56a-129">66</span></span>

<span data-ttu-id="1d56a-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="1d56a-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-132">67</span><span class="sxs-lookup"><span data-stu-id="1d56a-132">67</span></span>

<span data-ttu-id="1d56a-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="1d56a-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-135">68</span><span class="sxs-lookup"><span data-stu-id="1d56a-135">68</span></span>

<span data-ttu-id="1d56a-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="1d56a-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-138">69</span><span class="sxs-lookup"><span data-stu-id="1d56a-138">69</span></span>

<span data-ttu-id="1d56a-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1d56a-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-141">70</span><span class="sxs-lookup"><span data-stu-id="1d56a-141">70</span></span>

<span data-ttu-id="1d56a-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-144">71</span><span class="sxs-lookup"><span data-stu-id="1d56a-144">71</span></span>

<span data-ttu-id="1d56a-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="1d56a-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-147">72</span><span class="sxs-lookup"><span data-stu-id="1d56a-147">72</span></span>

<span data-ttu-id="1d56a-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="1d56a-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-150">73</span><span class="sxs-lookup"><span data-stu-id="1d56a-150">73</span></span>

<span data-ttu-id="1d56a-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-153">74</span><span class="sxs-lookup"><span data-stu-id="1d56a-153">74</span></span>

<span data-ttu-id="1d56a-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="1d56a-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-156">75</span><span class="sxs-lookup"><span data-stu-id="1d56a-156">75</span></span>

<span data-ttu-id="1d56a-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="1d56a-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-159">76</span><span class="sxs-lookup"><span data-stu-id="1d56a-159">76</span></span>

<span data-ttu-id="1d56a-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-162">77</span><span class="sxs-lookup"><span data-stu-id="1d56a-162">77</span></span>

<span data-ttu-id="1d56a-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="1d56a-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-165">78</span><span class="sxs-lookup"><span data-stu-id="1d56a-165">78</span></span>

<span data-ttu-id="1d56a-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="1d56a-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-168">79</span><span class="sxs-lookup"><span data-stu-id="1d56a-168">79</span></span>

<span data-ttu-id="1d56a-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="1d56a-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-171">80</span><span class="sxs-lookup"><span data-stu-id="1d56a-171">80</span></span>

<span data-ttu-id="1d56a-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1d56a-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="1d56a-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-174">81</span><span class="sxs-lookup"><span data-stu-id="1d56a-174">81</span></span>

<span data-ttu-id="1d56a-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="1d56a-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="1d56a-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-177">82</span><span class="sxs-lookup"><span data-stu-id="1d56a-177">82</span></span>

<span data-ttu-id="1d56a-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="1d56a-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="1d56a-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-180">83</span><span class="sxs-lookup"><span data-stu-id="1d56a-180">83</span></span>

<span data-ttu-id="1d56a-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="1d56a-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1d56a-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-183">84</span><span class="sxs-lookup"><span data-stu-id="1d56a-183">84</span></span>

<span data-ttu-id="1d56a-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1d56a-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1d56a-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-186">85 %</span><span class="sxs-lookup"><span data-stu-id="1d56a-186">85</span></span>

<span data-ttu-id="1d56a-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1d56a-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="1d56a-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-189">86</span><span class="sxs-lookup"><span data-stu-id="1d56a-189">86</span></span>

<span data-ttu-id="1d56a-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="1d56a-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-192">87</span><span class="sxs-lookup"><span data-stu-id="1d56a-192">87</span></span>

<span data-ttu-id="1d56a-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="1d56a-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-195">88</span><span class="sxs-lookup"><span data-stu-id="1d56a-195">88</span></span>

<span data-ttu-id="1d56a-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="1d56a-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="1d56a-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-198">89</span><span class="sxs-lookup"><span data-stu-id="1d56a-198">89</span></span>

<span data-ttu-id="1d56a-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="1d56a-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="1d56a-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-201">90</span><span class="sxs-lookup"><span data-stu-id="1d56a-201">90</span></span>

<span data-ttu-id="1d56a-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="1d56a-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="1d56a-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-204">91</span><span class="sxs-lookup"><span data-stu-id="1d56a-204">91</span></span>

<span data-ttu-id="1d56a-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="1d56a-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="1d56a-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-207">92</span><span class="sxs-lookup"><span data-stu-id="1d56a-207">92</span></span>

<span data-ttu-id="1d56a-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="1d56a-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="1d56a-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-210">93</span><span class="sxs-lookup"><span data-stu-id="1d56a-210">93</span></span>

<span data-ttu-id="1d56a-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="1d56a-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="1d56a-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-213">94</span><span class="sxs-lookup"><span data-stu-id="1d56a-213">94</span></span>

<span data-ttu-id="1d56a-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="1d56a-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="1d56a-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-216">95</span><span class="sxs-lookup"><span data-stu-id="1d56a-216">95</span></span>

<span data-ttu-id="1d56a-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="1d56a-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="1d56a-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-219">96</span><span class="sxs-lookup"><span data-stu-id="1d56a-219">96</span></span>

<span data-ttu-id="1d56a-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="1d56a-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="1d56a-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-222">97</span><span class="sxs-lookup"><span data-stu-id="1d56a-222">97</span></span>

<span data-ttu-id="1d56a-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="1d56a-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="1d56a-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-225">98</span><span class="sxs-lookup"><span data-stu-id="1d56a-225">98</span></span>

<span data-ttu-id="1d56a-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="1d56a-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1d56a-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-228">100</span><span class="sxs-lookup"><span data-stu-id="1d56a-228">100</span></span>

<span data-ttu-id="1d56a-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1d56a-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1d56a-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="1d56a-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1d56a-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="1d56a-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1d56a-232">Exemples</span><span class="sxs-lookup"><span data-stu-id="1d56a-232">Examples</span></span>

<span data-ttu-id="1d56a-233">L’exemple VBScript [de modification de nombre autorisé de connexions TCP](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) définit le nombre maximal autorisé de connexions TCP ouvertes simultanément sur un ordinateur à 10.</span><span class="sxs-lookup"><span data-stu-id="1d56a-233">The [Modify the Allowed Number of TCP Connections](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript sample sets the maximum allowed number of simultaneously-opened TCP connections on a computer to 10.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d56a-234">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d56a-234">Requirements</span></span>



| <span data-ttu-id="1d56a-235">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d56a-235">Requirement</span></span> | <span data-ttu-id="1d56a-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d56a-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d56a-237">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d56a-237">Minimum supported client</span></span><br/> | <span data-ttu-id="1d56a-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d56a-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d56a-239">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d56a-239">Minimum supported server</span></span><br/> | <span data-ttu-id="1d56a-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d56a-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d56a-241">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d56a-241">Namespace</span></span><br/>                | <span data-ttu-id="1d56a-242">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1d56a-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d56a-243">MOF</span><span class="sxs-lookup"><span data-stu-id="1d56a-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d56a-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d56a-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d56a-245">DLL</span><span class="sxs-lookup"><span data-stu-id="1d56a-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d56a-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d56a-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d56a-247">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d56a-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d56a-248">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="1d56a-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1d56a-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1d56a-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="1d56a-250">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="1d56a-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="1d56a-251">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="1d56a-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="1d56a-252">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="1d56a-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

