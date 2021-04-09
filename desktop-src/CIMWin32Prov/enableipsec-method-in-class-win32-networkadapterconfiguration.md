---
description: EnableIPSec&\# 8194 ; La méthode de classe WMI active la sécurité du protocole Internet (IPsec) sur une carte réseau compatible TCP/IP.
ms.assetid: 0a45d864-606d-4adb-9b51-62d46a0d68b1
ms.tgt_platform: multiple
title: Méthode EnableIPSec de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6988d68f9939752e3c8c2c9ace063b895a2d3720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860957"
---
# <a name="enableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1e1a9-103">Méthode EnableIPSec de la \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e1a9-103">EnableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1e1a9-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableIPSec** active la sécurité du protocole Internet (IPSec) sur une carte réseau compatible TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-104">The **EnableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables Internet Protocol security (IPsec) on a TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="1e1a9-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1e1a9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1e1a9-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1e1a9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e1a9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e1a9-107">Syntax</span></span>


```mof
uint32 EnableIPSec(
  [in] string IPSecPermitTCPPorts[],
  [in] string IPSecPermitUDPPorts[],
  [in] string IPSecPermitIPProtocols[]
);
```



## <a name="parameters"></a><span data-ttu-id="1e1a9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e1a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e1a9-109">*IPSecPermitTCPPorts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e1a9-109">*IPSecPermitTCPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-110">Liste des ports auxquels accorder l’autorisation d’accès pour TCP.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-110">List of ports to be granted access permission for TCP.</span></span> <span data-ttu-id="1e1a9-111">Une valeur numérique 0 (zéro) indique que l’autorisation d’accès est accordée pour tous les ports.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-111">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="1e1a9-112">Un tableau vide indique qu’aucun port ne doit recevoir l’autorisation d’accès.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-112">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-113">*IPSecPermitUDPPorts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e1a9-113">*IPSecPermitUDPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-114">Liste des ports auxquels accorder l’autorisation d’accès pour UDP.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-114">List of ports to be granted access permission for UDP.</span></span> <span data-ttu-id="1e1a9-115">Une valeur numérique 0 (zéro) indique que l’autorisation d’accès est accordée pour tous les ports.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-115">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="1e1a9-116">Un tableau vide indique qu’aucun port ne doit recevoir l’autorisation d’accès.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-116">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-117">*IPSecPermitIPProtocols* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e1a9-117">*IPSecPermitIPProtocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-118">Liste des protocoles autorisés à s’exécuter sur l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-118">List of protocols permitted to run over the IP.</span></span> <span data-ttu-id="1e1a9-119">Une valeur numérique 0 (zéro) indique que l’autorisation d’accès est accordée pour tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-119">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="1e1a9-120">Un tableau vide indique qu’aucun protocole ne dispose de l’autorisation d’accès.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-120">An empty array indicates that no protocols are granted access permission.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e1a9-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e1a9-121">Return value</span></span>

<span data-ttu-id="1e1a9-122">Retourne la valeur 0 (zéro) pour une exécution réussie lorsqu’un redémarrage n’est pas nécessaire, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et tout autre nombre en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="1e1a9-123">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1e1a9-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1e1a9-124">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1e1a9-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1e1a9-125">**Exécution réussie, aucun redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-126">0</span><span class="sxs-lookup"><span data-stu-id="1e1a9-126">0</span></span>

<span data-ttu-id="1e1a9-127">Opération réussie, aucun redémarrage n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-128">**Achèvement réussi, redémarrage requis**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-129">1</span><span class="sxs-lookup"><span data-stu-id="1e1a9-129">1</span></span>

<span data-ttu-id="1e1a9-130">Opération terminée, redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-131">**Méthode non prise en charge sur cette plateforme**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-132">64</span><span class="sxs-lookup"><span data-stu-id="1e1a9-132">64</span></span>

<span data-ttu-id="1e1a9-133">Méthode non prise en charge sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-134">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-135">65</span><span class="sxs-lookup"><span data-stu-id="1e1a9-135">65</span></span>

<span data-ttu-id="1e1a9-136">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-137">**Masque de sous-réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-138">66</span><span class="sxs-lookup"><span data-stu-id="1e1a9-138">66</span></span>

<span data-ttu-id="1e1a9-139">Masque de sous-réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-140">**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-141">67</span><span class="sxs-lookup"><span data-stu-id="1e1a9-141">67</span></span>

<span data-ttu-id="1e1a9-142">Une erreur s’est produite lors du traitement d’une instance qui a été retournée.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-143">**Paramètre d’entrée non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-144">68</span><span class="sxs-lookup"><span data-stu-id="1e1a9-144">68</span></span>

