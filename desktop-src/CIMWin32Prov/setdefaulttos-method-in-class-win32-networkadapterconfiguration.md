---
description: Cette méthode est obsolète. Les applications doivent utiliser l’API de qualité de service (QoS) pour manipuler les bits de type de service (TOS).
ms.assetid: 18860c13-7324-4a37-b83c-f3d15c425acb
ms.tgt_platform: multiple
title: Méthode SetDefaultTOS de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTOS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5df55ff88c87047a48a84a122c8e58c8148a7cff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512902"
---
# <a name="setdefaulttos-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="40834-104">Méthode SetDefaultTOS de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="40834-104">SetDefaultTOS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="40834-105">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="40834-105">This method is obsolete.</span></span> <span data-ttu-id="40834-106">Les applications doivent utiliser l’API de qualité de service (QoS) pour manipuler les bits de type de service (TOS).</span><span class="sxs-lookup"><span data-stu-id="40834-106">Applications should use the Quality of Service (QoS) API to manipulate Type of Service (TOS) bits.</span></span> <span data-ttu-id="40834-107">Pour plus d’informations, consultez [qualité de service](/previous-versions/windows/desktop/qos/qos-start-page).</span><span class="sxs-lookup"><span data-stu-id="40834-107">For more information, see [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page).</span></span>

<span data-ttu-id="40834-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="40834-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="40834-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="40834-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="40834-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40834-110">Syntax</span></span>


```mof
uint32 SetDefaultTOS(
  [in] uint8 DefaultTOS
);
```



## <a name="parameters"></a><span data-ttu-id="40834-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40834-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40834-112">*DefaultTOS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40834-112">*DefaultTOS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40834-113">Valeur du type de service (TOS) placée dans l’en-tête des paquets IP sortants.</span><span class="sxs-lookup"><span data-stu-id="40834-113">Type of Service (TOS) value put in the header of outgoing IP packets.</span></span> <span data-ttu-id="40834-114">Pour obtenir une définition des valeurs, consultez RFC 791.</span><span class="sxs-lookup"><span data-stu-id="40834-114">For a definition of the values, see RFC 791.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40834-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40834-115">Return value</span></span>

<span data-ttu-id="40834-116">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="40834-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="40834-117">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="40834-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="40834-118">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="40834-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="40834-119">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="40834-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="40834-120">0</span><span class="sxs-lookup"><span data-stu-id="40834-120">0</span></span>

<span data-ttu-id="40834-121">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="40834-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="40834-122">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="40834-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="40834-123">1</span><span class="sxs-lookup"><span data-stu-id="40834-123">1</span></span>

<span data-ttu-id="40834-124">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="40834-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="40834-125">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="40834-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="40834-126">64</span><span class="sxs-lookup"><span data-stu-id="40834-126">64</span></span>

<span data-ttu-id="40834-127">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="40834-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="40834-128">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="40834-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="40834-129">65</span><span class="sxs-lookup"><span data-stu-id="40834-129">65</span></span>

<span data-ttu-id="40834-130">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="40834-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="40834-131">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="40834-132">66</span><span class="sxs-lookup"><span data-stu-id="40834-132">66</span></span>

<span data-ttu-id="40834-133">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="40834-134">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="40834-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="40834-135">67</span><span class="sxs-lookup"><span data-stu-id="40834-135">67</span></span>

<span data-ttu-id="40834-136">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="40834-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="40834-137">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="40834-138">68</span><span class="sxs-lookup"><span data-stu-id="40834-138">68</span></span>

<span data-ttu-id="40834-139">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="40834-140">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="40834-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="40834-141">69</span><span class="sxs-lookup"><span data-stu-id="40834-141">69</span></span>

<span data-ttu-id="40834-142">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="40834-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="40834-143">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="40834-144">70</span><span class="sxs-lookup"><span data-stu-id="40834-144">70</span></span>

<span data-ttu-id="40834-145">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="40834-146">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="40834-147">71</span><span class="sxs-lookup"><span data-stu-id="40834-147">71</span></span>

<span data-ttu-id="40834-148">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="40834-149">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="40834-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="40834-150">72</span><span class="sxs-lookup"><span data-stu-id="40834-150">72</span></span>

<span data-ttu-id="40834-151">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="40834-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="40834-152">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="40834-153">73</span><span class="sxs-lookup"><span data-stu-id="40834-153">73</span></span>

<span data-ttu-id="40834-154">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="40834-155">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="40834-156">74</span><span class="sxs-lookup"><span data-stu-id="40834-156">74</span></span>

<span data-ttu-id="40834-157">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="40834-158">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="40834-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="40834-159">75</span><span class="sxs-lookup"><span data-stu-id="40834-159">75</span></span>

<span data-ttu-id="40834-160">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="40834-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="40834-161">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="40834-162">76</span><span class="sxs-lookup"><span data-stu-id="40834-162">76</span></span>

<span data-ttu-id="40834-163">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="40834-164">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="40834-165">77</span><span class="sxs-lookup"><span data-stu-id="40834-165">77</span></span>

<span data-ttu-id="40834-166">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="40834-167">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="40834-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="40834-168">78</span><span class="sxs-lookup"><span data-stu-id="40834-168">78</span></span>

