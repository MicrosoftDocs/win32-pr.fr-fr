---
description: La méthode SetTcpipNetbios est utilisée pour définir l’opération par défaut de NetBIOS sur TCP/IP.
ms.assetid: 2c639595-da13-400d-b4d0-432b39460554
ms.tgt_platform: multiple
title: Méthode SetTcpipNetbios de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpipNetbios
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20ecab5918d00dc5f189464becc0252f2a8c0569
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861726"
---
# <a name="settcpipnetbios-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="3a48f-103">Méthode SetTcpipNetbios de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a48f-103">SetTcpipNetbios method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="3a48f-104">La méthode **SetTcpipNetbios** est utilisée pour définir l’opération par défaut de NetBIOS sur TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3a48f-104">The **SetTcpipNetbios** method is used to set the default operation of NetBIOS over TCP/IP.</span></span>

<span data-ttu-id="3a48f-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3a48f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3a48f-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3a48f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a48f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a48f-107">Syntax</span></span>


```mof
uint32 SetTcpipNetbios(
  [in] uint32 TcpipNetbiosOptions
);
```



## <a name="parameters"></a><span data-ttu-id="3a48f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a48f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a48f-109">*TcpipNetbiosOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a48f-109">*TcpipNetbiosOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-110">Valeur qui spécifie les paramètres possibles relatifs à NetBIOS sur TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3a48f-110">Value that specifies the possible settings related to NetBIOS over TCP/IP.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="3a48f-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="3a48f-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3a48f-112">Activer NetBIOS via DHCP</span><span class="sxs-lookup"><span data-stu-id="3a48f-112">Enable Netbios via DHCP</span></span>

</dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="3a48f-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="3a48f-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3a48f-114">Activer NetBIOS</span><span class="sxs-lookup"><span data-stu-id="3a48f-114">Enable Netbios</span></span>

</dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="3a48f-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="3a48f-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a48f-116">Désactiver NetBIOS</span><span class="sxs-lookup"><span data-stu-id="3a48f-116">Disable Netbios</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a48f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a48f-117">Return value</span></span>

<span data-ttu-id="3a48f-118">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3a48f-118">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="3a48f-119">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3a48f-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3a48f-120">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3a48f-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3a48f-121">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="3a48f-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-122">0</span><span class="sxs-lookup"><span data-stu-id="3a48f-122">0</span></span>

<span data-ttu-id="3a48f-123">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="3a48f-123">Successful completion.</span></span> <span data-ttu-id="3a48f-124">Aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3a48f-124">No reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-125">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="3a48f-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-126">1</span><span class="sxs-lookup"><span data-stu-id="3a48f-126">1</span></span>

<span data-ttu-id="3a48f-127">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="3a48f-127">Successful completion.</span></span> <span data-ttu-id="3a48f-128">Redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="3a48f-128">Reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-129">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="3a48f-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-130">64</span><span class="sxs-lookup"><span data-stu-id="3a48f-130">64</span></span>

<span data-ttu-id="3a48f-131">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="3a48f-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-132">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="3a48f-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-133">65</span><span class="sxs-lookup"><span data-stu-id="3a48f-133">65</span></span>

<span data-ttu-id="3a48f-134">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="3a48f-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-135">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-136">66</span><span class="sxs-lookup"><span data-stu-id="3a48f-136">66</span></span>

<span data-ttu-id="3a48f-137">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-138">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="3a48f-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-139">67</span><span class="sxs-lookup"><span data-stu-id="3a48f-139">67</span></span>

<span data-ttu-id="3a48f-140">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="3a48f-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-141">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-142">68</span><span class="sxs-lookup"><span data-stu-id="3a48f-142">68</span></span>

<span data-ttu-id="3a48f-143">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-144">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="3a48f-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-145">69</span><span class="sxs-lookup"><span data-stu-id="3a48f-145">69</span></span>

<span data-ttu-id="3a48f-146">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="3a48f-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-147">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-148">70</span><span class="sxs-lookup"><span data-stu-id="3a48f-148">70</span></span>

<span data-ttu-id="3a48f-149">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-150">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-151">71</span><span class="sxs-lookup"><span data-stu-id="3a48f-151">71</span></span>

<span data-ttu-id="3a48f-152">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-153">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="3a48f-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-154">72</span><span class="sxs-lookup"><span data-stu-id="3a48f-154">72</span></span>

<span data-ttu-id="3a48f-155">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="3a48f-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-156">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-157">73</span><span class="sxs-lookup"><span data-stu-id="3a48f-157">73</span></span>

<span data-ttu-id="3a48f-158">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-159">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-160">74</span><span class="sxs-lookup"><span data-stu-id="3a48f-160">74</span></span>

<span data-ttu-id="3a48f-161">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-162">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="3a48f-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-163">75</span><span class="sxs-lookup"><span data-stu-id="3a48f-163">75</span></span>

<span data-ttu-id="3a48f-164">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="3a48f-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-165">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-166">76</span><span class="sxs-lookup"><span data-stu-id="3a48f-166">76</span></span>

<span data-ttu-id="3a48f-167">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-168">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-169">77</span><span class="sxs-lookup"><span data-stu-id="3a48f-169">77</span></span>

<span data-ttu-id="3a48f-170">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-171">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="3a48f-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-172">78</span><span class="sxs-lookup"><span data-stu-id="3a48f-172">78</span></span>

<span data-ttu-id="3a48f-173">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="3a48f-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-174">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-175">79</span><span class="sxs-lookup"><span data-stu-id="3a48f-175">79</span></span>

<span data-ttu-id="3a48f-176">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-177">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="3a48f-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-178">80</span><span class="sxs-lookup"><span data-stu-id="3a48f-178">80</span></span>