<span data-ttu-id="1e1a9-145">Paramètre d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-146">**Plus de 5 passerelles spécifiées**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-147">69</span><span class="sxs-lookup"><span data-stu-id="1e1a9-147">69</span></span>

<span data-ttu-id="1e1a9-148">Plus de cinq passerelles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-149">**Adresse IP non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-150">70</span><span class="sxs-lookup"><span data-stu-id="1e1a9-150">70</span></span>

<span data-ttu-id="1e1a9-151">Adresse IP non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-152">**Adresse IP de passerelle non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-153">71</span><span class="sxs-lookup"><span data-stu-id="1e1a9-153">71</span></span>

<span data-ttu-id="1e1a9-154">Adresse IP de passerelle non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-155">**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-156">72</span><span class="sxs-lookup"><span data-stu-id="1e1a9-156">72</span></span>

<span data-ttu-id="1e1a9-157">Une erreur s’est produite lors de l’accès au registre pour les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-158">**Nom de domaine non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-159">73</span><span class="sxs-lookup"><span data-stu-id="1e1a9-159">73</span></span>

<span data-ttu-id="1e1a9-160">Nom de domaine non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-161">**Nom d’hôte non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-162">74</span><span class="sxs-lookup"><span data-stu-id="1e1a9-162">74</span></span>

<span data-ttu-id="1e1a9-163">Nom d’hôte non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-164">**Aucun serveur WINS principal/secondaire défini**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-165">75</span><span class="sxs-lookup"><span data-stu-id="1e1a9-165">75</span></span>

<span data-ttu-id="1e1a9-166">Aucun serveur WINS principal ou secondaire n’est défini.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-167">**Fichier non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-168">76</span><span class="sxs-lookup"><span data-stu-id="1e1a9-168">76</span></span>

<span data-ttu-id="1e1a9-169">Fichier non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-170">**Chemin système non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-171">77</span><span class="sxs-lookup"><span data-stu-id="1e1a9-171">77</span></span>

<span data-ttu-id="1e1a9-172">Chemin d’accès système non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-173">**Échec de la copie du fichier**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-174">78</span><span class="sxs-lookup"><span data-stu-id="1e1a9-174">78</span></span>

<span data-ttu-id="1e1a9-175">Échec de la copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-176">**Paramètre de sécurité non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-177">79</span><span class="sxs-lookup"><span data-stu-id="1e1a9-177">79</span></span>

<span data-ttu-id="1e1a9-178">Paramètre de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-179">**Impossible de configurer le service TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-180">80</span><span class="sxs-lookup"><span data-stu-id="1e1a9-180">80</span></span>

<span data-ttu-id="1e1a9-181">Impossible de configurer le service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-182">**Impossible de configurer le service DHCP**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-183">81</span><span class="sxs-lookup"><span data-stu-id="1e1a9-183">81</span></span>

<span data-ttu-id="1e1a9-184">Impossible de configurer le service DHCP.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-185">**Impossible de renouveler le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-186">82</span><span class="sxs-lookup"><span data-stu-id="1e1a9-186">82</span></span>

<span data-ttu-id="1e1a9-187">Impossible de renouveler le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-188">**Impossible de libérer le bail DHCP**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-189">83</span><span class="sxs-lookup"><span data-stu-id="1e1a9-189">83</span></span>

<span data-ttu-id="1e1a9-190">Impossible de libérer le bail DHCP.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-191">**IP non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-192">84</span><span class="sxs-lookup"><span data-stu-id="1e1a9-192">84</span></span>

<span data-ttu-id="1e1a9-193">IP non activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-194">**IPX non activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-195">85 %</span><span class="sxs-lookup"><span data-stu-id="1e1a9-195">85</span></span>

<span data-ttu-id="1e1a9-196">IPX n’est pas activé sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-197">**Erreur liée à un nombre de trames/réseau**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-198">86</span><span class="sxs-lookup"><span data-stu-id="1e1a9-198">86</span></span>

<span data-ttu-id="1e1a9-199">Erreur liée à l’image ou au numéro de réseau.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-200">**Type de trame non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-201">87</span><span class="sxs-lookup"><span data-stu-id="1e1a9-201">87</span></span>

<span data-ttu-id="1e1a9-202">Type de trame non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-203">**Numéro de réseau non valide**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-204">88</span><span class="sxs-lookup"><span data-stu-id="1e1a9-204">88</span></span>