<span data-ttu-id="40834-169">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="40834-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="40834-170">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="40834-171">79</span><span class="sxs-lookup"><span data-stu-id="40834-171">79</span></span>

<span data-ttu-id="40834-172">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="40834-173">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="40834-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="40834-174">80</span><span class="sxs-lookup"><span data-stu-id="40834-174">80</span></span>

<span data-ttu-id="40834-175">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="40834-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="40834-176">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="40834-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="40834-177">81</span><span class="sxs-lookup"><span data-stu-id="40834-177">81</span></span>

<span data-ttu-id="40834-178">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="40834-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="40834-179">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="40834-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="40834-180">82</span><span class="sxs-lookup"><span data-stu-id="40834-180">82</span></span>

<span data-ttu-id="40834-181">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="40834-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="40834-182">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="40834-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="40834-183">83</span><span class="sxs-lookup"><span data-stu-id="40834-183">83</span></span>

<span data-ttu-id="40834-184">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="40834-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="40834-185">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="40834-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="40834-186">84</span><span class="sxs-lookup"><span data-stu-id="40834-186">84</span></span>

<span data-ttu-id="40834-187">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="40834-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="40834-188">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="40834-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="40834-189">85 %</span><span class="sxs-lookup"><span data-stu-id="40834-189">85</span></span>

<span data-ttu-id="40834-190">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="40834-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="40834-191">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="40834-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="40834-192">86</span><span class="sxs-lookup"><span data-stu-id="40834-192">86</span></span>

<span data-ttu-id="40834-193">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="40834-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="40834-194">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="40834-195">87</span><span class="sxs-lookup"><span data-stu-id="40834-195">87</span></span>

<span data-ttu-id="40834-196">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="40834-197">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="40834-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="40834-198">88</span><span class="sxs-lookup"><span data-stu-id="40834-198">88</span></span>

<span data-ttu-id="40834-199">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="40834-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="40834-200">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="40834-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="40834-201">89</span><span class="sxs-lookup"><span data-stu-id="40834-201">89</span></span>

<span data-ttu-id="40834-202">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="40834-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="40834-203">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="40834-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="40834-204">90</span><span class="sxs-lookup"><span data-stu-id="40834-204">90</span></span>

<span data-ttu-id="40834-205">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="40834-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="40834-206">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="40834-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="40834-207">91</span><span class="sxs-lookup"><span data-stu-id="40834-207">91</span></span>

<span data-ttu-id="40834-208">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="40834-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="40834-209">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="40834-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="40834-210">92</span><span class="sxs-lookup"><span data-stu-id="40834-210">92</span></span>

<span data-ttu-id="40834-211">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="40834-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="40834-212">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="40834-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="40834-213">93</span><span class="sxs-lookup"><span data-stu-id="40834-213">93</span></span>

<span data-ttu-id="40834-214">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="40834-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="40834-215">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="40834-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="40834-216">94</span><span class="sxs-lookup"><span data-stu-id="40834-216">94</span></span>

<span data-ttu-id="40834-217">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="40834-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="40834-218">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="40834-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="40834-219">95</span><span class="sxs-lookup"><span data-stu-id="40834-219">95</span></span>

<span data-ttu-id="40834-220">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="40834-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="40834-221">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="40834-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="40834-222">96</span><span class="sxs-lookup"><span data-stu-id="40834-222">96</span></span>

<span data-ttu-id="40834-223">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="40834-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="40834-224">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="40834-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="40834-225">97</span><span class="sxs-lookup"><span data-stu-id="40834-225">97</span></span>

<span data-ttu-id="40834-226">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="40834-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="40834-227">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="40834-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="40834-228">98</span><span class="sxs-lookup"><span data-stu-id="40834-228">98</span></span>

<span data-ttu-id="40834-229">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="40834-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="40834-230">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="40834-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="40834-231">100</span><span class="sxs-lookup"><span data-stu-id="40834-231">100</span></span>

<span data-ttu-id="40834-232">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="40834-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="40834-233">**Autres**</span><span class="sxs-lookup"><span data-stu-id="40834-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="40834-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="40834-234">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40834-235">Notes</span><span class="sxs-lookup"><span data-stu-id="40834-235">Remarks</span></span>

<span data-ttu-id="40834-236">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultTOS** permet de définir la valeur OT par défaut dans l’en-tête des paquets IP sortants.</span><span class="sxs-lookup"><span data-stu-id="40834-236">The **SetDefaultTOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default TOS value in the header of outgoing IP packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="40834-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40834-237">Requirements</span></span>



| <span data-ttu-id="40834-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40834-238">Requirement</span></span> | <span data-ttu-id="40834-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="40834-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40834-240">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40834-240">Minimum supported client</span></span><br/> | <span data-ttu-id="40834-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40834-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40834-242">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40834-242">Minimum supported server</span></span><br/> | <span data-ttu-id="40834-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40834-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40834-244">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="40834-244">Namespace</span></span><br/>                | <span data-ttu-id="40834-245">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="40834-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40834-246">MOF</span><span class="sxs-lookup"><span data-stu-id="40834-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40834-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40834-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40834-248">DLL</span><span class="sxs-lookup"><span data-stu-id="40834-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40834-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40834-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40834-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40834-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40834-251">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="40834-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="40834-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="40834-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="40834-253">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="40834-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="40834-254">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="40834-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="40834-255">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="40834-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

