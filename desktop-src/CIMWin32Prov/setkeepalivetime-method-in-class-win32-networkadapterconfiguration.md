---
description: La méthode statique de la classe WMI SetKeepAliveTime permet de définir la fréquence à laquelle TCP tente de vérifier qu’une connexion inactive est toujours disponible en envoyant un paquet Keep Alive.
ms.assetid: 8640b109-928b-46fc-8dce-9ee5dcbd94e3
ms.tgt_platform: multiple
title: Méthode SetKeepAliveTime de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1dc2674f3c09626749b4c7ac6151349401670e27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544584"
---
# <a name="setkeepalivetime-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f088a-103">Méthode SetKeepAliveTime de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="f088a-103">SetKeepAliveTime method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f088a-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetKeepAliveTime** permet de définir la fréquence à laquelle TCP tente de vérifier qu’une connexion inactive est toujours disponible en envoyant un paquet Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="f088a-104">The **SetKeepAliveTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span>

<span data-ttu-id="f088a-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f088a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f088a-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f088a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f088a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f088a-107">Syntax</span></span>


```mof
uint32 SetKeepAliveTime(
  [in] uint32 KeepAliveTime
);
```



## <a name="parameters"></a><span data-ttu-id="f088a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f088a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f088a-109">*KeepAliveTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f088a-109">*KeepAliveTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f088a-110">Intervalle, en millisecondes, que le protocole TCP attend pour vérifier qu’une connexion inactive est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="f088a-110">Interval, in milliseconds, the TCP waits to check that an idle connection is still available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f088a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f088a-111">Return value</span></span>

<span data-ttu-id="f088a-112">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f088a-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f088a-113">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f088a-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f088a-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f088a-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f088a-115">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="f088a-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-116">0</span><span class="sxs-lookup"><span data-stu-id="f088a-116">0</span></span>

<span data-ttu-id="f088a-117">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f088a-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-118">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="f088a-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-119">1</span><span class="sxs-lookup"><span data-stu-id="f088a-119">1</span></span>

<span data-ttu-id="f088a-120">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="f088a-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-121">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="f088a-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-122">64</span><span class="sxs-lookup"><span data-stu-id="f088a-122">64</span></span>

<span data-ttu-id="f088a-123">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="f088a-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-124">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="f088a-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-125">65</span><span class="sxs-lookup"><span data-stu-id="f088a-125">65</span></span>

<span data-ttu-id="f088a-126">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="f088a-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-127">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-128">66</span><span class="sxs-lookup"><span data-stu-id="f088a-128">66</span></span>

<span data-ttu-id="f088a-129">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-130">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="f088a-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-131">67</span><span class="sxs-lookup"><span data-stu-id="f088a-131">67</span></span>

<span data-ttu-id="f088a-132">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="f088a-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-133">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-134">68</span><span class="sxs-lookup"><span data-stu-id="f088a-134">68</span></span>

<span data-ttu-id="f088a-135">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-136">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="f088a-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-137">69</span><span class="sxs-lookup"><span data-stu-id="f088a-137">69</span></span>

<span data-ttu-id="f088a-138">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="f088a-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-139">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-140">70</span><span class="sxs-lookup"><span data-stu-id="f088a-140">70</span></span>

<span data-ttu-id="f088a-141">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-142">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-143">71</span><span class="sxs-lookup"><span data-stu-id="f088a-143">71</span></span>

<span data-ttu-id="f088a-144">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-145">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="f088a-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-146">72</span><span class="sxs-lookup"><span data-stu-id="f088a-146">72</span></span>

<span data-ttu-id="f088a-147">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="f088a-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-148">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-149">73</span><span class="sxs-lookup"><span data-stu-id="f088a-149">73</span></span>

<span data-ttu-id="f088a-150">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-151">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-152">74</span><span class="sxs-lookup"><span data-stu-id="f088a-152">74</span></span>

<span data-ttu-id="f088a-153">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-154">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="f088a-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-155">75</span><span class="sxs-lookup"><span data-stu-id="f088a-155">75</span></span>

<span data-ttu-id="f088a-156">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="f088a-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-157">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-158">76</span><span class="sxs-lookup"><span data-stu-id="f088a-158">76</span></span>

<span data-ttu-id="f088a-159">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-160">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-161">77</span><span class="sxs-lookup"><span data-stu-id="f088a-161">77</span></span>

<span data-ttu-id="f088a-162">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-163">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="f088a-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-164">78</span><span class="sxs-lookup"><span data-stu-id="f088a-164">78</span></span>

<span data-ttu-id="f088a-165">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="f088a-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-166">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-167">79</span><span class="sxs-lookup"><span data-stu-id="f088a-167">79</span></span>

<span data-ttu-id="f088a-168">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-169">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f088a-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-170">80</span><span class="sxs-lookup"><span data-stu-id="f088a-170">80</span></span>

<span data-ttu-id="f088a-171">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f088a-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-172">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="f088a-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-173">81</span><span class="sxs-lookup"><span data-stu-id="f088a-173">81</span></span>

<span data-ttu-id="f088a-174">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="f088a-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-175">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="f088a-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-176">82</span><span class="sxs-lookup"><span data-stu-id="f088a-176">82</span></span>

<span data-ttu-id="f088a-177">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="f088a-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-178">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="f088a-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-179">83</span><span class="sxs-lookup"><span data-stu-id="f088a-179">83</span></span>

