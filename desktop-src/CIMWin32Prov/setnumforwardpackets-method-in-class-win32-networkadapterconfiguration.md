---
description: La méthode statique de la classe WMI SetNumForwardPackets permet de définir le nombre d’en-têtes de paquets IP alloués pour la file d’attente de paquets du routeur. Lorsque tous les en-têtes sont en cours d’utilisation, le routeur commence à rejeter les paquets de la file d’attente au hasard.
ms.assetid: cadc7565-4cad-4e0f-a1eb-bf99d333bb28
ms.tgt_platform: multiple
title: Méthode SetNumForwardPackets de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetNumForwardPackets
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f46ecd62766b5df642dff1e52614171a513a8fca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748565"
---
# <a name="setnumforwardpackets-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2481f-104">Méthode SetNumForwardPackets de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="2481f-104">SetNumForwardPackets method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2481f-105">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetNumForwardPackets** permet de définir le nombre d’en-têtes de paquets IP alloués pour la file d’attente de paquets du routeur.</span><span class="sxs-lookup"><span data-stu-id="2481f-105">The **SetNumForwardPackets** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="2481f-106">Lorsque tous les en-têtes sont en cours d’utilisation, le routeur commence à rejeter les paquets de la file d’attente au hasard.</span><span class="sxs-lookup"><span data-stu-id="2481f-106">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span>

<span data-ttu-id="2481f-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2481f-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2481f-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2481f-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2481f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2481f-109">Syntax</span></span>


```mof
uint32 SetNumForwardPackets(
  [in] uint32 NumForwardPackets
);
```



## <a name="parameters"></a><span data-ttu-id="2481f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2481f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2481f-111">*NumForwardPackets* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2481f-111">*NumForwardPackets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2481f-112">Nombre d’en-têtes de paquet IP alloués pour la file d’attente de paquets du routeur.</span><span class="sxs-lookup"><span data-stu-id="2481f-112">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="2481f-113">Elle doit être au moins aussi grande que la valeur de la propriété [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) divisée par la taille maximale des données IP des réseaux connectés au routeur.</span><span class="sxs-lookup"><span data-stu-id="2481f-113">This should be at least as large as the value of the [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) property divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="2481f-114">Elle ne doit pas être supérieure à la valeur **ForwardBufferMemory** divisée par 256, car au moins 256 octets de mémoire tampon de transfert sont requis par chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="2481f-114">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are required by each packet.</span></span> <span data-ttu-id="2481f-115">Le nombre optimal de paquets de transfert pour une taille **ForwardBufferMemory** donnée dépend du type de trafic effectué sur le réseau et se situe entre ces deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="2481f-115">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic carried on the network, and will be somewhere between these two values.</span></span> <span data-ttu-id="2481f-116">Si le routeur est désactivé, ce paramètre est ignoré et aucun en-tête n’est alloué.</span><span class="sxs-lookup"><span data-stu-id="2481f-116">If the router is disabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="2481f-117">Plage valide : 1-0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="2481f-117">Valid range: 1 - 0xFFFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2481f-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2481f-118">Return value</span></span>

<span data-ttu-id="2481f-119">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2481f-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="2481f-120">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2481f-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2481f-121">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2481f-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2481f-122">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="2481f-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-123">0</span><span class="sxs-lookup"><span data-stu-id="2481f-123">0</span></span>

<span data-ttu-id="2481f-124">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2481f-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-125">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="2481f-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-126">1</span><span class="sxs-lookup"><span data-stu-id="2481f-126">1</span></span>

<span data-ttu-id="2481f-127">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="2481f-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-128">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="2481f-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-129">64</span><span class="sxs-lookup"><span data-stu-id="2481f-129">64</span></span>

<span data-ttu-id="2481f-130">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="2481f-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-131">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="2481f-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-132">65</span><span class="sxs-lookup"><span data-stu-id="2481f-132">65</span></span>

