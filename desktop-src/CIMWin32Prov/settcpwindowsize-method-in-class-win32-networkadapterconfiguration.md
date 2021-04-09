---
description: La méthode statique de la classe WMI SetTcpWindowSize permet de définir la taille maximale de la fenêtre de réception TCP offerte par le système.
ms.assetid: c108fd9c-6de4-4f3e-9691-b0b5c1a3dc5f
ms.tgt_platform: multiple
title: Méthode SetTcpWindowSize de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpWindowSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4a77acdc81c06d1f78da8bbc0160bd0d21bcfd8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110738"
---
# <a name="settcpwindowsize-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="5e7da-103">Méthode SetTcpWindowSize de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e7da-103">SetTcpWindowSize method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="5e7da-104">La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpWindowSize** permet de définir la taille maximale de la fenêtre de réception TCP offerte par le système.</span><span class="sxs-lookup"><span data-stu-id="5e7da-104">The **SetTcpWindowSize** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum TCP Receive Window size offered by the system.</span></span>

<span data-ttu-id="5e7da-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5e7da-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5e7da-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5e7da-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e7da-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e7da-107">Syntax</span></span>


```mof
uint32 SetTcpWindowSize(
  [in] uint16 TcpWindowSize
);
```



## <a name="parameters"></a><span data-ttu-id="5e7da-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e7da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e7da-109">*TcpWindowSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e7da-109">*TcpWindowSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-110">Taille maximale de la fenêtre de réception TCP offerte par le système.</span><span class="sxs-lookup"><span data-stu-id="5e7da-110">Maximum TCP receive window size offered by the system.</span></span> <span data-ttu-id="5e7da-111">La plage valide de valeurs en octets est 0-65535.</span><span class="sxs-lookup"><span data-stu-id="5e7da-111">The valid range of values in bytes is 0 - 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e7da-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e7da-112">Return value</span></span>

<span data-ttu-id="5e7da-113">Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5e7da-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="5e7da-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5e7da-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5e7da-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5e7da-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5e7da-116">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="5e7da-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-117">0</span><span class="sxs-lookup"><span data-stu-id="5e7da-117">0</span></span>

<span data-ttu-id="5e7da-118">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5e7da-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-119">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="5e7da-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-120">1</span><span class="sxs-lookup"><span data-stu-id="5e7da-120">1</span></span>

<span data-ttu-id="5e7da-121">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="5e7da-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-122">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="5e7da-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-123">64</span><span class="sxs-lookup"><span data-stu-id="5e7da-123">64</span></span>

<span data-ttu-id="5e7da-124">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="5e7da-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-125">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="5e7da-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-126">65</span><span class="sxs-lookup"><span data-stu-id="5e7da-126">65</span></span>

<span data-ttu-id="5e7da-127">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="5e7da-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-128">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-129">66</span><span class="sxs-lookup"><span data-stu-id="5e7da-129">66</span></span>

<span data-ttu-id="5e7da-130">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-131">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="5e7da-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-132">67</span><span class="sxs-lookup"><span data-stu-id="5e7da-132">67</span></span>

<span data-ttu-id="5e7da-133">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="5e7da-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-134">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-135">68</span><span class="sxs-lookup"><span data-stu-id="5e7da-135">68</span></span>

<span data-ttu-id="5e7da-136">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-137">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="5e7da-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-138">69</span><span class="sxs-lookup"><span data-stu-id="5e7da-138">69</span></span>

<span data-ttu-id="5e7da-139">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="5e7da-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-140">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-141">70</span><span class="sxs-lookup"><span data-stu-id="5e7da-141">70</span></span>

<span data-ttu-id="5e7da-142">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-143">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-144">71</span><span class="sxs-lookup"><span data-stu-id="5e7da-144">71</span></span>

<span data-ttu-id="5e7da-145">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-146">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="5e7da-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-147">72</span><span class="sxs-lookup"><span data-stu-id="5e7da-147">72</span></span>

