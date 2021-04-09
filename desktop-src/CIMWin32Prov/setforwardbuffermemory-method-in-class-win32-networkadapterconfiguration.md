---
description: La méthode statique de la classe WMI SetForwardBufferMemory permet de spécifier la quantité de mémoire allouée par l’adresse IP pour stocker les données de paquets dans la file d’attente de paquets du routeur.
ms.assetid: e76452e8-2ee8-4d39-9405-33b0aeeac74d
ms.tgt_platform: multiple
title: Méthode SetForwardBufferMemory de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetForwardBufferMemory
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 30179610e6eee121a86119fa347067b40ef04c2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861318"
---
# <a name="setforwardbuffermemory-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="5513f-103">Méthode SetForwardBufferMemory de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="5513f-103">SetForwardBufferMemory method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="5513f-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetForwardBufferMemory** permet de spécifier la quantité de mémoire allouée par l’adresse IP pour stocker les données de paquets dans la file d’attente de paquets du routeur.</span><span class="sxs-lookup"><span data-stu-id="5513f-104">The **SetForwardBufferMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify how much memory IP allocates to store packet data in the router packet queue.</span></span>

<span data-ttu-id="5513f-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5513f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5513f-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5513f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5513f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5513f-107">Syntax</span></span>


```mof
uint32 SetForwardBufferMemory(
  [in] uint32 ForwardBufferMemory
);
```



## <a name="parameters"></a><span data-ttu-id="5513f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5513f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5513f-109">*ForwardBufferMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5513f-109">*ForwardBufferMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5513f-110">Taille, en octets, de la file d’attente de paquets du routeur utilisée pour stocker les données du paquet.</span><span class="sxs-lookup"><span data-stu-id="5513f-110">Size, in bytes, of the router packet queue used to store packet data.</span></span> <span data-ttu-id="5513f-111">La valeur par défaut est 74240 (paquets de 50 1480 octets, arrondis à un multiple de 256).</span><span class="sxs-lookup"><span data-stu-id="5513f-111">The default value is 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5513f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5513f-112">Return value</span></span>

<span data-ttu-id="5513f-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5513f-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="5513f-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5513f-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5513f-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5513f-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5513f-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="5513f-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-117">0</span><span class="sxs-lookup"><span data-stu-id="5513f-117">0</span></span>

<span data-ttu-id="5513f-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5513f-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="5513f-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-120">1</span><span class="sxs-lookup"><span data-stu-id="5513f-120">1</span></span>

<span data-ttu-id="5513f-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="5513f-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="5513f-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-123">64</span><span class="sxs-lookup"><span data-stu-id="5513f-123">64</span></span>

<span data-ttu-id="5513f-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="5513f-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="5513f-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-126">65</span><span class="sxs-lookup"><span data-stu-id="5513f-126">65</span></span>

<span data-ttu-id="5513f-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="5513f-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-129">66</span><span class="sxs-lookup"><span data-stu-id="5513f-129">66</span></span>

<span data-ttu-id="5513f-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="5513f-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-132">67</span><span class="sxs-lookup"><span data-stu-id="5513f-132">67</span></span>

<span data-ttu-id="5513f-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="5513f-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-135">68</span><span class="sxs-lookup"><span data-stu-id="5513f-135">68</span></span>

<span data-ttu-id="5513f-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="5513f-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-138">69</span><span class="sxs-lookup"><span data-stu-id="5513f-138">69</span></span>

<span data-ttu-id="5513f-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="5513f-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-141">70</span><span class="sxs-lookup"><span data-stu-id="5513f-141">70</span></span>

<span data-ttu-id="5513f-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-144">71</span><span class="sxs-lookup"><span data-stu-id="5513f-144">71</span></span>

<span data-ttu-id="5513f-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="5513f-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-147">72</span><span class="sxs-lookup"><span data-stu-id="5513f-147">72</span></span>

<span data-ttu-id="5513f-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="5513f-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-150">73</span><span class="sxs-lookup"><span data-stu-id="5513f-150">73</span></span>

<span data-ttu-id="5513f-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-153">74</span><span class="sxs-lookup"><span data-stu-id="5513f-153">74</span></span>

<span data-ttu-id="5513f-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="5513f-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-156">75</span><span class="sxs-lookup"><span data-stu-id="5513f-156">75</span></span>

<span data-ttu-id="5513f-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="5513f-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-159">76</span><span class="sxs-lookup"><span data-stu-id="5513f-159">76</span></span>

<span data-ttu-id="5513f-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-162">77</span><span class="sxs-lookup"><span data-stu-id="5513f-162">77</span></span>

<span data-ttu-id="5513f-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="5513f-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-165">78</span><span class="sxs-lookup"><span data-stu-id="5513f-165">78</span></span>

<span data-ttu-id="5513f-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="5513f-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-168">79</span><span class="sxs-lookup"><span data-stu-id="5513f-168">79</span></span>

<span data-ttu-id="5513f-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="5513f-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-171">80</span><span class="sxs-lookup"><span data-stu-id="5513f-171">80</span></span>

<span data-ttu-id="5513f-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="5513f-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="5513f-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-174">81</span><span class="sxs-lookup"><span data-stu-id="5513f-174">81</span></span>

<span data-ttu-id="5513f-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="5513f-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="5513f-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-177">82</span><span class="sxs-lookup"><span data-stu-id="5513f-177">82</span></span>

<span data-ttu-id="5513f-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="5513f-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="5513f-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-180">83</span><span class="sxs-lookup"><span data-stu-id="5513f-180">83</span></span>

<span data-ttu-id="5513f-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="5513f-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="5513f-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-183">84</span><span class="sxs-lookup"><span data-stu-id="5513f-183">84</span></span>