<span data-ttu-id="2481f-133">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="2481f-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-134">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-135">66</span><span class="sxs-lookup"><span data-stu-id="2481f-135">66</span></span>

<span data-ttu-id="2481f-136">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-137">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="2481f-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-138">67</span><span class="sxs-lookup"><span data-stu-id="2481f-138">67</span></span>

<span data-ttu-id="2481f-139">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="2481f-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-140">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-141">68</span><span class="sxs-lookup"><span data-stu-id="2481f-141">68</span></span>

<span data-ttu-id="2481f-142">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-143">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="2481f-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-144">69</span><span class="sxs-lookup"><span data-stu-id="2481f-144">69</span></span>

<span data-ttu-id="2481f-145">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2481f-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-146">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-147">70</span><span class="sxs-lookup"><span data-stu-id="2481f-147">70</span></span>

<span data-ttu-id="2481f-148">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-149">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-150">71</span><span class="sxs-lookup"><span data-stu-id="2481f-150">71</span></span>

<span data-ttu-id="2481f-151">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-152">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="2481f-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-153">72</span><span class="sxs-lookup"><span data-stu-id="2481f-153">72</span></span>

<span data-ttu-id="2481f-154">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="2481f-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-155">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-156">73</span><span class="sxs-lookup"><span data-stu-id="2481f-156">73</span></span>

<span data-ttu-id="2481f-157">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-158">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-159">74</span><span class="sxs-lookup"><span data-stu-id="2481f-159">74</span></span>

<span data-ttu-id="2481f-160">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-161">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="2481f-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-162">75</span><span class="sxs-lookup"><span data-stu-id="2481f-162">75</span></span>

<span data-ttu-id="2481f-163">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="2481f-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-164">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-165">76</span><span class="sxs-lookup"><span data-stu-id="2481f-165">76</span></span>

<span data-ttu-id="2481f-166">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-167">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-168">77</span><span class="sxs-lookup"><span data-stu-id="2481f-168">77</span></span>

<span data-ttu-id="2481f-169">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-170">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="2481f-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-171">78</span><span class="sxs-lookup"><span data-stu-id="2481f-171">78</span></span>

<span data-ttu-id="2481f-172">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="2481f-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-173">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-174">79</span><span class="sxs-lookup"><span data-stu-id="2481f-174">79</span></span>

<span data-ttu-id="2481f-175">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-176">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="2481f-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-177">80</span><span class="sxs-lookup"><span data-stu-id="2481f-177">80</span></span>

<span data-ttu-id="2481f-178">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2481f-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-179">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="2481f-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-180">81</span><span class="sxs-lookup"><span data-stu-id="2481f-180">81</span></span>

<span data-ttu-id="2481f-181">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="2481f-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-182">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="2481f-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-183">82</span><span class="sxs-lookup"><span data-stu-id="2481f-183">82</span></span>

<span data-ttu-id="2481f-184">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="2481f-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-185">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="2481f-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-186">83</span><span class="sxs-lookup"><span data-stu-id="2481f-186">83</span></span>

<span data-ttu-id="2481f-187">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="2481f-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-188">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="2481f-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-189">84</span><span class="sxs-lookup"><span data-stu-id="2481f-189">84</span></span>

<span data-ttu-id="2481f-190">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="2481f-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-191">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="2481f-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-192">85 %</span><span class="sxs-lookup"><span data-stu-id="2481f-192">85</span></span>

<span data-ttu-id="2481f-193">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="2481f-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-194">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="2481f-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-195">86</span><span class="sxs-lookup"><span data-stu-id="2481f-195">86</span></span>

<span data-ttu-id="2481f-196">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="2481f-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-197">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-198">87</span><span class="sxs-lookup"><span data-stu-id="2481f-198">87</span></span>

<span data-ttu-id="2481f-199">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-200">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="2481f-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-201">88</span><span class="sxs-lookup"><span data-stu-id="2481f-201">88</span></span>