<span data-ttu-id="5e7da-148">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="5e7da-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-149">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-150">73</span><span class="sxs-lookup"><span data-stu-id="5e7da-150">73</span></span>

<span data-ttu-id="5e7da-151">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-152">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-153">74</span><span class="sxs-lookup"><span data-stu-id="5e7da-153">74</span></span>

<span data-ttu-id="5e7da-154">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-155">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="5e7da-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-156">75</span><span class="sxs-lookup"><span data-stu-id="5e7da-156">75</span></span>

<span data-ttu-id="5e7da-157">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="5e7da-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-158">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-159">76</span><span class="sxs-lookup"><span data-stu-id="5e7da-159">76</span></span>

<span data-ttu-id="5e7da-160">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-161">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-162">77</span><span class="sxs-lookup"><span data-stu-id="5e7da-162">77</span></span>

<span data-ttu-id="5e7da-163">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-164">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="5e7da-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-165">78</span><span class="sxs-lookup"><span data-stu-id="5e7da-165">78</span></span>

<span data-ttu-id="5e7da-166">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="5e7da-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-167">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-168">79</span><span class="sxs-lookup"><span data-stu-id="5e7da-168">79</span></span>

<span data-ttu-id="5e7da-169">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-170">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="5e7da-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-171">80</span><span class="sxs-lookup"><span data-stu-id="5e7da-171">80</span></span>

<span data-ttu-id="5e7da-172">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="5e7da-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-173">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="5e7da-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-174">81</span><span class="sxs-lookup"><span data-stu-id="5e7da-174">81</span></span>

<span data-ttu-id="5e7da-175">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="5e7da-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-176">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="5e7da-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-177">82</span><span class="sxs-lookup"><span data-stu-id="5e7da-177">82</span></span>

<span data-ttu-id="5e7da-178">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="5e7da-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-179">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="5e7da-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-180">83</span><span class="sxs-lookup"><span data-stu-id="5e7da-180">83</span></span>

<span data-ttu-id="5e7da-181">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="5e7da-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-182">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="5e7da-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-183">84</span><span class="sxs-lookup"><span data-stu-id="5e7da-183">84</span></span>

<span data-ttu-id="5e7da-184">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="5e7da-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-185">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="5e7da-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-186">85 %</span><span class="sxs-lookup"><span data-stu-id="5e7da-186">85</span></span>

<span data-ttu-id="5e7da-187">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="5e7da-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-188">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="5e7da-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-189">86</span><span class="sxs-lookup"><span data-stu-id="5e7da-189">86</span></span>

<span data-ttu-id="5e7da-190">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="5e7da-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-191">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-192">87</span><span class="sxs-lookup"><span data-stu-id="5e7da-192">87</span></span>

<span data-ttu-id="5e7da-193">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-194">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="5e7da-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-195">88</span><span class="sxs-lookup"><span data-stu-id="5e7da-195">88</span></span>

<span data-ttu-id="5e7da-196">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="5e7da-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-197">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="5e7da-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-198">89</span><span class="sxs-lookup"><span data-stu-id="5e7da-198">89</span></span>

<span data-ttu-id="5e7da-199">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="5e7da-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-200">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="5e7da-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-201">90</span><span class="sxs-lookup"><span data-stu-id="5e7da-201">90</span></span>

<span data-ttu-id="5e7da-202">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="5e7da-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-203">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="5e7da-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-204">91</span><span class="sxs-lookup"><span data-stu-id="5e7da-204">91</span></span>

<span data-ttu-id="5e7da-205">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="5e7da-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-206">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="5e7da-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-207">92</span><span class="sxs-lookup"><span data-stu-id="5e7da-207">92</span></span>

<span data-ttu-id="5e7da-208">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="5e7da-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-209">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="5e7da-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-210">93</span><span class="sxs-lookup"><span data-stu-id="5e7da-210">93</span></span>

<span data-ttu-id="5e7da-211">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5e7da-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-212">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="5e7da-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-213">94</span><span class="sxs-lookup"><span data-stu-id="5e7da-213">94</span></span>

