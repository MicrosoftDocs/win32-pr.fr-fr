---
title: Configuration du Registre pour les allocations de port et la liaison sélective
description: À compter de Windows 2000, un utilitaire du kit de ressources Windows appelé Rpccfg.exe doit être utilisé pour définir des liaisons. Pour plus d’informations, consultez le kit de ressources Windows pour obtenir la version appropriée du système d’exploitation.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- Appel de procédure distante RPC, tâches, configuration du Registre pour les allocations de port et la liaison sélective
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef1749fab1beb8e637d208a7d7af64577066fe6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103941442"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a><span data-ttu-id="241b4-105">Configuration du Registre pour les allocations de port et la liaison sélective</span><span class="sxs-lookup"><span data-stu-id="241b4-105">Configuring the Registry for Port Allocations and Selective Binding</span></span>

<span data-ttu-id="241b4-106">À compter de Windows 2000, un utilitaire du kit de ressources Windows appelé Rpccfg.exe doit être utilisé pour définir des liaisons.</span><span class="sxs-lookup"><span data-stu-id="241b4-106">Starting with Windows 2000, a utility in the Windows Resource Kit called Rpccfg.exe should be used to set bindings.</span></span> <span data-ttu-id="241b4-107">Pour plus d’informations, consultez le kit de ressources Windows pour obtenir la version appropriée du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="241b4-107">For more information, consult the Windows Resource Kit for the appropriate operating system version.</span></span>

<span data-ttu-id="241b4-108">Pour les versions de Windows antérieures à Windows 2000, les clés de Registre du tableau suivant spécifient les valeurs système par défaut pour l’allocation de port dynamique et pour la liaison aux cartes réseau sur les ordinateurs multirésidents.</span><span class="sxs-lookup"><span data-stu-id="241b4-108">For versions of windows prior to Windows 2000, the registry keys in the following table specify the system defaults for dynamic port allocation and for binding to NICs on multihomed computers.</span></span> <span data-ttu-id="241b4-109">Vous devez d’abord créer ces clés, puis spécifier les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="241b4-109">You must first create these keys and then specify the appropriate settings.</span></span>

<span data-ttu-id="241b4-110">L’utilisation de la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) affecte ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="241b4-110">Using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function affects these settings.</span></span> <span data-ttu-id="241b4-111">Les développeurs doivent être familiarisés avec les paramètres de Registre expliqués dans cette section et la fonction **RpcServerUseProtseqEx** lors de la gestion des allocations de port.</span><span class="sxs-lookup"><span data-stu-id="241b4-111">Developers should be familiar with the registry settings explained in this section and the **RpcServerUseProtseqEx** function when managing port allocations.</span></span> <span data-ttu-id="241b4-112">Un exemple avec trois applications hypothétiques suit le tableau ci-dessous et montre comment ces paramètres et la fonction **RpcServerUseProtseqEx** interagissent.</span><span class="sxs-lookup"><span data-stu-id="241b4-112">An example with three hypothetical applications follows the table below, and illustrates how these settings and the **RpcServerUseProtseqEx** function interoperate.</span></span>

<span data-ttu-id="241b4-113">Si une clé est manquante ou si elle contient une valeur non valide, la configuration entière est marquée comme non valide et tous les appels **RpcServerUseProtseq \*** sur [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) ou [**ncadg \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) échouent.</span><span class="sxs-lookup"><span data-stu-id="241b4-113">If a key is missing or if it contains an invalid value, the entire configuration is marked as invalid, and all **RpcServerUseProtseq\*** calls over [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) or [**ncadg\_ip\_udp**](/windows/desktop/Midl/ncadg-ip-udp) will fail.</span></span>