<span data-ttu-id="2481f-202">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="2481f-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-203">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="2481f-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-204">89</span><span class="sxs-lookup"><span data-stu-id="2481f-204">89</span></span>

<span data-ttu-id="2481f-205">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="2481f-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-206">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="2481f-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-207">90</span><span class="sxs-lookup"><span data-stu-id="2481f-207">90</span></span>

<span data-ttu-id="2481f-208">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="2481f-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-209">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="2481f-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-210">91</span><span class="sxs-lookup"><span data-stu-id="2481f-210">91</span></span>

<span data-ttu-id="2481f-211">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="2481f-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-212">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="2481f-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-213">92</span><span class="sxs-lookup"><span data-stu-id="2481f-213">92</span></span>

<span data-ttu-id="2481f-214">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="2481f-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-215">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="2481f-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-216">93</span><span class="sxs-lookup"><span data-stu-id="2481f-216">93</span></span>

<span data-ttu-id="2481f-217">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2481f-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-218">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="2481f-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-219">94</span><span class="sxs-lookup"><span data-stu-id="2481f-219">94</span></span>

<span data-ttu-id="2481f-220">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="2481f-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-221">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="2481f-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-222">95</span><span class="sxs-lookup"><span data-stu-id="2481f-222">95</span></span>

<span data-ttu-id="2481f-223">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="2481f-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-224">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="2481f-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-225">96</span><span class="sxs-lookup"><span data-stu-id="2481f-225">96</span></span>

<span data-ttu-id="2481f-226">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="2481f-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-227">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="2481f-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-228">97</span><span class="sxs-lookup"><span data-stu-id="2481f-228">97</span></span>

<span data-ttu-id="2481f-229">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="2481f-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-230">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="2481f-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-231">98</span><span class="sxs-lookup"><span data-stu-id="2481f-231">98</span></span>

<span data-ttu-id="2481f-232">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="2481f-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-233">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="2481f-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-234">100</span><span class="sxs-lookup"><span data-stu-id="2481f-234">100</span></span>

<span data-ttu-id="2481f-235">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="2481f-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2481f-236">**Autres**</span><span class="sxs-lookup"><span data-stu-id="2481f-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2481f-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2481f-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2481f-238">Exemples</span><span class="sxs-lookup"><span data-stu-id="2481f-238">Examples</span></span>

<span data-ttu-id="2481f-239">L’exemple VBScript [de modification du nombre de paquets transférés autorisés](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) configure le nombre de paquets de transfert alloués à la file d’attente de paquets du routeur.</span><span class="sxs-lookup"><span data-stu-id="2481f-239">The [Modify the Number of Allowed Forward Packets](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) VBScript sample configures the number of forward packets allocated to the router packet queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="2481f-240">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2481f-240">Requirements</span></span>



| <span data-ttu-id="2481f-241">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2481f-241">Requirement</span></span> | <span data-ttu-id="2481f-242">Valeur</span><span class="sxs-lookup"><span data-stu-id="2481f-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2481f-243">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2481f-243">Minimum supported client</span></span><br/> | <span data-ttu-id="2481f-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2481f-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2481f-245">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2481f-245">Minimum supported server</span></span><br/> | <span data-ttu-id="2481f-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2481f-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2481f-247">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2481f-247">Namespace</span></span><br/>                | <span data-ttu-id="2481f-248">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2481f-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2481f-249">MOF</span><span class="sxs-lookup"><span data-stu-id="2481f-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2481f-250"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2481f-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2481f-251">DLL</span><span class="sxs-lookup"><span data-stu-id="2481f-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2481f-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2481f-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2481f-253">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2481f-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2481f-254">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="2481f-254">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2481f-255">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="2481f-255">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2481f-256">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="2481f-256">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2481f-257">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="2481f-257">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2481f-258">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="2481f-258">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

