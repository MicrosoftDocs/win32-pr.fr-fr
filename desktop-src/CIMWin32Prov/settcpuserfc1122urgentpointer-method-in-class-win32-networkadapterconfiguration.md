---
description: La méthode statique de la classe WMI SetTcpUseRFC1122UrgentPointer permet de spécifier si TCP utilise la spécification RFC 1122 pour les données urgentes, ou le mode utilisé par les systèmes dérivés de Berkeley Software Design (BSD).
ms.assetid: f8d07690-2723-4bc3-b15f-a24d575456a7
ms.tgt_platform: multiple
title: Méthode SetTcpUseRFC1122UrgentPointer de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpUseRFC1122UrgentPointer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 928a809211288eb7f024c735ce033b819e5d49f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110739"
---
# <a name="settcpuserfc1122urgentpointer-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="b7e05-103">Méthode SetTcpUseRFC1122UrgentPointer de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e05-103">SetTcpUseRFC1122UrgentPointer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="b7e05-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpUseRFC1122UrgentPointer** permet de spécifier si TCP utilise la spécification RFC 1122 pour les données urgentes, ou le mode utilisé par les systèmes dérivés de Berkeley Software Design (BSD).</span><span class="sxs-lookup"><span data-stu-id="b7e05-104">The **SetTcpUseRFC1122UrgentPointer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span>

<span data-ttu-id="b7e05-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b7e05-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b7e05-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b7e05-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e05-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7e05-107">Syntax</span></span>


```mof
uint32 SetTcpUseRFC1122UrgentPointer(
  [in] boolean TcpUseRFC1122UrgentPointer
);
```



## <a name="parameters"></a><span data-ttu-id="b7e05-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7e05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e05-109">*TcpUseRFC1122UrgentPointer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7e05-109">*TcpUseRFC1122UrgentPointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-110">Si la **valeur est true**, TCP utilise la spécification RFC 1122.</span><span class="sxs-lookup"><span data-stu-id="b7e05-110">If **true**, TCP uses the RFC 1122 specification.</span></span> <span data-ttu-id="b7e05-111">Si la **valeur est false**, les données urgentes sont envoyées dans le mode utilisé par les systèmes dérivés de BSD.</span><span class="sxs-lookup"><span data-stu-id="b7e05-111">If **false**, urgent data is sent in the mode used by BSD-derived systems.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e05-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7e05-112">Return value</span></span>

<span data-ttu-id="b7e05-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b7e05-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="b7e05-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b7e05-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b7e05-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b7e05-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b7e05-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="b7e05-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-117">0</span><span class="sxs-lookup"><span data-stu-id="b7e05-117">0</span></span>

<span data-ttu-id="b7e05-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b7e05-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="b7e05-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-120">1</span><span class="sxs-lookup"><span data-stu-id="b7e05-120">1</span></span>

<span data-ttu-id="b7e05-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="b7e05-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="b7e05-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-123">64</span><span class="sxs-lookup"><span data-stu-id="b7e05-123">64</span></span>

<span data-ttu-id="b7e05-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="b7e05-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="b7e05-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-126">65</span><span class="sxs-lookup"><span data-stu-id="b7e05-126">65</span></span>

<span data-ttu-id="b7e05-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="b7e05-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-129">66</span><span class="sxs-lookup"><span data-stu-id="b7e05-129">66</span></span>

<span data-ttu-id="b7e05-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="b7e05-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-132">67</span><span class="sxs-lookup"><span data-stu-id="b7e05-132">67</span></span>

<span data-ttu-id="b7e05-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="b7e05-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-135">68</span><span class="sxs-lookup"><span data-stu-id="b7e05-135">68</span></span>

<span data-ttu-id="b7e05-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="b7e05-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-138">69</span><span class="sxs-lookup"><span data-stu-id="b7e05-138">69</span></span>

<span data-ttu-id="b7e05-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b7e05-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-141">70</span><span class="sxs-lookup"><span data-stu-id="b7e05-141">70</span></span>

<span data-ttu-id="b7e05-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-144">71</span><span class="sxs-lookup"><span data-stu-id="b7e05-144">71</span></span>

<span data-ttu-id="b7e05-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="b7e05-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-147">72</span><span class="sxs-lookup"><span data-stu-id="b7e05-147">72</span></span>

<span data-ttu-id="b7e05-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="b7e05-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-150">73</span><span class="sxs-lookup"><span data-stu-id="b7e05-150">73</span></span>

<span data-ttu-id="b7e05-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-153">74</span><span class="sxs-lookup"><span data-stu-id="b7e05-153">74</span></span>

<span data-ttu-id="b7e05-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="b7e05-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-156">75</span><span class="sxs-lookup"><span data-stu-id="b7e05-156">75</span></span>

<span data-ttu-id="b7e05-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="b7e05-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-159">76</span><span class="sxs-lookup"><span data-stu-id="b7e05-159">76</span></span>

<span data-ttu-id="b7e05-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-162">77</span><span class="sxs-lookup"><span data-stu-id="b7e05-162">77</span></span>

<span data-ttu-id="b7e05-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="b7e05-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-165">78</span><span class="sxs-lookup"><span data-stu-id="b7e05-165">78</span></span>

<span data-ttu-id="b7e05-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="b7e05-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-168">79</span><span class="sxs-lookup"><span data-stu-id="b7e05-168">79</span></span>

<span data-ttu-id="b7e05-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="b7e05-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-171">80</span><span class="sxs-lookup"><span data-stu-id="b7e05-171">80</span></span>