<span data-ttu-id="f088a-180">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="f088a-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-181">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="f088a-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-182">84</span><span class="sxs-lookup"><span data-stu-id="f088a-182">84</span></span>

<span data-ttu-id="f088a-183">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="f088a-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-184">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="f088a-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-185">85 %</span><span class="sxs-lookup"><span data-stu-id="f088a-185">85</span></span>

<span data-ttu-id="f088a-186">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="f088a-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-187">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="f088a-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-188">86</span><span class="sxs-lookup"><span data-stu-id="f088a-188">86</span></span>

<span data-ttu-id="f088a-189">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="f088a-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-190">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-191">87</span><span class="sxs-lookup"><span data-stu-id="f088a-191">87</span></span>

<span data-ttu-id="f088a-192">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-193">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="f088a-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-194">88</span><span class="sxs-lookup"><span data-stu-id="f088a-194">88</span></span>

<span data-ttu-id="f088a-195">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="f088a-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-196">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="f088a-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-197">89</span><span class="sxs-lookup"><span data-stu-id="f088a-197">89</span></span>

<span data-ttu-id="f088a-198">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="f088a-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-199">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="f088a-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-200">90</span><span class="sxs-lookup"><span data-stu-id="f088a-200">90</span></span>

<span data-ttu-id="f088a-201">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="f088a-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-202">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="f088a-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-203">91</span><span class="sxs-lookup"><span data-stu-id="f088a-203">91</span></span>

<span data-ttu-id="f088a-204">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="f088a-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-205">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="f088a-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-206">92</span><span class="sxs-lookup"><span data-stu-id="f088a-206">92</span></span>

<span data-ttu-id="f088a-207">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f088a-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-208">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="f088a-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-209">93</span><span class="sxs-lookup"><span data-stu-id="f088a-209">93</span></span>

<span data-ttu-id="f088a-210">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f088a-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-211">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="f088a-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-212">94</span><span class="sxs-lookup"><span data-stu-id="f088a-212">94</span></span>

<span data-ttu-id="f088a-213">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="f088a-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-214">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="f088a-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-215">95</span><span class="sxs-lookup"><span data-stu-id="f088a-215">95</span></span>

<span data-ttu-id="f088a-216">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="f088a-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-217">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="f088a-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-218">96</span><span class="sxs-lookup"><span data-stu-id="f088a-218">96</span></span>

<span data-ttu-id="f088a-219">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="f088a-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-220">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="f088a-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-221">97</span><span class="sxs-lookup"><span data-stu-id="f088a-221">97</span></span>

<span data-ttu-id="f088a-222">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="f088a-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-223">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="f088a-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-224">98</span><span class="sxs-lookup"><span data-stu-id="f088a-224">98</span></span>

<span data-ttu-id="f088a-225">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="f088a-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-226">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="f088a-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-227">100</span><span class="sxs-lookup"><span data-stu-id="f088a-227">100</span></span>

<span data-ttu-id="f088a-228">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="f088a-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f088a-229">**Autres**</span><span class="sxs-lookup"><span data-stu-id="f088a-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f088a-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f088a-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f088a-231">Notes</span><span class="sxs-lookup"><span data-stu-id="f088a-231">Remarks</span></span>

<span data-ttu-id="f088a-232">Si le système distant est toujours accessible et fonctionne, il accuse réception de la transmission Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="f088a-232">If the remote system is still reachable and functioning, it will acknowledge the Keep Alive transmission.</span></span> <span data-ttu-id="f088a-233">Les paquets Keep Alive ne sont pas envoyés par défaut.</span><span class="sxs-lookup"><span data-stu-id="f088a-233">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="f088a-234">Cette fonctionnalité peut être activée dans une connexion par une application.</span><span class="sxs-lookup"><span data-stu-id="f088a-234">This feature may be enabled in a connection by an application.</span></span>

## <a name="examples"></a><span data-ttu-id="f088a-235">Exemples</span><span class="sxs-lookup"><span data-stu-id="f088a-235">Examples</span></span>

<span data-ttu-id="f088a-236">L’exemple VBScript [modifier l’heure de maintien de l’activité pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) configure l’heure de maintien de l’activité pour toutes les cartes réseau d’un ordinateur à 300 000 millisecondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="f088a-236">The [Modify Keep Alive Time for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) VBScript sample configures the keep alive time for all network adapters on a computer to 300,000 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="f088a-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f088a-237">Requirements</span></span>



| <span data-ttu-id="f088a-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f088a-238">Requirement</span></span> | <span data-ttu-id="f088a-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="f088a-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f088a-240">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f088a-240">Minimum supported client</span></span><br/> | <span data-ttu-id="f088a-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f088a-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f088a-242">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f088a-242">Minimum supported server</span></span><br/> | <span data-ttu-id="f088a-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f088a-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f088a-244">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f088a-244">Namespace</span></span><br/>                | <span data-ttu-id="f088a-245">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f088a-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f088a-246">MOF</span><span class="sxs-lookup"><span data-stu-id="f088a-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f088a-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f088a-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f088a-248">DLL</span><span class="sxs-lookup"><span data-stu-id="f088a-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f088a-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f088a-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f088a-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f088a-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f088a-251">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="f088a-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f088a-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="f088a-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f088a-253">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="f088a-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f088a-254">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="f088a-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f088a-255">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="f088a-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

