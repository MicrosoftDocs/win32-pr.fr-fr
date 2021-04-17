---
description: La méthode statique de la classe WMI SetIGMPLevel permet de définir la portée à laquelle le système prend en charge la multidiffusion IP et participe au protocole de gestion de groupes Internet.
ms.assetid: 38877576-aa23-4841-b3ae-1a02bfdd70d8
ms.tgt_platform: multiple
title: Méthode SetIGMPLevel de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIGMPLevel
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 97ead4df1d45b110c3d0a91976dc8eca6ffd72c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523788"
---
# <a name="setigmplevel-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1fa2b-103">Méthode SetIGMPLevel de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fa2b-103">SetIGMPLevel method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1fa2b-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetIGMPLevel** permet de définir la portée à laquelle le système prend en charge la multidiffusion IP et participe au protocole de gestion de groupes Internet.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-104">The **SetIGMPLevel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span>

<span data-ttu-id="1fa2b-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1fa2b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1fa2b-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1fa2b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa2b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fa2b-107">Syntax</span></span>


```mof
uint32 SetIGMPLevel(
  [in] uint8 IGMPLevel
);
```



## <a name="parameters"></a><span data-ttu-id="1fa2b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fa2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fa2b-109">*IGMPLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fa2b-109">*IGMPLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-110">Type de données : **entier**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-110">Data type: **Integer**</span></span>

<span data-ttu-id="1fa2b-111">Définit le niveau auquel le système prend en charge la multidiffusion IP et participe au protocole de gestion de groupes Internet.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-111">Sets the level at which the system supports IP multicast and participates in the Internet Group Management Protocol.</span></span> <span data-ttu-id="1fa2b-112">Au niveau 0, le système ne prend pas en charge la multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-112">At level 0, the system provides no multicast support.</span></span> <span data-ttu-id="1fa2b-113">Au niveau 1, le système peut uniquement envoyer des paquets de multidiffusion IP.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-113">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="1fa2b-114">Au niveau 2, le système peut envoyer des paquets de multidiffusion IP et participer pleinement à IGMP pour recevoir des paquets de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-114">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="1fa2b-115">**Aucune multidiffusion** (0)</span><span class="sxs-lookup"><span data-stu-id="1fa2b-115">**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="1fa2b-116">**Multidiffusion IP** (1)</span><span class="sxs-lookup"><span data-stu-id="1fa2b-116">**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="1fa2b-117">**IP & multidiffusion IGMP** (2)</span><span class="sxs-lookup"><span data-stu-id="1fa2b-117">**IP & IGMP multicast** (2)</span></span>


<span data-ttu-id="1fa2b-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1fa2b-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="1fa2b-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fa2b-119">Return value</span></span>

<span data-ttu-id="1fa2b-120">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-120">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="1fa2b-121">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1fa2b-121">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1fa2b-122">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1fa2b-122">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1fa2b-123">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-123">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-124">0</span><span class="sxs-lookup"><span data-stu-id="1fa2b-124">0</span></span>

<span data-ttu-id="1fa2b-125">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-125">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-126">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-126">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-127">1</span><span class="sxs-lookup"><span data-stu-id="1fa2b-127">1</span></span>

<span data-ttu-id="1fa2b-128">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-128">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-129">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-130">64</span><span class="sxs-lookup"><span data-stu-id="1fa2b-130">64</span></span>

<span data-ttu-id="1fa2b-131">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-132">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-133">65</span><span class="sxs-lookup"><span data-stu-id="1fa2b-133">65</span></span>

<span data-ttu-id="1fa2b-134">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-135">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-136">66</span><span class="sxs-lookup"><span data-stu-id="1fa2b-136">66</span></span>

<span data-ttu-id="1fa2b-137">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-138">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-139">67</span><span class="sxs-lookup"><span data-stu-id="1fa2b-139">67</span></span>

<span data-ttu-id="1fa2b-140">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-141">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-142">68</span><span class="sxs-lookup"><span data-stu-id="1fa2b-142">68</span></span>

<span data-ttu-id="1fa2b-143">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-144">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-145">69</span><span class="sxs-lookup"><span data-stu-id="1fa2b-145">69</span></span>

<span data-ttu-id="1fa2b-146">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-147">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-148">70</span><span class="sxs-lookup"><span data-stu-id="1fa2b-148">70</span></span>

<span data-ttu-id="1fa2b-149">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-150">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-151">71</span><span class="sxs-lookup"><span data-stu-id="1fa2b-151">71</span></span>

<span data-ttu-id="1fa2b-152">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-153">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-154">72</span><span class="sxs-lookup"><span data-stu-id="1fa2b-154">72</span></span>

<span data-ttu-id="1fa2b-155">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-156">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-157">73</span><span class="sxs-lookup"><span data-stu-id="1fa2b-157">73</span></span>

<span data-ttu-id="1fa2b-158">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-159">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-160">74</span><span class="sxs-lookup"><span data-stu-id="1fa2b-160">74</span></span>

<span data-ttu-id="1fa2b-161">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-162">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-163">75</span><span class="sxs-lookup"><span data-stu-id="1fa2b-163">75</span></span>

<span data-ttu-id="1fa2b-164">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-165">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-166">76</span><span class="sxs-lookup"><span data-stu-id="1fa2b-166">76</span></span>