<span data-ttu-id="1e1a9-205">Numéro de réseau non valide.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-206">**Numéro de réseau en double**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-207">89</span><span class="sxs-lookup"><span data-stu-id="1e1a9-207">89</span></span>

<span data-ttu-id="1e1a9-208">Numéro de réseau en double.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-209">**Paramètre hors limites**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-210">90</span><span class="sxs-lookup"><span data-stu-id="1e1a9-210">90</span></span>

<span data-ttu-id="1e1a9-211">Paramètre hors limites.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-212">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-213">91</span><span class="sxs-lookup"><span data-stu-id="1e1a9-213">91</span></span>

<span data-ttu-id="1e1a9-214">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-215">**Mémoire insuffisante**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-216">92</span><span class="sxs-lookup"><span data-stu-id="1e1a9-216">92</span></span>

<span data-ttu-id="1e1a9-217">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-218">**Existe déjà**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-219">93</span><span class="sxs-lookup"><span data-stu-id="1e1a9-219">93</span></span>

<span data-ttu-id="1e1a9-220">Existe déjà.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-221">**Chemin d’accès, fichier ou objet introuvable**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-222">94</span><span class="sxs-lookup"><span data-stu-id="1e1a9-222">94</span></span>

<span data-ttu-id="1e1a9-223">Chemin d’accès, fichier ou objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-224">**Impossible de notifier le service**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-225">95</span><span class="sxs-lookup"><span data-stu-id="1e1a9-225">95</span></span>

<span data-ttu-id="1e1a9-226">Impossible de notifier le service.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-227">**Impossible d’informer le service DNS**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-228">96</span><span class="sxs-lookup"><span data-stu-id="1e1a9-228">96</span></span>

<span data-ttu-id="1e1a9-229">Impossible d’informer le service DNS.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-230">**Interface non configurable**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-231">97</span><span class="sxs-lookup"><span data-stu-id="1e1a9-231">97</span></span>

<span data-ttu-id="1e1a9-232">Interface non configurable.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-233">**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-234">98</span><span class="sxs-lookup"><span data-stu-id="1e1a9-234">98</span></span>

<span data-ttu-id="1e1a9-235">Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-235">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-236">**DHCP n’est pas activé sur l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-237">100</span><span class="sxs-lookup"><span data-stu-id="1e1a9-237">100</span></span>

<span data-ttu-id="1e1a9-238">DHCP n’est pas activé sur la carte.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-238">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e1a9-239">**Autres**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1e1a9-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="1e1a9-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e1a9-241">Notes</span><span class="sxs-lookup"><span data-stu-id="1e1a9-241">Remarks</span></span>

<span data-ttu-id="1e1a9-242">Les ports sont sécurisés uniquement lorsque la propriété **IPFilterSecurityEnabled** dans [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-242">Ports are secured only when the **IPFilterSecurityEnabled** property in [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) is **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="1e1a9-243">Exemples</span><span class="sxs-lookup"><span data-stu-id="1e1a9-243">Examples</span></span>

<span data-ttu-id="1e1a9-244">L’exemple de script [activer IPSec sur une carte réseau](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) , sur la Galerie TechNet, utilise **EnableIPSec** pour activer la sécurité IP pour une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="1e1a9-244">The [Enable IPSec on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript sample, on TechNet Gallery, uses **EnableIPSec** to enable IP security for a network adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e1a9-245">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e1a9-245">Requirements</span></span>



| <span data-ttu-id="1e1a9-246">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e1a9-246">Requirement</span></span> | <span data-ttu-id="1e1a9-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e1a9-247">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e1a9-248">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e1a9-248">Minimum supported client</span></span><br/> | <span data-ttu-id="1e1a9-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e1a9-249">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e1a9-250">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e1a9-250">Minimum supported server</span></span><br/> | <span data-ttu-id="1e1a9-251">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e1a9-251">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e1a9-252">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e1a9-252">Namespace</span></span><br/>                | <span data-ttu-id="1e1a9-253">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1e1a9-253">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1e1a9-254">MOF</span><span class="sxs-lookup"><span data-stu-id="1e1a9-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e1a9-255"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e1a9-255"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e1a9-256">DLL</span><span class="sxs-lookup"><span data-stu-id="1e1a9-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e1a9-257"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e1a9-257"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e1a9-258">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e1a9-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e1a9-259">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="1e1a9-259">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1e1a9-260">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1e1a9-260">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="1e1a9-261">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="1e1a9-261">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="1e1a9-262">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="1e1a9-262">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="1e1a9-263">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="1e1a9-263">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

