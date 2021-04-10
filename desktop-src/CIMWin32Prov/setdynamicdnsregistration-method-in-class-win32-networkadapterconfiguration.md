---
description: La méthode SetDynamicDNSRegistration indique l’inscription DNS dynamique des adresses IP pour cette carte liée à IP.
ms.assetid: 8e6ca408-3283-40b8-b621-9befdc39b730
ms.tgt_platform: multiple
title: Méthode SetDynamicDNSRegistration de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDynamicDNSRegistration
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36818205e356f873b391159293e9204a9ced44a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861381"
---
# <a name="setdynamicdnsregistration-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="fa0b1-103">Méthode SetDynamicDNSRegistration de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="fa0b1-103">SetDynamicDNSRegistration method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="fa0b1-104">La méthode **SetDynamicDNSRegistration** indique l’inscription DNS dynamique des adresses IP pour cette carte liée à IP.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-104">The **SetDynamicDNSRegistration** method indicates the dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span>

<span data-ttu-id="fa0b1-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="fa0b1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fa0b1-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fa0b1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa0b1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa0b1-107">Syntax</span></span>


```mof
uint32 SetDynamicDNSRegistration(
  [in]           boolean FullDNSRegistrationEnabled,
  [in, optional] boolean DomainDNSRegistrationEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="fa0b1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa0b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa0b1-109">*FullDNSRegistrationEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa0b1-109">*FullDNSRegistrationEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-110">Si la **valeur est true**, les adresses IP de cette connexion sont inscrites dans DNS sous le nom DNS complet de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-110">If **true**, the IP addresses for this connection is registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="fa0b1-111">Le nom DNS complet de l’ordinateur s’affiche sous l’onglet **identification réseau** du panneau de configuration du système.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-111">The full DNS name of the computer is displayed on the **Network Identification** tab of the system Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-112">*DomainDNSRegistrationEnabled* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fa0b1-112">*DomainDNSRegistrationEnabled* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-113">Si la **valeur est true**, les adresses IP de cette connexion sont enregistrées sous le nom de domaine de cette connexion, en plus d’être inscrites sous le nom DNS complet de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-113">If **true**, the IP addresses for this connection are registered under the domain name of this connection, in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="fa0b1-114">Le nom de domaine de cette connexion est défini à l’aide de la méthode [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) ou attribuée par DHCP.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-114">The domain name of this connection is either set using the method [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) or assigned by DHCP.</span></span> <span data-ttu-id="fa0b1-115">Le nom inscrit est le nom d’hôte de l’ordinateur avec le nom de domaine ajouté.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-115">The registered name is the host name of the computer with the domain name appended.</span></span> <span data-ttu-id="fa0b1-116">Ce paramètre a une signification uniquement lorsque *FullDNSRegistrationEnabled* est activé.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-116">This parameter has meaning only when *FullDNSRegistrationEnabled* is enabled.</span></span> <span data-ttu-id="fa0b1-117">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-117">The default value is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa0b1-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa0b1-118">Return value</span></span>

<span data-ttu-id="fa0b1-119">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="fa0b1-120">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fa0b1-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fa0b1-121">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fa0b1-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fa0b1-122">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-123">0</span><span class="sxs-lookup"><span data-stu-id="fa0b1-123">0</span></span>

<span data-ttu-id="fa0b1-124">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-125">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-126">1</span><span class="sxs-lookup"><span data-stu-id="fa0b1-126">1</span></span>

<span data-ttu-id="fa0b1-127">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-128">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-129">64</span><span class="sxs-lookup"><span data-stu-id="fa0b1-129">64</span></span>

<span data-ttu-id="fa0b1-130">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-131">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-132">65</span><span class="sxs-lookup"><span data-stu-id="fa0b1-132">65</span></span>

<span data-ttu-id="fa0b1-133">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-134">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-135">66</span><span class="sxs-lookup"><span data-stu-id="fa0b1-135">66</span></span>

<span data-ttu-id="fa0b1-136">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-137">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-138">67</span><span class="sxs-lookup"><span data-stu-id="fa0b1-138">67</span></span>

<span data-ttu-id="fa0b1-139">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-140">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-141">68</span><span class="sxs-lookup"><span data-stu-id="fa0b1-141">68</span></span>

<span data-ttu-id="fa0b1-142">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-143">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-144">69</span><span class="sxs-lookup"><span data-stu-id="fa0b1-144">69</span></span>

<span data-ttu-id="fa0b1-145">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-146">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-147">70</span><span class="sxs-lookup"><span data-stu-id="fa0b1-147">70</span></span>

<span data-ttu-id="fa0b1-148">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-149">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-150">71</span><span class="sxs-lookup"><span data-stu-id="fa0b1-150">71</span></span>

<span data-ttu-id="fa0b1-151">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-152">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-153">72</span><span class="sxs-lookup"><span data-stu-id="fa0b1-153">72</span></span>

<span data-ttu-id="fa0b1-154">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-155">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-156">73</span><span class="sxs-lookup"><span data-stu-id="fa0b1-156">73</span></span>

<span data-ttu-id="fa0b1-157">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-158">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-159">74</span><span class="sxs-lookup"><span data-stu-id="fa0b1-159">74</span></span>

<span data-ttu-id="fa0b1-160">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-161">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-162">75</span><span class="sxs-lookup"><span data-stu-id="fa0b1-162">75</span></span>

<span data-ttu-id="fa0b1-163">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-164">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-165">76</span><span class="sxs-lookup"><span data-stu-id="fa0b1-165">76</span></span>

<span data-ttu-id="fa0b1-166">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-167">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-168">77</span><span class="sxs-lookup"><span data-stu-id="fa0b1-168">77</span></span>

<span data-ttu-id="fa0b1-169">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-170">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-171">78</span><span class="sxs-lookup"><span data-stu-id="fa0b1-171">78</span></span>

<span data-ttu-id="fa0b1-172">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-173">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-174">79</span><span class="sxs-lookup"><span data-stu-id="fa0b1-174">79</span></span>

<span data-ttu-id="fa0b1-175">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-176">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-177">80</span><span class="sxs-lookup"><span data-stu-id="fa0b1-177">80</span></span>

<span data-ttu-id="fa0b1-178">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-179">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-180">81</span><span class="sxs-lookup"><span data-stu-id="fa0b1-180">81</span></span>

<span data-ttu-id="fa0b1-181">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-182">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-183">82</span><span class="sxs-lookup"><span data-stu-id="fa0b1-183">82</span></span>

<span data-ttu-id="fa0b1-184">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-185">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-186">83</span><span class="sxs-lookup"><span data-stu-id="fa0b1-186">83</span></span>

<span data-ttu-id="fa0b1-187">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-188">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-189">84</span><span class="sxs-lookup"><span data-stu-id="fa0b1-189">84</span></span>

<span data-ttu-id="fa0b1-190">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-191">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-192">85 %</span><span class="sxs-lookup"><span data-stu-id="fa0b1-192">85</span></span>

<span data-ttu-id="fa0b1-193">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-194">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-195">86</span><span class="sxs-lookup"><span data-stu-id="fa0b1-195">86</span></span>

<span data-ttu-id="fa0b1-196">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-197">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-198">87</span><span class="sxs-lookup"><span data-stu-id="fa0b1-198">87</span></span>

<span data-ttu-id="fa0b1-199">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-200">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-201">88</span><span class="sxs-lookup"><span data-stu-id="fa0b1-201">88</span></span>

<span data-ttu-id="fa0b1-202">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-203">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-204">89</span><span class="sxs-lookup"><span data-stu-id="fa0b1-204">89</span></span>

<span data-ttu-id="fa0b1-205">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-206">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-207">90</span><span class="sxs-lookup"><span data-stu-id="fa0b1-207">90</span></span>

<span data-ttu-id="fa0b1-208">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-209">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-210">91</span><span class="sxs-lookup"><span data-stu-id="fa0b1-210">91</span></span>

<span data-ttu-id="fa0b1-211">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-212">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-213">92</span><span class="sxs-lookup"><span data-stu-id="fa0b1-213">92</span></span>

<span data-ttu-id="fa0b1-214">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-215">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-216">93</span><span class="sxs-lookup"><span data-stu-id="fa0b1-216">93</span></span>

<span data-ttu-id="fa0b1-217">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-218">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-219">94</span><span class="sxs-lookup"><span data-stu-id="fa0b1-219">94</span></span>

<span data-ttu-id="fa0b1-220">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-221">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-222">95</span><span class="sxs-lookup"><span data-stu-id="fa0b1-222">95</span></span>

<span data-ttu-id="fa0b1-223">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-224">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-225">96</span><span class="sxs-lookup"><span data-stu-id="fa0b1-225">96</span></span>

<span data-ttu-id="fa0b1-226">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-227">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-228">97</span><span class="sxs-lookup"><span data-stu-id="fa0b1-228">97</span></span>

<span data-ttu-id="fa0b1-229">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-230">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-231">98</span><span class="sxs-lookup"><span data-stu-id="fa0b1-231">98</span></span>

<span data-ttu-id="fa0b1-232">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-233">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-234">100</span><span class="sxs-lookup"><span data-stu-id="fa0b1-234">100</span></span>

<span data-ttu-id="fa0b1-235">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b1-236">**Autres**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="fa0b1-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="fa0b1-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fa0b1-238">Exemples</span><span class="sxs-lookup"><span data-stu-id="fa0b1-238">Examples</span></span>

<span data-ttu-id="fa0b1-239">L’exemple de [modification de l’inscription DNS dynamique pour une carte réseau](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) configure l’inscription DNS dynamique pour une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-239">The [Modify Dynamic DNS Registration for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript sample configures dynamic DNS registration for a network adapter.</span></span>

<span data-ttu-id="fa0b1-240">L’exemple de configuration de [cartes réseau iSCSI par Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) automatise les paramètres de configuration d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fa0b1-240">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa0b1-241">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa0b1-241">Requirements</span></span>



| <span data-ttu-id="fa0b1-242">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa0b1-242">Requirement</span></span> | <span data-ttu-id="fa0b1-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa0b1-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0b1-244">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa0b1-244">Minimum supported client</span></span><br/> | <span data-ttu-id="fa0b1-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa0b1-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa0b1-246">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa0b1-246">Minimum supported server</span></span><br/> | <span data-ttu-id="fa0b1-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa0b1-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa0b1-248">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fa0b1-248">Namespace</span></span><br/>                | <span data-ttu-id="fa0b1-249">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fa0b1-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa0b1-250">MOF</span><span class="sxs-lookup"><span data-stu-id="fa0b1-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa0b1-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b1-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa0b1-252">DLL</span><span class="sxs-lookup"><span data-stu-id="fa0b1-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa0b1-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b1-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa0b1-254">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa0b1-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa0b1-255">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="fa0b1-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="fa0b1-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="fa0b1-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="fa0b1-257">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="fa0b1-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="fa0b1-258">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="fa0b1-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="fa0b1-259">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="fa0b1-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