<span data-ttu-id="b7e05-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b7e05-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="b7e05-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-174">81</span><span class="sxs-lookup"><span data-stu-id="b7e05-174">81</span></span>

<span data-ttu-id="b7e05-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="b7e05-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="b7e05-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-177">82</span><span class="sxs-lookup"><span data-stu-id="b7e05-177">82</span></span>

<span data-ttu-id="b7e05-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="b7e05-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="b7e05-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-180">83</span><span class="sxs-lookup"><span data-stu-id="b7e05-180">83</span></span>

<span data-ttu-id="b7e05-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="b7e05-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="b7e05-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-183">84</span><span class="sxs-lookup"><span data-stu-id="b7e05-183">84</span></span>

<span data-ttu-id="b7e05-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="b7e05-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="b7e05-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-186">85 %</span><span class="sxs-lookup"><span data-stu-id="b7e05-186">85</span></span>

<span data-ttu-id="b7e05-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="b7e05-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="b7e05-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-189">86</span><span class="sxs-lookup"><span data-stu-id="b7e05-189">86</span></span>

<span data-ttu-id="b7e05-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="b7e05-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-192">87</span><span class="sxs-lookup"><span data-stu-id="b7e05-192">87</span></span>

<span data-ttu-id="b7e05-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="b7e05-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-195">88</span><span class="sxs-lookup"><span data-stu-id="b7e05-195">88</span></span>

<span data-ttu-id="b7e05-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="b7e05-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="b7e05-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-198">89</span><span class="sxs-lookup"><span data-stu-id="b7e05-198">89</span></span>

<span data-ttu-id="b7e05-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="b7e05-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="b7e05-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-201">90</span><span class="sxs-lookup"><span data-stu-id="b7e05-201">90</span></span>

<span data-ttu-id="b7e05-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="b7e05-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="b7e05-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-204">91</span><span class="sxs-lookup"><span data-stu-id="b7e05-204">91</span></span>

<span data-ttu-id="b7e05-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="b7e05-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="b7e05-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-207">92</span><span class="sxs-lookup"><span data-stu-id="b7e05-207">92</span></span>

<span data-ttu-id="b7e05-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="b7e05-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="b7e05-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-210">93</span><span class="sxs-lookup"><span data-stu-id="b7e05-210">93</span></span>

<span data-ttu-id="b7e05-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="b7e05-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="b7e05-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-213">94</span><span class="sxs-lookup"><span data-stu-id="b7e05-213">94</span></span>

<span data-ttu-id="b7e05-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="b7e05-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="b7e05-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-216">95</span><span class="sxs-lookup"><span data-stu-id="b7e05-216">95</span></span>

<span data-ttu-id="b7e05-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="b7e05-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="b7e05-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-219">96</span><span class="sxs-lookup"><span data-stu-id="b7e05-219">96</span></span>

<span data-ttu-id="b7e05-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="b7e05-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="b7e05-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-222">97</span><span class="sxs-lookup"><span data-stu-id="b7e05-222">97</span></span>

<span data-ttu-id="b7e05-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="b7e05-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="b7e05-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-225">98</span><span class="sxs-lookup"><span data-stu-id="b7e05-225">98</span></span>

<span data-ttu-id="b7e05-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="b7e05-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="b7e05-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-228">100</span><span class="sxs-lookup"><span data-stu-id="b7e05-228">100</span></span>

<span data-ttu-id="b7e05-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="b7e05-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b7e05-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="b7e05-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="b7e05-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7e05-232">Notes</span><span class="sxs-lookup"><span data-stu-id="b7e05-232">Remarks</span></span>

<span data-ttu-id="b7e05-233">Les RFC 1122 et BSD interprètent le pointeur urgent dans l’en-tête TCP et la longueur des données urgentes différemment.</span><span class="sxs-lookup"><span data-stu-id="b7e05-233">RFC 1122 and BSD interpret the urgent pointer in the TCP header and the length of the urgent data differently.</span></span> <span data-ttu-id="b7e05-234">Ils ne sont pas interopérables.</span><span class="sxs-lookup"><span data-stu-id="b7e05-234">They are not interoperable.</span></span> <span data-ttu-id="b7e05-235">La valeur par défaut est le mode BSD.</span><span class="sxs-lookup"><span data-stu-id="b7e05-235">The default is BSD mode.</span></span>

## <a name="examples"></a><span data-ttu-id="b7e05-236">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7e05-236">Examples</span></span>

<span data-ttu-id="b7e05-237">L’exemple VBScript [modifier l’utilisation du pointeur urgent pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) configure un ordinateur pour utiliser la spécification RFC 1122 pour les données urgentes.</span><span class="sxs-lookup"><span data-stu-id="b7e05-237">The [Modify Urgent Pointer Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) VBScript sample configures a computer to use the RFC 1122 specification for urgent data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e05-238">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7e05-238">Requirements</span></span>



| <span data-ttu-id="b7e05-239">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7e05-239">Requirement</span></span> | <span data-ttu-id="b7e05-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7e05-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e05-241">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7e05-241">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e05-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7e05-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7e05-243">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7e05-243">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e05-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7e05-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7e05-245">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b7e05-245">Namespace</span></span><br/>                | <span data-ttu-id="b7e05-246">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b7e05-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7e05-247">MOF</span><span class="sxs-lookup"><span data-stu-id="b7e05-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7e05-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7e05-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7e05-249">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e05-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e05-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e05-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7e05-251">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7e05-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e05-252">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="b7e05-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b7e05-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="b7e05-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="b7e05-254">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="b7e05-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="b7e05-255">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="b7e05-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="b7e05-256">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="b7e05-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