<span data-ttu-id="3a48f-179">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3a48f-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-180">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="3a48f-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-181">81</span><span class="sxs-lookup"><span data-stu-id="3a48f-181">81</span></span>

<span data-ttu-id="3a48f-182">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="3a48f-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-183">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="3a48f-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-184">82</span><span class="sxs-lookup"><span data-stu-id="3a48f-184">82</span></span>

<span data-ttu-id="3a48f-185">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="3a48f-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-186">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="3a48f-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-187">83</span><span class="sxs-lookup"><span data-stu-id="3a48f-187">83</span></span>

<span data-ttu-id="3a48f-188">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="3a48f-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-189">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="3a48f-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-190">84</span><span class="sxs-lookup"><span data-stu-id="3a48f-190">84</span></span>

<span data-ttu-id="3a48f-191">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="3a48f-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-192">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="3a48f-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-193">85 %</span><span class="sxs-lookup"><span data-stu-id="3a48f-193">85</span></span>

<span data-ttu-id="3a48f-194">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="3a48f-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-195">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="3a48f-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-196">86</span><span class="sxs-lookup"><span data-stu-id="3a48f-196">86</span></span>

<span data-ttu-id="3a48f-197">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="3a48f-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-198">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-199">87</span><span class="sxs-lookup"><span data-stu-id="3a48f-199">87</span></span>

<span data-ttu-id="3a48f-200">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-201">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="3a48f-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-202">88</span><span class="sxs-lookup"><span data-stu-id="3a48f-202">88</span></span>

<span data-ttu-id="3a48f-203">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="3a48f-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-204">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="3a48f-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-205">89</span><span class="sxs-lookup"><span data-stu-id="3a48f-205">89</span></span>

<span data-ttu-id="3a48f-206">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="3a48f-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-207">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="3a48f-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-208">90</span><span class="sxs-lookup"><span data-stu-id="3a48f-208">90</span></span>

<span data-ttu-id="3a48f-209">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="3a48f-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-210">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="3a48f-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-211">91</span><span class="sxs-lookup"><span data-stu-id="3a48f-211">91</span></span>

<span data-ttu-id="3a48f-212">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="3a48f-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-213">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="3a48f-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-214">92</span><span class="sxs-lookup"><span data-stu-id="3a48f-214">92</span></span>

<span data-ttu-id="3a48f-215">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="3a48f-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-216">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="3a48f-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-217">93</span><span class="sxs-lookup"><span data-stu-id="3a48f-217">93</span></span>

<span data-ttu-id="3a48f-218">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3a48f-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-219">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="3a48f-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-220">94</span><span class="sxs-lookup"><span data-stu-id="3a48f-220">94</span></span>

<span data-ttu-id="3a48f-221">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="3a48f-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-222">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="3a48f-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-223">95</span><span class="sxs-lookup"><span data-stu-id="3a48f-223">95</span></span>

<span data-ttu-id="3a48f-224">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="3a48f-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-225">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="3a48f-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-226">96</span><span class="sxs-lookup"><span data-stu-id="3a48f-226">96</span></span>

<span data-ttu-id="3a48f-227">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="3a48f-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-228">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="3a48f-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-229">97</span><span class="sxs-lookup"><span data-stu-id="3a48f-229">97</span></span>

<span data-ttu-id="3a48f-230">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="3a48f-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-231">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="3a48f-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-232">98</span><span class="sxs-lookup"><span data-stu-id="3a48f-232">98</span></span>

<span data-ttu-id="3a48f-233">Tous les baux DHCP ne peuvent pas être libérés ni renouvelés.</span><span class="sxs-lookup"><span data-stu-id="3a48f-233">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-234">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="3a48f-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-235">100</span><span class="sxs-lookup"><span data-stu-id="3a48f-235">100</span></span>

<span data-ttu-id="3a48f-236">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="3a48f-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3a48f-237">**Autres**</span><span class="sxs-lookup"><span data-stu-id="3a48f-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3a48f-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="3a48f-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3a48f-239">Exemples</span><span class="sxs-lookup"><span data-stu-id="3a48f-239">Examples</span></span>

<span data-ttu-id="3a48f-240">L’exemple de [modification de l’utilisation NetBIOS sur une carte réseau](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) active NetBIOS pour une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="3a48f-240">The [Modify NetBIOS Use on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript sample enables NetBIOS for a network adapter.</span></span>

<span data-ttu-id="3a48f-241">L’exemple de configuration de [cartes réseau iSCSI par Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) automatise les paramètres de configuration d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3a48f-241">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a48f-242">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a48f-242">Requirements</span></span>



| <span data-ttu-id="3a48f-243">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a48f-243">Requirement</span></span> | <span data-ttu-id="3a48f-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a48f-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a48f-245">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a48f-245">Minimum supported client</span></span><br/> | <span data-ttu-id="3a48f-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a48f-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a48f-247">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a48f-247">Minimum supported server</span></span><br/> | <span data-ttu-id="3a48f-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a48f-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a48f-249">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3a48f-249">Namespace</span></span><br/>                | <span data-ttu-id="3a48f-250">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3a48f-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a48f-251">MOF</span><span class="sxs-lookup"><span data-stu-id="3a48f-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a48f-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a48f-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a48f-253">DLL</span><span class="sxs-lookup"><span data-stu-id="3a48f-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a48f-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a48f-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a48f-255">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a48f-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a48f-256">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="3a48f-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3a48f-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="3a48f-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="3a48f-258">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="3a48f-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="3a48f-259">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="3a48f-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="3a48f-260">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="3a48f-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