> [!Note]  
> <span data-ttu-id="241b4-114">Les ports alloués à un processus restent alloués jusqu’à ce que ce processus soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="241b4-114">Ports allocated to a process remain allocated until that process dies.</span></span> <span data-ttu-id="241b4-115">Si tous les ports disponibles sont en cours d’utilisation, la fonction retourne RPC \_ S \_ \_ sur \_ ressources.</span><span class="sxs-lookup"><span data-stu-id="241b4-115">If all available ports are in use, the function returns RPC\_S\_OUT\_OF\_RESOURCES.</span></span>

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="241b4-116">Clé de port</span><span class="sxs-lookup"><span data-stu-id="241b4-116">Port key</span></span></th>
<th><span data-ttu-id="241b4-117">Type de données</span><span class="sxs-lookup"><span data-stu-id="241b4-117">Data type</span></span></th>
<th><span data-ttu-id="241b4-118">Description</span><span class="sxs-lookup"><span data-stu-id="241b4-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><span data-ttu-id="241b4-119"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="241b4-119"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="241b4-120">Spécifie un ensemble de plages de ports IP comprenant tous les ports disponibles à partir d’Internet ou tous les ports qui ne sont pas disponibles sur Internet.</span><span class="sxs-lookup"><span data-stu-id="241b4-120">Specifies a set of IP port ranges consisting of either all the ports available from the Internet or all the ports not available from the Internet.</span></span> <span data-ttu-id="241b4-121">Chaque chaîne représente un port unique ou un ensemble de ports inclusifs (par exemple, 1000-1050, 1984).</span><span class="sxs-lookup"><span data-stu-id="241b4-121">Each string represents a single port or an inclusive set of ports (for example,1000-1050, 1984).</span></span> <span data-ttu-id="241b4-122">Si des entrées sont en dehors de la plage comprise entre 0 et 65535, ou si une chaîne ne peut pas être interprétée, le temps d’exécution RPC traitera la configuration entière comme non valide.</span><span class="sxs-lookup"><span data-stu-id="241b4-122">If any entries are outside the range 0 to 65535, or if any string cannot be interpreted, the RPC run time will treat the entire configuration as invalid.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><span data-ttu-id="241b4-123"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="241b4-123"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="241b4-124">O ou N (ne respecte pas la casse).</span><span class="sxs-lookup"><span data-stu-id="241b4-124">Y or N (not case-sensitive).</span></span> <span data-ttu-id="241b4-125">Si Y, les ports répertoriés dans la clé ports sont tous les ports disponibles sur Internet sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="241b4-125">If Y, the ports listed in the Ports key are all the Internet-available ports on that computer.</span></span> <span data-ttu-id="241b4-126">Si N, les ports répertoriés dans la clé ports sont tous les ports qui ne sont pas disponibles sur Internet.</span><span class="sxs-lookup"><span data-stu-id="241b4-126">If N, the ports listed in the Ports key are all those ports that are not Internet-available.</span></span></td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><span data-ttu-id="241b4-127"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="241b4-127"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="241b4-128">O ou N (ne respecte pas la casse).</span><span class="sxs-lookup"><span data-stu-id="241b4-128">Y or N (not case-sensitive).</span></span> <span data-ttu-id="241b4-129">Spécifie la stratégie par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="241b4-129">Specifies the system default policy.</span></span> <span data-ttu-id="241b4-130">Si Y, les processus utilisant la valeur par défaut sont des ports affectés à partir de l’ensemble de ports disponibles sur Internet, comme défini ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="241b4-130">If Y, the processes using the default will be assigned ports from the set of Internet-available ports, as defined above.</span></span> <span data-ttu-id="241b4-131">Si N, les processus utilisant la valeur par défaut seront affectés aux ports à partir de l’ensemble de ports intranet uniquement.</span><span class="sxs-lookup"><span data-stu-id="241b4-131">If N, processes using the default will be assigned ports from the set of intranet-only ports.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><span data-ttu-id="241b4-132"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="241b4-132"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="241b4-133">Répertorie les noms de toutes les cartes réseau sur lesquelles effectuer la liaison par défaut (par exemple, \Device\AMDPCN1).</span><span class="sxs-lookup"><span data-stu-id="241b4-133">Lists the device names of all the NICs on which to bind by default (for example, \Device\AMDPCN1).</span></span> <span data-ttu-id="241b4-134">Si la clé n’existe pas, le serveur est lié à toutes les cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="241b4-134">If the key does not exist, the server will bind to all NICs.</span></span> <span data-ttu-id="241b4-135">Si la clé existe, le serveur crée une liaison avec les cartes réseau spécifiées dans la clé, à moins que le champ NICFlags ne soit défini sur RPC_C_BIND_TO_ALL_NICS.</span><span class="sxs-lookup"><span data-stu-id="241b4-135">If the key does exist, the server will bind to the NICs specified in the key, unless the NICFlags field is set to RPC_C_BIND_TO_ALL_NICS.</span></span> <span data-ttu-id="241b4-136">Si la clé a une valeur null ( &quot; &quot; ), la configuration est marquée comme non valide et tous les appels à <strong>RpcServerUseProtseq \*</strong> sur <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> ou <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> échouent.</span><span class="sxs-lookup"><span data-stu-id="241b4-136">If the key has a null (&quot;&quot;) value, the configuration will be marked as invalid and all calls to <strong>RpcServerUseProtseq\*</strong> over <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> or <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> will fail.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="241b4-137">Le tableau suivant illustre comment trois exemples d’applications sont affectés par les paramètres définis dans le tableau précédent et comment les paramètres appliqués à l’aide de la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) sont également affectés.</span><span class="sxs-lookup"><span data-stu-id="241b4-137">The following table illustrates how three sample applications are affected by the settings defined in the previous table, and how settings applied using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function are also affected.</span></span>