<span data-ttu-id="5e7da-214">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="5e7da-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-215">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="5e7da-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-216">95</span><span class="sxs-lookup"><span data-stu-id="5e7da-216">95</span></span>

<span data-ttu-id="5e7da-217">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="5e7da-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-218">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="5e7da-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-219">96</span><span class="sxs-lookup"><span data-stu-id="5e7da-219">96</span></span>

<span data-ttu-id="5e7da-220">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="5e7da-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-221">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="5e7da-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-222">97</span><span class="sxs-lookup"><span data-stu-id="5e7da-222">97</span></span>

<span data-ttu-id="5e7da-223">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="5e7da-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-224">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="5e7da-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-225">98</span><span class="sxs-lookup"><span data-stu-id="5e7da-225">98</span></span>

<span data-ttu-id="5e7da-226">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="5e7da-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-227">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="5e7da-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-228">100</span><span class="sxs-lookup"><span data-stu-id="5e7da-228">100</span></span>

<span data-ttu-id="5e7da-229">DHCP n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="5e7da-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5e7da-230">**Autres**</span><span class="sxs-lookup"><span data-stu-id="5e7da-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5e7da-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="5e7da-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e7da-232">Notes</span><span class="sxs-lookup"><span data-stu-id="5e7da-232">Remarks</span></span>

<span data-ttu-id="5e7da-233">La fenêtre de réception spécifie le nombre d'octets qu'un expéditeur peut transmettre sans recevoir d'accusé de réception.</span><span class="sxs-lookup"><span data-stu-id="5e7da-233">The receive window specifies the number of bytes a sender can transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="5e7da-234">En général, les fenêtres de réception plus volumineuses améliorent les performances sur les réseaux à haut débit et à bande passante élevée.</span><span class="sxs-lookup"><span data-stu-id="5e7da-234">In general, larger receive windows improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="5e7da-235">Pour des performances optimales, la fenêtre de réception doit être un multiple pair de la taille maximale du segment TCP (MSS).</span><span class="sxs-lookup"><span data-stu-id="5e7da-235">For efficiency, the receive window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span>

> [!Note]  
> <span data-ttu-id="5e7da-236">Windows Vista : cette méthode accède à l' `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` entrée de Registre, qui n’est pas utilisée dans l’implémentation actuelle du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5e7da-236">Windows Vista: This method accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5e7da-237">Exemples</span><span class="sxs-lookup"><span data-stu-id="5e7da-237">Examples</span></span>

<span data-ttu-id="5e7da-238">L’exemple VBScript [de modification de la taille de fenêtre TCP pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) définit la taille de fenêtre TCP pour toutes les cartes réseau d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5e7da-238">The [Modify the TCP Window Size for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript sample sets the TCP window size for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e7da-239">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e7da-239">Requirements</span></span>



| <span data-ttu-id="5e7da-240">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e7da-240">Requirement</span></span> | <span data-ttu-id="5e7da-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e7da-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e7da-242">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e7da-242">Minimum supported client</span></span><br/> | <span data-ttu-id="5e7da-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e7da-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e7da-244">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e7da-244">Minimum supported server</span></span><br/> | <span data-ttu-id="5e7da-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e7da-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e7da-246">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5e7da-246">End of client support</span></span><br/>    | <span data-ttu-id="5e7da-247">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5e7da-247">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="5e7da-248">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="5e7da-248">End of server support</span></span><br/>    | <span data-ttu-id="5e7da-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e7da-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e7da-250">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5e7da-250">Namespace</span></span><br/>                | <span data-ttu-id="5e7da-251">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5e7da-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e7da-252">MOF</span><span class="sxs-lookup"><span data-stu-id="5e7da-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e7da-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e7da-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e7da-254">DLL</span><span class="sxs-lookup"><span data-stu-id="5e7da-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e7da-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e7da-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e7da-256">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e7da-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e7da-257">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="5e7da-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5e7da-258">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="5e7da-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="5e7da-259">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="5e7da-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="5e7da-260">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="5e7da-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="5e7da-261">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="5e7da-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