<span data-ttu-id="5513f-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="5513f-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="5513f-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-186">85 %</span><span class="sxs-lookup"><span data-stu-id="5513f-186">85</span></span>

<span data-ttu-id="5513f-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="5513f-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="5513f-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-189">86</span><span class="sxs-lookup"><span data-stu-id="5513f-189">86</span></span>

<span data-ttu-id="5513f-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="5513f-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-192">87</span><span class="sxs-lookup"><span data-stu-id="5513f-192">87</span></span>

<span data-ttu-id="5513f-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="5513f-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-195">88</span><span class="sxs-lookup"><span data-stu-id="5513f-195">88</span></span>

<span data-ttu-id="5513f-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="5513f-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="5513f-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-198">89</span><span class="sxs-lookup"><span data-stu-id="5513f-198">89</span></span>

<span data-ttu-id="5513f-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="5513f-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="5513f-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-201">90</span><span class="sxs-lookup"><span data-stu-id="5513f-201">90</span></span>

<span data-ttu-id="5513f-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="5513f-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="5513f-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-204">91</span><span class="sxs-lookup"><span data-stu-id="5513f-204">91</span></span>

<span data-ttu-id="5513f-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="5513f-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="5513f-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-207">92</span><span class="sxs-lookup"><span data-stu-id="5513f-207">92</span></span>

<span data-ttu-id="5513f-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="5513f-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="5513f-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-210">93</span><span class="sxs-lookup"><span data-stu-id="5513f-210">93</span></span>

<span data-ttu-id="5513f-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5513f-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="5513f-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-213">94</span><span class="sxs-lookup"><span data-stu-id="5513f-213">94</span></span>

<span data-ttu-id="5513f-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="5513f-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="5513f-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-216">95</span><span class="sxs-lookup"><span data-stu-id="5513f-216">95</span></span>

<span data-ttu-id="5513f-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="5513f-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="5513f-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-219">96</span><span class="sxs-lookup"><span data-stu-id="5513f-219">96</span></span>

<span data-ttu-id="5513f-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="5513f-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="5513f-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-222">97</span><span class="sxs-lookup"><span data-stu-id="5513f-222">97</span></span>

<span data-ttu-id="5513f-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="5513f-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="5513f-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-225">98</span><span class="sxs-lookup"><span data-stu-id="5513f-225">98</span></span>

<span data-ttu-id="5513f-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="5513f-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="5513f-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-228">100</span><span class="sxs-lookup"><span data-stu-id="5513f-228">100</span></span>

<span data-ttu-id="5513f-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="5513f-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5513f-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="5513f-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5513f-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="5513f-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5513f-232">Notes</span><span class="sxs-lookup"><span data-stu-id="5513f-232">Remarks</span></span>

<span data-ttu-id="5513f-233">Lorsque l’espace de la mémoire tampon est rempli, le routeur commence à ignorer les paquets aléatoirement dans sa file d’attente.</span><span class="sxs-lookup"><span data-stu-id="5513f-233">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span>

<span data-ttu-id="5513f-234">Les tampons de données de file d’attente de paquets ont une longueur de 256 octets, donc la valeur du paramètre *ForwardBufferMemory* doit être un multiple de 256.</span><span class="sxs-lookup"><span data-stu-id="5513f-234">Packet queue data buffers are 256 bytes in length, so the value of the *ForwardBufferMemory* parameter should be a multiple of 256.</span></span> <span data-ttu-id="5513f-235">Plusieurs mémoires tampons sont chaînées pour les paquets plus volumineux.</span><span class="sxs-lookup"><span data-stu-id="5513f-235">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="5513f-236">L’en-tête IP d’un paquet est stocké séparément.</span><span class="sxs-lookup"><span data-stu-id="5513f-236">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="5513f-237">Ce paramètre est ignoré et aucune mémoire tampon n’est allouée si le routeur IP n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="5513f-237">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="5513f-238">La taille de la mémoire tampon peut être comprise entre l’unité de transmission maximale (MTU) du réseau et une valeur inférieure à 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="5513f-238">The buffer size can range from the network Maximum Transmission Unit (MTU) to a value smaller than 0xFFFFFFFF.</span></span>

## <a name="examples"></a><span data-ttu-id="5513f-239">Exemples</span><span class="sxs-lookup"><span data-stu-id="5513f-239">Examples</span></span>

<span data-ttu-id="5513f-240">L’exemple VBScript [de modification de la mémoire tampon de transfert pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) configure la mémoire tampon de transfert pour toutes les cartes réseau d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5513f-240">The [Modify the Forward Buffer Memory for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) VBScript sample configures the forward buffer memory for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5513f-241">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5513f-241">Requirements</span></span>



| <span data-ttu-id="5513f-242">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5513f-242">Requirement</span></span> | <span data-ttu-id="5513f-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="5513f-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5513f-244">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5513f-244">Minimum supported client</span></span><br/> | <span data-ttu-id="5513f-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5513f-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5513f-246">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5513f-246">Minimum supported server</span></span><br/> | <span data-ttu-id="5513f-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5513f-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5513f-248">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5513f-248">Namespace</span></span><br/>                | <span data-ttu-id="5513f-249">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5513f-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5513f-250">MOF</span><span class="sxs-lookup"><span data-stu-id="5513f-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5513f-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5513f-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5513f-252">DLL</span><span class="sxs-lookup"><span data-stu-id="5513f-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5513f-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5513f-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5513f-254">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5513f-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5513f-255">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="5513f-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5513f-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="5513f-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="5513f-257">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="5513f-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="5513f-258">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="5513f-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="5513f-259">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="5513f-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