<span data-ttu-id="241b4-138">Dans cet exemple, trois applications hypothétiques sont prises en compte :</span><span class="sxs-lookup"><span data-stu-id="241b4-138">In this example, three hypothetical applications are considered:</span></span>

-   <span data-ttu-id="241b4-139">Internetapp : cette application est destinée à être exposée à Internet et a spécifié le \_ \_ \_ port Internet RPC utilisé \_ dans le membre **EndpointFlags** de la structure de la [**\_ stratégie RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passée à la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="241b4-139">InternetApp: This application is intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTERNET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="241b4-140">LocalApp : cette application n’est pas destinée à être exposée à Internet, et a spécifié le \_ \_ \_ port intranet RPC use \_ dans le membre **EndpointFlags** de la structure de la [**\_ stratégie RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passée à la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="241b4-140">LocalApp: This application is not intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTRANET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="241b4-141">DefaultApp : cette application spécifie zéro dans le membre **EndpointFlags** de la structure de [**\_ stratégie RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passée à la fonction [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="241b4-141">DefaultApp: This application specifies zero in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>

<span data-ttu-id="241b4-142">Le tableau suivant décrit l’impact de ces paramètres sur les valeurs spécifiées dans les entrées de Registre expliquées dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="241b4-142">The following table explains the impact these settings have based on values specified in the registry entries explained in the previous table.</span></span> <span data-ttu-id="241b4-143">Pour les considérations relatives à la mise en forme, les codes suivants sont affectés :</span><span class="sxs-lookup"><span data-stu-id="241b4-143">For formatting considerations, the following codes are assigned:</span></span>

<span data-ttu-id="241b4-144">Assembly PIA = valeur de clé PortsInternetAvailable</span><span class="sxs-lookup"><span data-stu-id="241b4-144">PIA = PortsInternetAvailable Key value</span></span>

<span data-ttu-id="241b4-145">UIP = valeur de clé de UseInternetPorts</span><span class="sxs-lookup"><span data-stu-id="241b4-145">UIP = UseInternetPorts Key value</span></span>

<span data-ttu-id="241b4-146">La valeur de la clé ports, par souci de cet exemple, est 5000-5100 pour chaque entrée.</span><span class="sxs-lookup"><span data-stu-id="241b4-146">The value of the Ports key, for sake of this example, is 5000-5100 for each entry.</span></span>



| <span data-ttu-id="241b4-147">Application</span><span class="sxs-lookup"><span data-stu-id="241b4-147">Application</span></span> | <span data-ttu-id="241b4-148">PIA</span><span class="sxs-lookup"><span data-stu-id="241b4-148">PIA</span></span> | <span data-ttu-id="241b4-149">UIP</span><span class="sxs-lookup"><span data-stu-id="241b4-149">UIP</span></span> | <span data-ttu-id="241b4-150">Résultats</span><span class="sxs-lookup"><span data-stu-id="241b4-150">Result</span></span>                                  |
|-------------|-----|-----|-----------------------------------------|
| <span data-ttu-id="241b4-151">Internetapp</span><span class="sxs-lookup"><span data-stu-id="241b4-151">InternetApp</span></span> | <span data-ttu-id="241b4-152">O</span><span class="sxs-lookup"><span data-stu-id="241b4-152">Y</span></span>   | <span data-ttu-id="241b4-153">O</span><span class="sxs-lookup"><span data-stu-id="241b4-153">Y</span></span>   | <span data-ttu-id="241b4-154">Utilise des ports entre 5000 et 5100</span><span class="sxs-lookup"><span data-stu-id="241b4-154">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="241b4-155">LocalApp</span><span class="sxs-lookup"><span data-stu-id="241b4-155">LocalApp</span></span>    | <span data-ttu-id="241b4-156">O</span><span class="sxs-lookup"><span data-stu-id="241b4-156">Y</span></span>   | <span data-ttu-id="241b4-157">O</span><span class="sxs-lookup"><span data-stu-id="241b4-157">Y</span></span>   | <span data-ttu-id="241b4-158">Utilise un port en dehors de la plage 5000-5100</span><span class="sxs-lookup"><span data-stu-id="241b4-158">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="241b4-159">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="241b4-159">DefaultApp</span></span>  | <span data-ttu-id="241b4-160">O</span><span class="sxs-lookup"><span data-stu-id="241b4-160">Y</span></span>   | <span data-ttu-id="241b4-161">O</span><span class="sxs-lookup"><span data-stu-id="241b4-161">Y</span></span>   | <span data-ttu-id="241b4-162">Utilise des ports entre 5000 et 5100</span><span class="sxs-lookup"><span data-stu-id="241b4-162">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="241b4-163">Internetapp</span><span class="sxs-lookup"><span data-stu-id="241b4-163">InternetApp</span></span> | <span data-ttu-id="241b4-164">O</span><span class="sxs-lookup"><span data-stu-id="241b4-164">Y</span></span>   | <span data-ttu-id="241b4-165">N</span><span class="sxs-lookup"><span data-stu-id="241b4-165">N</span></span>   | <span data-ttu-id="241b4-166">Utilise des ports entre 5000 et 5100</span><span class="sxs-lookup"><span data-stu-id="241b4-166">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="241b4-167">LocalApp</span><span class="sxs-lookup"><span data-stu-id="241b4-167">LocalApp</span></span>    | <span data-ttu-id="241b4-168">O</span><span class="sxs-lookup"><span data-stu-id="241b4-168">Y</span></span>   | <span data-ttu-id="241b4-169">N</span><span class="sxs-lookup"><span data-stu-id="241b4-169">N</span></span>   | <span data-ttu-id="241b4-170">Utilise un port en dehors de la plage 5000-5100</span><span class="sxs-lookup"><span data-stu-id="241b4-170">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="241b4-171">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="241b4-171">DefaultApp</span></span>  | <span data-ttu-id="241b4-172">O</span><span class="sxs-lookup"><span data-stu-id="241b4-172">Y</span></span>   | <span data-ttu-id="241b4-173">N</span><span class="sxs-lookup"><span data-stu-id="241b4-173">N</span></span>   | <span data-ttu-id="241b4-174">Utilise un port en dehors de la plage 5000-5100</span><span class="sxs-lookup"><span data-stu-id="241b4-174">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="241b4-175">Internetapp</span><span class="sxs-lookup"><span data-stu-id="241b4-175">InternetApp</span></span> | <span data-ttu-id="241b4-176">N</span><span class="sxs-lookup"><span data-stu-id="241b4-176">N</span></span>   | <span data-ttu-id="241b4-177">O</span><span class="sxs-lookup"><span data-stu-id="241b4-177">Y</span></span>   | <span data-ttu-id="241b4-178">Utilise un port en dehors de la plage 5000-5100</span><span class="sxs-lookup"><span data-stu-id="241b4-178">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="241b4-179">LocalApp</span><span class="sxs-lookup"><span data-stu-id="241b4-179">LocalApp</span></span>    | <span data-ttu-id="241b4-180">N</span><span class="sxs-lookup"><span data-stu-id="241b4-180">N</span></span>   | <span data-ttu-id="241b4-181">O</span><span class="sxs-lookup"><span data-stu-id="241b4-181">Y</span></span>   | <span data-ttu-id="241b4-182">Utilise des ports entre 5000 et 5100</span><span class="sxs-lookup"><span data-stu-id="241b4-182">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="241b4-183">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="241b4-183">DefaultApp</span></span>  | <span data-ttu-id="241b4-184">N</span><span class="sxs-lookup"><span data-stu-id="241b4-184">N</span></span>   | <span data-ttu-id="241b4-185">O</span><span class="sxs-lookup"><span data-stu-id="241b4-185">Y</span></span>   | <span data-ttu-id="241b4-186">Utilise un port en dehors de la plage 5000-5100</span><span class="sxs-lookup"><span data-stu-id="241b4-186">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="241b4-187">Internetapp</span><span class="sxs-lookup"><span data-stu-id="241b4-187">InternetApp</span></span> | <span data-ttu-id="241b4-188">N</span><span class="sxs-lookup"><span data-stu-id="241b4-188">N</span></span>   | <span data-ttu-id="241b4-189">N</span><span class="sxs-lookup"><span data-stu-id="241b4-189">N</span></span>   | <span data-ttu-id="241b4-190">Utilise un port en dehors de la plage 5000-5100</span><span class="sxs-lookup"><span data-stu-id="241b4-190">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="241b4-191">LocalApp</span><span class="sxs-lookup"><span data-stu-id="241b4-191">LocalApp</span></span>    | <span data-ttu-id="241b4-192">N</span><span class="sxs-lookup"><span data-stu-id="241b4-192">N</span></span>   | <span data-ttu-id="241b4-193">N</span><span class="sxs-lookup"><span data-stu-id="241b4-193">N</span></span>   | <span data-ttu-id="241b4-194">Utilise des ports entre 5000 et 5100</span><span class="sxs-lookup"><span data-stu-id="241b4-194">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="241b4-195">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="241b4-195">DefaultApp</span></span>  | <span data-ttu-id="241b4-196">N</span><span class="sxs-lookup"><span data-stu-id="241b4-196">N</span></span>   | <span data-ttu-id="241b4-197">N</span><span class="sxs-lookup"><span data-stu-id="241b4-197">N</span></span>   | <span data-ttu-id="241b4-198">Utilise des ports entre 5000 et 5100</span><span class="sxs-lookup"><span data-stu-id="241b4-198">Uses ports between 5000 and 5100</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="241b4-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="241b4-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="241b4-200">**\_stratégie RPC**</span><span class="sxs-lookup"><span data-stu-id="241b4-200">**RPC\_POLICY**</span></span>](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[<span data-ttu-id="241b4-201">**RpcServerUseAllProtseqsEx**</span><span class="sxs-lookup"><span data-stu-id="241b4-201">**RpcServerUseAllProtseqsEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[<span data-ttu-id="241b4-202">**RpcServerUseAllProtseqsIfEx**</span><span class="sxs-lookup"><span data-stu-id="241b4-202">**RpcServerUseAllProtseqsIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[<span data-ttu-id="241b4-203">**RpcServerUseProtseqEx**</span><span class="sxs-lookup"><span data-stu-id="241b4-203">**RpcServerUseProtseqEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[<span data-ttu-id="241b4-204">**RpcServerUseProtseqEpEx**</span><span class="sxs-lookup"><span data-stu-id="241b4-204">**RpcServerUseProtseqEpEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[<span data-ttu-id="241b4-205">**RpcServerUseProtseqIfEx**</span><span class="sxs-lookup"><span data-stu-id="241b4-205">**RpcServerUseProtseqIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[<span data-ttu-id="241b4-206">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="241b4-206">**ncacn\_ip\_tcp**</span></span>](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[<span data-ttu-id="241b4-207">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="241b4-207">**ncadg\_ip\_udp**</span></span>](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 