<span data-ttu-id="1fa2b-167">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-168">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-169">77</span><span class="sxs-lookup"><span data-stu-id="1fa2b-169">77</span></span>

<span data-ttu-id="1fa2b-170">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-171">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-172">78</span><span class="sxs-lookup"><span data-stu-id="1fa2b-172">78</span></span>

<span data-ttu-id="1fa2b-173">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-174">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-175">79</span><span class="sxs-lookup"><span data-stu-id="1fa2b-175">79</span></span>

<span data-ttu-id="1fa2b-176">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-177">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-178">80</span><span class="sxs-lookup"><span data-stu-id="1fa2b-178">80</span></span>

<span data-ttu-id="1fa2b-179">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-180">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-181">81</span><span class="sxs-lookup"><span data-stu-id="1fa2b-181">81</span></span>

<span data-ttu-id="1fa2b-182">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-183">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-184">82</span><span class="sxs-lookup"><span data-stu-id="1fa2b-184">82</span></span>

<span data-ttu-id="1fa2b-185">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-186">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-187">83</span><span class="sxs-lookup"><span data-stu-id="1fa2b-187">83</span></span>

<span data-ttu-id="1fa2b-188">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-189">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-190">84</span><span class="sxs-lookup"><span data-stu-id="1fa2b-190">84</span></span>

<span data-ttu-id="1fa2b-191">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-192">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-193">85 %</span><span class="sxs-lookup"><span data-stu-id="1fa2b-193">85</span></span>

<span data-ttu-id="1fa2b-194">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-195">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-196">86</span><span class="sxs-lookup"><span data-stu-id="1fa2b-196">86</span></span>

<span data-ttu-id="1fa2b-197">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-198">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-199">87</span><span class="sxs-lookup"><span data-stu-id="1fa2b-199">87</span></span>

<span data-ttu-id="1fa2b-200">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-201">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-202">88</span><span class="sxs-lookup"><span data-stu-id="1fa2b-202">88</span></span>

<span data-ttu-id="1fa2b-203">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-204">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-205">89</span><span class="sxs-lookup"><span data-stu-id="1fa2b-205">89</span></span>

<span data-ttu-id="1fa2b-206">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-207">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-208">90</span><span class="sxs-lookup"><span data-stu-id="1fa2b-208">90</span></span>

<span data-ttu-id="1fa2b-209">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-210">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-211">91</span><span class="sxs-lookup"><span data-stu-id="1fa2b-211">91</span></span>

<span data-ttu-id="1fa2b-212">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-213">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-214">92</span><span class="sxs-lookup"><span data-stu-id="1fa2b-214">92</span></span>

<span data-ttu-id="1fa2b-215">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-216">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-217">93</span><span class="sxs-lookup"><span data-stu-id="1fa2b-217">93</span></span>

<span data-ttu-id="1fa2b-218">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-219">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-220">94</span><span class="sxs-lookup"><span data-stu-id="1fa2b-220">94</span></span>

<span data-ttu-id="1fa2b-221">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-222">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-223">95</span><span class="sxs-lookup"><span data-stu-id="1fa2b-223">95</span></span>

<span data-ttu-id="1fa2b-224">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-225">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-226">96</span><span class="sxs-lookup"><span data-stu-id="1fa2b-226">96</span></span>

<span data-ttu-id="1fa2b-227">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-228">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-229">97</span><span class="sxs-lookup"><span data-stu-id="1fa2b-229">97</span></span>

<span data-ttu-id="1fa2b-230">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-231">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-232">98</span><span class="sxs-lookup"><span data-stu-id="1fa2b-232">98</span></span>

<span data-ttu-id="1fa2b-233">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-233">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-234">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-235">100</span><span class="sxs-lookup"><span data-stu-id="1fa2b-235">100</span></span>

<span data-ttu-id="1fa2b-236">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1fa2b-237">**Autres**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1fa2b-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="1fa2b-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1fa2b-239">Exemples</span><span class="sxs-lookup"><span data-stu-id="1fa2b-239">Examples</span></span>

<span data-ttu-id="1fa2b-240">L’exemple VBScript [de modification du niveau IGMP pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) désactive la multidiffusion IGMP sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1fa2b-240">The [Modify the IGMP Level for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript sample disables IGMP multicasting on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa2b-241">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fa2b-241">Requirements</span></span>



| <span data-ttu-id="1fa2b-242">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fa2b-242">Requirement</span></span> | <span data-ttu-id="1fa2b-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa2b-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa2b-244">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fa2b-244">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa2b-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fa2b-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1fa2b-246">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fa2b-246">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa2b-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fa2b-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1fa2b-248">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1fa2b-248">Namespace</span></span><br/>                | <span data-ttu-id="1fa2b-249">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1fa2b-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1fa2b-250">MOF</span><span class="sxs-lookup"><span data-stu-id="1fa2b-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fa2b-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fa2b-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fa2b-252">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa2b-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fa2b-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa2b-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa2b-254">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fa2b-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa2b-255">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="1fa2b-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1fa2b-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1fa2b-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="1fa2b-257">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="1fa2b-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="1fa2b-258">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="1fa2b-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="1fa2b-259">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="1fa2b-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

