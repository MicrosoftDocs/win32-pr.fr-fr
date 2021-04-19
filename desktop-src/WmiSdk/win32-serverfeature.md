---
description: La \_ classe Win32 ServerFeature représente les fonctionnalités installées sur un ordinateur exécutant Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Win32_ServerFeature, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: 1be8a2ea1d646e9d882febc7c8eba08b69bb69f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534758"
---
# <a name="win32_serverfeature-class"></a><span data-ttu-id="7c14f-103">\_Classe ServerFeature Win32</span><span class="sxs-lookup"><span data-stu-id="7c14f-103">Win32\_ServerFeature class</span></span>

<span data-ttu-id="7c14f-104">\[La classe **Win32 \_ ServerFeature** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7c14f-104">\[The **Win32\_ServerFeature** class is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7c14f-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7c14f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7c14f-106">Au lieu de cela, utilisez les [classes du fournisseur ServerManager deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span><span class="sxs-lookup"><span data-stu-id="7c14f-106">Instead, use the [ServerManager Deploymentprovider Provider Classes](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span></span>

<span data-ttu-id="7c14f-107">La classe **Win32 \_ ServerFeature** représente les fonctionnalités installées sur un ordinateur exécutant Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7c14f-107">The **Win32\_ServerFeature** class represents the features installed on a computer running Windows Server.</span></span>

<span data-ttu-id="7c14f-108">Cette classe peut être utilisée par les développeurs et les administrateurs qui doivent automatiser le processus de détermination des fonctionnalités installées sur un ensemble d’ordinateurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="7c14f-108">This class can be used by developers and administrators who need to automate the process of determining the features installed on a set of server computers.</span></span> <span data-ttu-id="7c14f-109">Les instances de cette classe ne sont pas disponibles sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="7c14f-109">Instances of this class are not available on client computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c14f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c14f-110">Syntax</span></span>

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="7c14f-111">Membres</span><span class="sxs-lookup"><span data-stu-id="7c14f-111">Members</span></span>

<span data-ttu-id="7c14f-112">La classe **Win32 \_ ServerFeature** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7c14f-112">The **Win32\_ServerFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="7c14f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c14f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c14f-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c14f-114">Properties</span></span>

<span data-ttu-id="7c14f-115">La classe **Win32 \_ ServerFeature** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7c14f-115">The **Win32\_ServerFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c14f-116">**Identifiant**</span><span class="sxs-lookup"><span data-stu-id="7c14f-116">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c14f-117">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c14f-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c14f-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c14f-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7c14f-119">Qualificateurs : [**clé**](key-qualifier.md), [**non \_ null**](optional-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7c14f-119">Qualifiers: [**Key**](key-qualifier.md), [**Not\_Null**](optional-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7c14f-120">ID de la fonctionnalité serveur.</span><span class="sxs-lookup"><span data-stu-id="7c14f-120">Server feature ID.</span></span> <span data-ttu-id="7c14f-121">La liste suivante répertorie les valeurs possibles de la propriété ID :</span><span class="sxs-lookup"><span data-stu-id="7c14f-121">The following list shows the possible values of the ID property:</span></span>



<span data-ttu-id="7c14f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-122">Value</span></span>

<span data-ttu-id="7c14f-123">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-123">Name</span></span>

<span data-ttu-id="7c14f-124">1</span><span class="sxs-lookup"><span data-stu-id="7c14f-124">1</span></span>

[<span data-ttu-id="7c14f-125">Serveur d’applications</span><span class="sxs-lookup"><span data-stu-id="7c14f-125">Application Server</span></span>](/windows)

<span data-ttu-id="7c14f-126">2</span><span class="sxs-lookup"><span data-stu-id="7c14f-126">2</span></span>

<span data-ttu-id="7c14f-127">Serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-127">Web Server (IIS)</span></span>

<span data-ttu-id="7c14f-128">3</span><span class="sxs-lookup"><span data-stu-id="7c14f-128">3</span></span>

[<span data-ttu-id="7c14f-129">Services de diffusion multimédia en continu</span><span class="sxs-lookup"><span data-stu-id="7c14f-129">Streaming Media Services</span></span>](/windows)

<span data-ttu-id="7c14f-130">5</span><span class="sxs-lookup"><span data-stu-id="7c14f-130">5</span></span>

<span data-ttu-id="7c14f-131">Serveur de télécopie</span><span class="sxs-lookup"><span data-stu-id="7c14f-131">Fax Server</span></span>

<span data-ttu-id="7c14f-132">6</span><span class="sxs-lookup"><span data-stu-id="7c14f-132">6</span></span>

<span data-ttu-id="7c14f-133">Services de fichiers et iSCSI</span><span class="sxs-lookup"><span data-stu-id="7c14f-133">File and iSCSI Services</span></span><br/> [<span data-ttu-id="7c14f-134">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-134">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-135">7</span><span class="sxs-lookup"><span data-stu-id="7c14f-135">7</span></span>

<span data-ttu-id="7c14f-136">Services d'impression et de numérisation de document</span><span class="sxs-lookup"><span data-stu-id="7c14f-136">Print and Document Services</span></span><br/> [<span data-ttu-id="7c14f-137">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-137">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-138">8</span><span class="sxs-lookup"><span data-stu-id="7c14f-138">8</span></span>

[<span data-ttu-id="7c14f-139">Active Directory Federation Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-139">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="7c14f-140">9</span><span class="sxs-lookup"><span data-stu-id="7c14f-140">9</span></span>

<span data-ttu-id="7c14f-141">Services AD LDS (Active Directory Lightweight Directory Services)</span><span class="sxs-lookup"><span data-stu-id="7c14f-141">Active Directory Lightweight Directory Services</span></span>

<span data-ttu-id="7c14f-142">10</span><span class="sxs-lookup"><span data-stu-id="7c14f-142">10</span></span>

<span data-ttu-id="7c14f-143">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-143">Active Directory Domain Services</span></span>

<span data-ttu-id="7c14f-144">11</span><span class="sxs-lookup"><span data-stu-id="7c14f-144">11</span></span>

[<span data-ttu-id="7c14f-145">Services UDDI</span><span class="sxs-lookup"><span data-stu-id="7c14f-145">UDDI Services</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-146">12</span><span class="sxs-lookup"><span data-stu-id="7c14f-146">12</span></span>

[<span data-ttu-id="7c14f-147">Serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-147">DHCP Server</span></span>](/windows)

<span data-ttu-id="7c14f-148">13</span><span class="sxs-lookup"><span data-stu-id="7c14f-148">13</span></span>

[<span data-ttu-id="7c14f-149">Serveur DNS</span><span class="sxs-lookup"><span data-stu-id="7c14f-149">DNS Server</span></span>](/windows)

<span data-ttu-id="7c14f-150">14</span><span class="sxs-lookup"><span data-stu-id="7c14f-150">14</span></span>

<span data-ttu-id="7c14f-151">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-151">Network Policy and Access Services</span></span>

<span data-ttu-id="7c14f-152">16</span><span class="sxs-lookup"><span data-stu-id="7c14f-152">16</span></span>

<span data-ttu-id="7c14f-153">Services de certificats Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c14f-153">Active Directory Certificate Services</span></span>

<span data-ttu-id="7c14f-154">17</span><span class="sxs-lookup"><span data-stu-id="7c14f-154">17</span></span>

<span data-ttu-id="7c14f-155">Services AD RMS (Active Directory Rights Management Services)</span><span class="sxs-lookup"><span data-stu-id="7c14f-155">Active Directory Rights Management Services</span></span>

<span data-ttu-id="7c14f-156">18</span><span class="sxs-lookup"><span data-stu-id="7c14f-156">18</span></span>

[<span data-ttu-id="7c14f-157">Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-157">Remote Desktop Services</span></span>](/windows)<br/> [<span data-ttu-id="7c14f-158">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-158">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-159">19</span><span class="sxs-lookup"><span data-stu-id="7c14f-159">19</span></span>

<span data-ttu-id="7c14f-160">Services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-160">Windows Deployment Services</span></span>

<span data-ttu-id="7c14f-161">20</span><span class="sxs-lookup"><span data-stu-id="7c14f-161">20</span></span>

<span data-ttu-id="7c14f-162">Hyper-V</span><span class="sxs-lookup"><span data-stu-id="7c14f-162">Hyper-V</span></span>

<span data-ttu-id="7c14f-163">21</span><span class="sxs-lookup"><span data-stu-id="7c14f-163">21</span></span>

[<span data-ttu-id="7c14f-164">Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-164">Windows Server Update Services</span></span>](/windows)

<span data-ttu-id="7c14f-165">33</span><span class="sxs-lookup"><span data-stu-id="7c14f-165">33</span></span>

[<span data-ttu-id="7c14f-166">Clustering de basculement</span><span class="sxs-lookup"><span data-stu-id="7c14f-166">Failover Clustering</span></span>](/windows)

<span data-ttu-id="7c14f-167">34</span><span class="sxs-lookup"><span data-stu-id="7c14f-167">34</span></span>

[<span data-ttu-id="7c14f-168">Équilibrage de la charge réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-168">Network Load Balancing</span></span>](/windows)

<span data-ttu-id="7c14f-169">36</span><span class="sxs-lookup"><span data-stu-id="7c14f-169">36</span></span>

[<span data-ttu-id="7c14f-170">Fonctionnalités .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="7c14f-170">.NET Framework 3.5.1 Features</span></span>](/windows)<br/> [<span data-ttu-id="7c14f-171">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-171">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-172">37</span><span class="sxs-lookup"><span data-stu-id="7c14f-172">37</span></span>

[<span data-ttu-id="7c14f-173">Gestionnaire de ressources système Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-173">Windows System Resource Manager</span></span>](/windows)

<span data-ttu-id="7c14f-174">38</span><span class="sxs-lookup"><span data-stu-id="7c14f-174">38</span></span>

<span data-ttu-id="7c14f-175">Service de réseau local sans fil</span><span class="sxs-lookup"><span data-stu-id="7c14f-175">Wireless LAN Service</span></span>

<span data-ttu-id="7c14f-176">39</span><span class="sxs-lookup"><span data-stu-id="7c14f-176">39</span></span>

[<span data-ttu-id="7c14f-177">Fonctionnalités de Sauvegarde Windows Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-177">Windows Server Backup Features</span></span>](/windows)

<span data-ttu-id="7c14f-178">40</span><span class="sxs-lookup"><span data-stu-id="7c14f-178">40</span></span>

<span data-ttu-id="7c14f-179">Serveur WINS</span><span class="sxs-lookup"><span data-stu-id="7c14f-179">WINS Server</span></span>

<span data-ttu-id="7c14f-180">41</span><span class="sxs-lookup"><span data-stu-id="7c14f-180">41</span></span>

<span data-ttu-id="7c14f-181">Service d’activation des processus Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-181">Windows Process Activation Service</span></span>

<span data-ttu-id="7c14f-182">42</span><span class="sxs-lookup"><span data-stu-id="7c14f-182">42</span></span>

[<span data-ttu-id="7c14f-183">Assistance à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-183">Remote Assistance</span></span>](/windows)

<span data-ttu-id="7c14f-184">43</span><span class="sxs-lookup"><span data-stu-id="7c14f-184">43</span></span>

<span data-ttu-id="7c14f-185">Services TCP/IP simples</span><span class="sxs-lookup"><span data-stu-id="7c14f-185">Simple TCP/IP Services</span></span>

<span data-ttu-id="7c14f-186">44</span><span class="sxs-lookup"><span data-stu-id="7c14f-186">44</span></span>

[<span data-ttu-id="7c14f-187">Client Telnet</span><span class="sxs-lookup"><span data-stu-id="7c14f-187">Telnet Client</span></span>](/windows)

<span data-ttu-id="7c14f-188">45</span><span class="sxs-lookup"><span data-stu-id="7c14f-188">45</span></span>

[<span data-ttu-id="7c14f-189">Serveur Telnet</span><span class="sxs-lookup"><span data-stu-id="7c14f-189">Telnet Server</span></span>](/windows)

<span data-ttu-id="7c14f-190">46</span><span class="sxs-lookup"><span data-stu-id="7c14f-190">46</span></span>

[<span data-ttu-id="7c14f-191">Sous-système pour les applications UNIX</span><span class="sxs-lookup"><span data-stu-id="7c14f-191">Subsystem For Unix-based Applications</span></span>](/windows)

<span data-ttu-id="7c14f-192">47</span><span class="sxs-lookup"><span data-stu-id="7c14f-192">47</span></span>

<span data-ttu-id="7c14f-193">Proxy RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-193">RPC Over HTTP Proxy</span></span>

<span data-ttu-id="7c14f-194">48</span><span class="sxs-lookup"><span data-stu-id="7c14f-194">48</span></span>

<span data-ttu-id="7c14f-195">SMTP Server (Serveur SMTP)</span><span class="sxs-lookup"><span data-stu-id="7c14f-195">SMTP Server</span></span>

<span data-ttu-id="7c14f-196">49</span><span class="sxs-lookup"><span data-stu-id="7c14f-196">49</span></span>

<span data-ttu-id="7c14f-197">Message Queuing</span><span class="sxs-lookup"><span data-stu-id="7c14f-197">Message Queuing</span></span>

<span data-ttu-id="7c14f-198">51</span><span class="sxs-lookup"><span data-stu-id="7c14f-198">51</span></span>

[<span data-ttu-id="7c14f-199">Base de données interne Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-199">Windows Internal Database</span></span>](/windows)

<span data-ttu-id="7c14f-200">52</span><span class="sxs-lookup"><span data-stu-id="7c14f-200">52</span></span>

[<span data-ttu-id="7c14f-201">Gestionnaire de stockage pour réseau San</span><span class="sxs-lookup"><span data-stu-id="7c14f-201">Storage Manager For SANs</span></span>](/windows)

<span data-ttu-id="7c14f-202">53</span><span class="sxs-lookup"><span data-stu-id="7c14f-202">53</span></span>

<span data-ttu-id="7c14f-203">Moniteur de port LPR</span><span class="sxs-lookup"><span data-stu-id="7c14f-203">LPR Port Monitor</span></span>

<span data-ttu-id="7c14f-204">55</span><span class="sxs-lookup"><span data-stu-id="7c14f-204">55</span></span>

[<span data-ttu-id="7c14f-205">Serveur de nom de stockage Internet</span><span class="sxs-lookup"><span data-stu-id="7c14f-205">Internet Storage Name Server</span></span>](/windows)

<span data-ttu-id="7c14f-206">57</span><span class="sxs-lookup"><span data-stu-id="7c14f-206">57</span></span>

[<span data-ttu-id="7c14f-207">MPIO (Multipath I/O)</span><span class="sxs-lookup"><span data-stu-id="7c14f-207">Multipath I/O</span></span>](/windows)

<span data-ttu-id="7c14f-208">58</span><span class="sxs-lookup"><span data-stu-id="7c14f-208">58</span></span>

<span data-ttu-id="7c14f-209">Client TFTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-209">TFTP Client</span></span>

<span data-ttu-id="7c14f-210">59</span><span class="sxs-lookup"><span data-stu-id="7c14f-210">59</span></span>

[<span data-ttu-id="7c14f-211">Services SNMP</span><span class="sxs-lookup"><span data-stu-id="7c14f-211">SNMP Services</span></span>](/windows)

<span data-ttu-id="7c14f-212">60</span><span class="sxs-lookup"><span data-stu-id="7c14f-212">60</span></span>

[<span data-ttu-id="7c14f-213">Gestionnaire de stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7c14f-213">Removable Storage Manager</span></span>](/windows)

<span data-ttu-id="7c14f-214">61</span><span class="sxs-lookup"><span data-stu-id="7c14f-214">61</span></span>

<span data-ttu-id="7c14f-215">Chiffrement de lecteur BitLocker</span><span class="sxs-lookup"><span data-stu-id="7c14f-215">BitLocker Drive Encryption</span></span>

<span data-ttu-id="7c14f-216">62</span><span class="sxs-lookup"><span data-stu-id="7c14f-216">62</span></span>

[<span data-ttu-id="7c14f-217">Services pour le système de fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-217">Services For Network File System</span></span>](/windows)

<span data-ttu-id="7c14f-218">63</span><span class="sxs-lookup"><span data-stu-id="7c14f-218">63</span></span>

<span data-ttu-id="7c14f-219">Client d'impression Internet</span><span class="sxs-lookup"><span data-stu-id="7c14f-219">Internet Printing Client</span></span>

<span data-ttu-id="7c14f-220">64</span><span class="sxs-lookup"><span data-stu-id="7c14f-220">64</span></span>

[<span data-ttu-id="7c14f-221">Protocole PNRP (Peer Name Resolution Protocol)</span><span class="sxs-lookup"><span data-stu-id="7c14f-221">Peer Name Resolution Protocol</span></span>](/windows)

<span data-ttu-id="7c14f-222">65</span><span class="sxs-lookup"><span data-stu-id="7c14f-222">65</span></span>

<span data-ttu-id="7c14f-223">Kit d'administration du Gestionnaire des connexions Microsoft</span><span class="sxs-lookup"><span data-stu-id="7c14f-223">Connection Manager Administration Kit</span></span>

<span data-ttu-id="7c14f-224">66</span><span class="sxs-lookup"><span data-stu-id="7c14f-224">66</span></span>

[<span data-ttu-id="7c14f-225">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-225">Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-226">67</span><span class="sxs-lookup"><span data-stu-id="7c14f-226">67</span></span>

[<span data-ttu-id="7c14f-227">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="7c14f-227">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="7c14f-228">68</span><span class="sxs-lookup"><span data-stu-id="7c14f-228">68</span></span>

[<span data-ttu-id="7c14f-229">Expérience audio-vidéo haute qualité Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-229">Quality Windows Audio Video Experience</span></span>](/windows)

<span data-ttu-id="7c14f-230">69</span><span class="sxs-lookup"><span data-stu-id="7c14f-230">69</span></span>

[<span data-ttu-id="7c14f-231">Gestion des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="7c14f-231">Group Policy Management</span></span>](/windows)

<span data-ttu-id="7c14f-232">71</span><span class="sxs-lookup"><span data-stu-id="7c14f-232">71</span></span>

[<span data-ttu-id="7c14f-233">service d'indexation</span><span class="sxs-lookup"><span data-stu-id="7c14f-233">Indexing Service</span></span>](/windows)

<span data-ttu-id="7c14f-234">72</span><span class="sxs-lookup"><span data-stu-id="7c14f-234">72</span></span>

[<span data-ttu-id="7c14f-235">Gestionnaire de ressources du serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-235">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="7c14f-236">73</span><span class="sxs-lookup"><span data-stu-id="7c14f-236">73</span></span>

<span data-ttu-id="7c14f-237">Compression différentielle à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-237">Remote Differential Compression</span></span>

<span data-ttu-id="7c14f-238">310</span><span class="sxs-lookup"><span data-stu-id="7c14f-238">310</span></span>

<span data-ttu-id="7c14f-239">Services de prise en charge de l'écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="7c14f-239">Ink and Handwriting Services</span></span><br/>

<span data-ttu-id="7c14f-240">320</span><span class="sxs-lookup"><span data-stu-id="7c14f-240">320</span></span>

[<span data-ttu-id="7c14f-241">Outils de migration de Windows Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-241">Windows Server Migration Tools</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-242">321</span><span class="sxs-lookup"><span data-stu-id="7c14f-242">321</span></span>

[<span data-ttu-id="7c14f-243">Extension WinRM IIS</span><span class="sxs-lookup"><span data-stu-id="7c14f-243">WinRM IIS Extension</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-244">324</span><span class="sxs-lookup"><span data-stu-id="7c14f-244">324</span></span>

[<span data-ttu-id="7c14f-245">BranchCache</span><span class="sxs-lookup"><span data-stu-id="7c14f-245">BranchCache</span></span>](#branchcache)<br/>

<span data-ttu-id="7c14f-246">334</span><span class="sxs-lookup"><span data-stu-id="7c14f-246">334</span></span>

[<span data-ttu-id="7c14f-247">Console de gestion DirectAccess</span><span class="sxs-lookup"><span data-stu-id="7c14f-247">DirectAccess Management Console</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-248">335</span><span class="sxs-lookup"><span data-stu-id="7c14f-248">335</span></span>

[<span data-ttu-id="7c14f-249">Service de transfert intelligent en arrière-plan (BITS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-249">Background Intelligent Transfer Service (BITS)</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-250">338</span><span class="sxs-lookup"><span data-stu-id="7c14f-250">338</span></span>

[<span data-ttu-id="7c14f-251">Visionneuse XPS</span><span class="sxs-lookup"><span data-stu-id="7c14f-251">XPS Viewer</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-252">339</span><span class="sxs-lookup"><span data-stu-id="7c14f-252">339</span></span>

[<span data-ttu-id="7c14f-253">Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="7c14f-253">Windows Biometric Framework</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-254">340</span><span class="sxs-lookup"><span data-stu-id="7c14f-254">340</span></span>

<span data-ttu-id="7c14f-255">Prise en charge WoW64</span><span class="sxs-lookup"><span data-stu-id="7c14f-255">WoW64 Support</span></span><br/>

<span data-ttu-id="7c14f-256">351</span><span class="sxs-lookup"><span data-stu-id="7c14f-256">351</span></span>

[<span data-ttu-id="7c14f-257">Environnement d’écriture de scripts intégré de Windows PowerShell (ISE)</span><span class="sxs-lookup"><span data-stu-id="7c14f-257">Windows PowerShell Integrated Scripting Environment (ISE)</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-258">352</span><span class="sxs-lookup"><span data-stu-id="7c14f-258">352</span></span>

<span data-ttu-id="7c14f-259">Windows TIFF IFilter</span><span class="sxs-lookup"><span data-stu-id="7c14f-259">Windows TIFF IFilter</span></span><br/>

<span data-ttu-id="7c14f-260">404</span><span class="sxs-lookup"><span data-stu-id="7c14f-260">404</span></span>

[<span data-ttu-id="7c14f-261">Services de mise à jour Windows Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-261">Window Server Update Services</span></span>](/windows)

<span data-ttu-id="7c14f-262">409</span><span class="sxs-lookup"><span data-stu-id="7c14f-262">409</span></span>

[<span data-ttu-id="7c14f-263">Serveur de gestion des adresses IP (IPAM)</span><span class="sxs-lookup"><span data-stu-id="7c14f-263">IP Address Management (IPAM) Server</span></span>](/windows)

<span data-ttu-id="7c14f-264">417</span><span class="sxs-lookup"><span data-stu-id="7c14f-264">417</span></span>

[<span data-ttu-id="7c14f-265">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-265">Windows PowerShell</span></span>](/windows)

<span data-ttu-id="7c14f-266">418</span><span class="sxs-lookup"><span data-stu-id="7c14f-266">418</span></span>

[<span data-ttu-id="7c14f-267">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="7c14f-267">.NET Framework 4.5</span></span>](/windows)

<span data-ttu-id="7c14f-268">432</span><span class="sxs-lookup"><span data-stu-id="7c14f-268">432</span></span>

[<span data-ttu-id="7c14f-269">Service Windows Search</span><span class="sxs-lookup"><span data-stu-id="7c14f-269">Windows Search Service</span></span>](/windows)

<span data-ttu-id="7c14f-270">438</span><span class="sxs-lookup"><span data-stu-id="7c14f-270">438</span></span>

[<span data-ttu-id="7c14f-271">Client pour NFS</span><span class="sxs-lookup"><span data-stu-id="7c14f-271">Client for NFS</span></span>](/windows)

<span data-ttu-id="7c14f-272">441</span><span class="sxs-lookup"><span data-stu-id="7c14f-272">441</span></span>

[<span data-ttu-id="7c14f-273">Déverrouillage réseau BitLocker</span><span class="sxs-lookup"><span data-stu-id="7c14f-273">BitLocker Network Unlock</span></span>](/windows)

<span data-ttu-id="7c14f-274">442</span><span class="sxs-lookup"><span data-stu-id="7c14f-274">442</span></span>

[<span data-ttu-id="7c14f-275">Extension ISS Management OData</span><span class="sxs-lookup"><span data-stu-id="7c14f-275">Management OData IIS Extension</span></span>](/windows)

<span data-ttu-id="7c14f-276">450</span><span class="sxs-lookup"><span data-stu-id="7c14f-276">450</span></span>

[<span data-ttu-id="7c14f-277">.NET Framework 4.5 Advanced Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-277">.NET Framework 4.5 Advanced Services</span></span>](/windows)

<span data-ttu-id="7c14f-278">466</span><span class="sxs-lookup"><span data-stu-id="7c14f-278">466</span></span>

[<span data-ttu-id="7c14f-279">Fonctionnalités de .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="7c14f-279">.NET Framework 4.5 Features</span></span>](/windows)

<span data-ttu-id="7c14f-280">468</span><span class="sxs-lookup"><span data-stu-id="7c14f-280">468</span></span>

[<span data-ttu-id="7c14f-281">Accès à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-281">Remote Access</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-282">477</span><span class="sxs-lookup"><span data-stu-id="7c14f-282">477</span></span>

[<span data-ttu-id="7c14f-283">Interfaces utilisateur et infrastructure</span><span class="sxs-lookup"><span data-stu-id="7c14f-283">User Interfaces and Infrastructure</span></span>](/windows)

<span data-ttu-id="7c14f-284">478</span><span class="sxs-lookup"><span data-stu-id="7c14f-284">478</span></span>

[<span data-ttu-id="7c14f-285">Outils de gestion graphiques et infrastructure</span><span class="sxs-lookup"><span data-stu-id="7c14f-285">Graphical Management Tools and Infrastructure</span></span>](/windows)

<span data-ttu-id="7c14f-286">481</span><span class="sxs-lookup"><span data-stu-id="7c14f-286">481</span></span>

[<span data-ttu-id="7c14f-287">Services de fichiers et de stockage</span><span class="sxs-lookup"><span data-stu-id="7c14f-287">File and Storage Services</span></span>](/windows)

<span data-ttu-id="7c14f-288">485</span><span class="sxs-lookup"><span data-stu-id="7c14f-288">485</span></span>

[<span data-ttu-id="7c14f-289">Expérience Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="7c14f-289">Windows Server Essentials Experience</span></span>](/windows)

<span data-ttu-id="7c14f-290">488</span><span class="sxs-lookup"><span data-stu-id="7c14f-290">488</span></span>

[<span data-ttu-id="7c14f-291">DirectPlay</span><span class="sxs-lookup"><span data-stu-id="7c14f-291">Direct Play</span></span>](/windows)

<span data-ttu-id="7c14f-292">Services de fichiers-services de rôle (6)</span><span class="sxs-lookup"><span data-stu-id="7c14f-292">File Services - Role Services (6)</span></span>

<span data-ttu-id="7c14f-293">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-293">Value</span></span>

<span data-ttu-id="7c14f-294">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-294">Name</span></span>

<span data-ttu-id="7c14f-295">100</span><span class="sxs-lookup"><span data-stu-id="7c14f-295">100</span></span>

[<span data-ttu-id="7c14f-296">système de fichiers DFS</span><span class="sxs-lookup"><span data-stu-id="7c14f-296">Distributed File System</span></span>](/windows)

<span data-ttu-id="7c14f-297">101</span><span class="sxs-lookup"><span data-stu-id="7c14f-297">101</span></span>

<span data-ttu-id="7c14f-298">Espace de noms DFS</span><span class="sxs-lookup"><span data-stu-id="7c14f-298">DFS Namespace</span></span>

<span data-ttu-id="7c14f-299">102</span><span class="sxs-lookup"><span data-stu-id="7c14f-299">102</span></span>

<span data-ttu-id="7c14f-300">Réplication DFS</span><span class="sxs-lookup"><span data-stu-id="7c14f-300">DFS Replication</span></span>

<span data-ttu-id="7c14f-301">103</span><span class="sxs-lookup"><span data-stu-id="7c14f-301">103</span></span>

[<span data-ttu-id="7c14f-302">Service de réplication de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-302">File Replication Service</span></span>](/windows)

<span data-ttu-id="7c14f-303">104</span><span class="sxs-lookup"><span data-stu-id="7c14f-303">104</span></span>

[<span data-ttu-id="7c14f-304">Gestionnaire de ressources du serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-304">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="7c14f-305">105</span><span class="sxs-lookup"><span data-stu-id="7c14f-305">105</span></span>

[<span data-ttu-id="7c14f-306">Services pour le système de fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-306">Services For Network File System</span></span>](/windows)

<span data-ttu-id="7c14f-307">106</span><span class="sxs-lookup"><span data-stu-id="7c14f-307">106</span></span>

[<span data-ttu-id="7c14f-308">Stockage d’instance simple</span><span class="sxs-lookup"><span data-stu-id="7c14f-308">Single Instance Storage</span></span>](/windows)

<span data-ttu-id="7c14f-309">107</span><span class="sxs-lookup"><span data-stu-id="7c14f-309">107</span></span>

[<span data-ttu-id="7c14f-310">Service Windows Search</span><span class="sxs-lookup"><span data-stu-id="7c14f-310">Windows Search Service</span></span>](/windows)

<span data-ttu-id="7c14f-311">108</span><span class="sxs-lookup"><span data-stu-id="7c14f-311">108</span></span>

[<span data-ttu-id="7c14f-312">service d'indexation</span><span class="sxs-lookup"><span data-stu-id="7c14f-312">Indexing Service</span></span>](/windows)

<span data-ttu-id="7c14f-313">255</span><span class="sxs-lookup"><span data-stu-id="7c14f-313">255</span></span>

<span data-ttu-id="7c14f-314">Serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-314">File Server</span></span>

<span data-ttu-id="7c14f-315">350</span><span class="sxs-lookup"><span data-stu-id="7c14f-315">350</span></span>

<span data-ttu-id="7c14f-316">BranchCache pour fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-316">BranchCache for Network Files</span></span>

<span data-ttu-id="7c14f-317">431</span><span class="sxs-lookup"><span data-stu-id="7c14f-317">431</span></span>

[<span data-ttu-id="7c14f-318">Serveur pour NFS</span><span class="sxs-lookup"><span data-stu-id="7c14f-318">Server for NFS</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-319">434</span><span class="sxs-lookup"><span data-stu-id="7c14f-319">434</span></span>

[<span data-ttu-id="7c14f-320">Service Agent VSS du serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-320">File Server VSS Agent Service</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-321">435</span><span class="sxs-lookup"><span data-stu-id="7c14f-321">435</span></span>

[<span data-ttu-id="7c14f-322">Serveur cible iSCSI</span><span class="sxs-lookup"><span data-stu-id="7c14f-322">iSCSI Target Server</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-323">436</span><span class="sxs-lookup"><span data-stu-id="7c14f-323">436</span></span>

[<span data-ttu-id="7c14f-324">Déduplication des données</span><span class="sxs-lookup"><span data-stu-id="7c14f-324">Data Deduplication</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-325">437</span><span class="sxs-lookup"><span data-stu-id="7c14f-325">437</span></span>

[<span data-ttu-id="7c14f-326">Fournisseur de stockage cible iSCSI (fournisseurs de matériel VDS et VSS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-326">iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>](/windows)

<span data-ttu-id="7c14f-327">486</span><span class="sxs-lookup"><span data-stu-id="7c14f-327">486</span></span>

[<span data-ttu-id="7c14f-328">Dossiers de travail</span><span class="sxs-lookup"><span data-stu-id="7c14f-328">Work Folders</span></span>](/windows)

<span data-ttu-id="7c14f-329">Services de rôle AD DS (10)</span><span class="sxs-lookup"><span data-stu-id="7c14f-329">AD DS - Role Services (10)</span></span>

<span data-ttu-id="7c14f-330">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-330">Value</span></span>

<span data-ttu-id="7c14f-331">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-331">Name</span></span>

<span data-ttu-id="7c14f-332">110</span><span class="sxs-lookup"><span data-stu-id="7c14f-332">110</span></span>

[<span data-ttu-id="7c14f-333">Contrôleur de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c14f-333">Active Directory Domain Controller</span></span>](/windows)

<span data-ttu-id="7c14f-334">111</span><span class="sxs-lookup"><span data-stu-id="7c14f-334">111</span></span>

[<span data-ttu-id="7c14f-335">Gestion des identités pour UNIX</span><span class="sxs-lookup"><span data-stu-id="7c14f-335">Identity Management For Unix</span></span>](/windows)

<span data-ttu-id="7c14f-336">112</span><span class="sxs-lookup"><span data-stu-id="7c14f-336">112</span></span>

[<span data-ttu-id="7c14f-337">Serveur pour Network Information Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-337">Server For Network Information Services</span></span>](/windows)

<span data-ttu-id="7c14f-338">113</span><span class="sxs-lookup"><span data-stu-id="7c14f-338">113</span></span>

[<span data-ttu-id="7c14f-339">Synchronisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="7c14f-339">Password Synchronization</span></span>](/windows)

<span data-ttu-id="7c14f-340">294</span><span class="sxs-lookup"><span data-stu-id="7c14f-340">294</span></span>

[<span data-ttu-id="7c14f-341">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="7c14f-341">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="7c14f-342">Diffusion multimédia-services de rôle (3)</span><span class="sxs-lookup"><span data-stu-id="7c14f-342">Streaming Media - Role Services (3)</span></span>

<span data-ttu-id="7c14f-343">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-343">Value</span></span>

<span data-ttu-id="7c14f-344">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-344">Name</span></span>

<span data-ttu-id="7c14f-345">120</span><span class="sxs-lookup"><span data-stu-id="7c14f-345">120</span></span>

[<span data-ttu-id="7c14f-346">Serveur Windows Media</span><span class="sxs-lookup"><span data-stu-id="7c14f-346">Windows Media Server</span></span>](/windows)

<span data-ttu-id="7c14f-347">121</span><span class="sxs-lookup"><span data-stu-id="7c14f-347">121</span></span>

[<span data-ttu-id="7c14f-348">Administration basée sur le Web</span><span class="sxs-lookup"><span data-stu-id="7c14f-348">Web-based Administration</span></span>](/windows)

<span data-ttu-id="7c14f-349">122</span><span class="sxs-lookup"><span data-stu-id="7c14f-349">122</span></span>

[<span data-ttu-id="7c14f-350">Agent de journalisation</span><span class="sxs-lookup"><span data-stu-id="7c14f-350">Logging Agent</span></span>](/windows)

<span data-ttu-id="7c14f-351">ADFS-services de rôle (8)</span><span class="sxs-lookup"><span data-stu-id="7c14f-351">ADFS - Role Services (8)</span></span>

<span data-ttu-id="7c14f-352">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-352">Value</span></span>

<span data-ttu-id="7c14f-353">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-353">Name</span></span>

<span data-ttu-id="7c14f-354">125</span><span class="sxs-lookup"><span data-stu-id="7c14f-354">125</span></span>

[<span data-ttu-id="7c14f-355">Active Directory Federation Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-355">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="7c14f-356">126</span><span class="sxs-lookup"><span data-stu-id="7c14f-356">126</span></span>

[<span data-ttu-id="7c14f-357">Stratégie de service FS (Federation Service)</span><span class="sxs-lookup"><span data-stu-id="7c14f-357">Federation Service Policy</span></span>](/windows)

<span data-ttu-id="7c14f-358">127</span><span class="sxs-lookup"><span data-stu-id="7c14f-358">127</span></span>

[<span data-ttu-id="7c14f-359">Agents Web AD FS</span><span class="sxs-lookup"><span data-stu-id="7c14f-359">AD FS Web Agents</span></span>](/windows)

<span data-ttu-id="7c14f-360">128</span><span class="sxs-lookup"><span data-stu-id="7c14f-360">128</span></span>

[<span data-ttu-id="7c14f-361">Agent prenant en charge les revendications</span><span class="sxs-lookup"><span data-stu-id="7c14f-361">Claims-aware Agent</span></span>](/windows)

<span data-ttu-id="7c14f-362">129</span><span class="sxs-lookup"><span data-stu-id="7c14f-362">129</span></span>

[<span data-ttu-id="7c14f-363">Agent basé sur les jetons Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-363">Windows Token-based Agent</span></span>](/windows)

<span data-ttu-id="7c14f-364">Services de rôle Services Bureau à distance (18)</span><span class="sxs-lookup"><span data-stu-id="7c14f-364">Remote Desktop Services - Role Services (18)</span></span>

<span data-ttu-id="7c14f-365">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-365">Value</span></span>

<span data-ttu-id="7c14f-366">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-366">Name</span></span>

<span data-ttu-id="7c14f-367">130</span><span class="sxs-lookup"><span data-stu-id="7c14f-367">130</span></span>

<span data-ttu-id="7c14f-368">Hôte de session Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-368">Remote Desktop Session Host</span></span><br/> [<span data-ttu-id="7c14f-369">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-369">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-370">131</span><span class="sxs-lookup"><span data-stu-id="7c14f-370">131</span></span>

[<span data-ttu-id="7c14f-371">Gestionnaire de licences des services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-371">Remote Desktop Licensing</span></span>](/windows)<br/> [<span data-ttu-id="7c14f-372">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-372">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-373">132</span><span class="sxs-lookup"><span data-stu-id="7c14f-373">132</span></span>

<span data-ttu-id="7c14f-374">Passerelle des services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-374">Remote Desktop Gateway</span></span><br/> [<span data-ttu-id="7c14f-375">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-375">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-376">133</span><span class="sxs-lookup"><span data-stu-id="7c14f-376">133</span></span>

<span data-ttu-id="7c14f-377">Service Broker pour les connexions Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-377">Remote Desktop Connection Broker</span></span><br/> [<span data-ttu-id="7c14f-378">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-378">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-379">134</span><span class="sxs-lookup"><span data-stu-id="7c14f-379">134</span></span>

<span data-ttu-id="7c14f-380">Accès web au Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-380">Remote Desktop Web Access</span></span><br/> [<span data-ttu-id="7c14f-381">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-381">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-382">322</span><span class="sxs-lookup"><span data-stu-id="7c14f-382">322</span></span>

<span data-ttu-id="7c14f-383">Hôte de virtualisation des services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-383">Remote Desktop Virtualization Host</span></span><br/>

<span data-ttu-id="7c14f-384">Services de rôle serveur hôte de virtualisation des services Bureau à distance (322)</span><span class="sxs-lookup"><span data-stu-id="7c14f-384">Remote Desktop Virtualization Host - Role Services (322)</span></span>

<span data-ttu-id="7c14f-385">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-385">Value</span></span>

<span data-ttu-id="7c14f-386">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-386">Name</span></span>

<span data-ttu-id="7c14f-387">325</span><span class="sxs-lookup"><span data-stu-id="7c14f-387">325</span></span>

[<span data-ttu-id="7c14f-388">Services principaux</span><span class="sxs-lookup"><span data-stu-id="7c14f-388">Core Services</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-389">327</span><span class="sxs-lookup"><span data-stu-id="7c14f-389">327</span></span>

[<span data-ttu-id="7c14f-390">Graphiques virtuels Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-390">Remote Desktop Virtual Graphics</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-391">Services de rôle Services d’impression et de numérisation de document (7)</span><span class="sxs-lookup"><span data-stu-id="7c14f-391">Print and Document Services - Role Services (7)</span></span>

<span data-ttu-id="7c14f-392">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-392">Value</span></span>

<span data-ttu-id="7c14f-393">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-393">Name</span></span>

<span data-ttu-id="7c14f-394">135</span><span class="sxs-lookup"><span data-stu-id="7c14f-394">135</span></span>

<span data-ttu-id="7c14f-395">Serveur d’impression</span><span class="sxs-lookup"><span data-stu-id="7c14f-395">Print Server</span></span>

<span data-ttu-id="7c14f-396">136</span><span class="sxs-lookup"><span data-stu-id="7c14f-396">136</span></span>

<span data-ttu-id="7c14f-397">Impression Internet</span><span class="sxs-lookup"><span data-stu-id="7c14f-397">Internet Printing</span></span>

<span data-ttu-id="7c14f-398">137</span><span class="sxs-lookup"><span data-stu-id="7c14f-398">137</span></span>

<span data-ttu-id="7c14f-399">Service d’impression LPD</span><span class="sxs-lookup"><span data-stu-id="7c14f-399">LPD Print Service</span></span>

<span data-ttu-id="7c14f-400">328</span><span class="sxs-lookup"><span data-stu-id="7c14f-400">328</span></span>

[<span data-ttu-id="7c14f-401">Serveur de numérisation distribuée</span><span class="sxs-lookup"><span data-stu-id="7c14f-401">Distributed Scan Server</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-402">Serveur Web (IIS)-services de rôle (2)</span><span class="sxs-lookup"><span data-stu-id="7c14f-402">Web Server (IIS) - Role Services (2)</span></span>

<span data-ttu-id="7c14f-403">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-403">Value</span></span>

<span data-ttu-id="7c14f-404">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-404">Name</span></span>

<span data-ttu-id="7c14f-405">140</span><span class="sxs-lookup"><span data-stu-id="7c14f-405">140</span></span>

<span data-ttu-id="7c14f-406">Serveur web</span><span class="sxs-lookup"><span data-stu-id="7c14f-406">Web Server</span></span>

<span data-ttu-id="7c14f-407">141</span><span class="sxs-lookup"><span data-stu-id="7c14f-407">141</span></span>

<span data-ttu-id="7c14f-408">Fonctionnalités HTTP communes</span><span class="sxs-lookup"><span data-stu-id="7c14f-408">Common HTTP Features</span></span>

<span data-ttu-id="7c14f-409">142</span><span class="sxs-lookup"><span data-stu-id="7c14f-409">142</span></span>

<span data-ttu-id="7c14f-410">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="7c14f-410">Static Content</span></span>

<span data-ttu-id="7c14f-411">143</span><span class="sxs-lookup"><span data-stu-id="7c14f-411">143</span></span>

<span data-ttu-id="7c14f-412">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="7c14f-412">Default Document</span></span>

<span data-ttu-id="7c14f-413">144</span><span class="sxs-lookup"><span data-stu-id="7c14f-413">144</span></span>

<span data-ttu-id="7c14f-414">Parcourir le répertoire</span><span class="sxs-lookup"><span data-stu-id="7c14f-414">Directory Browse</span></span>

<span data-ttu-id="7c14f-415">145</span><span class="sxs-lookup"><span data-stu-id="7c14f-415">145</span></span>

<span data-ttu-id="7c14f-416">Erreurs HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-416">HTTP Errors</span></span>

<span data-ttu-id="7c14f-417">146</span><span class="sxs-lookup"><span data-stu-id="7c14f-417">146</span></span>

<span data-ttu-id="7c14f-418">Redirection HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-418">HTTP Redirection</span></span>

<span data-ttu-id="7c14f-419">147</span><span class="sxs-lookup"><span data-stu-id="7c14f-419">147</span></span>

<span data-ttu-id="7c14f-420">Développement d'applications</span><span class="sxs-lookup"><span data-stu-id="7c14f-420">Application Development</span></span>

<span data-ttu-id="7c14f-421">148</span><span class="sxs-lookup"><span data-stu-id="7c14f-421">148</span></span>

<span data-ttu-id="7c14f-422">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="7c14f-422">ASP.NET</span></span>

<span data-ttu-id="7c14f-423">149</span><span class="sxs-lookup"><span data-stu-id="7c14f-423">149</span></span>

<span data-ttu-id="7c14f-424">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="7c14f-424">.NET Extensibility</span></span>

<span data-ttu-id="7c14f-425">150</span><span class="sxs-lookup"><span data-stu-id="7c14f-425">150</span></span>

<span data-ttu-id="7c14f-426">ASP</span><span class="sxs-lookup"><span data-stu-id="7c14f-426">ASP</span></span>

<span data-ttu-id="7c14f-427">151</span><span class="sxs-lookup"><span data-stu-id="7c14f-427">151</span></span>

<span data-ttu-id="7c14f-428">CGI</span><span class="sxs-lookup"><span data-stu-id="7c14f-428">CGI</span></span>

<span data-ttu-id="7c14f-429">152</span><span class="sxs-lookup"><span data-stu-id="7c14f-429">152</span></span>

<span data-ttu-id="7c14f-430">Extensions ISAPI</span><span class="sxs-lookup"><span data-stu-id="7c14f-430">ISAPI Extensions</span></span>

<span data-ttu-id="7c14f-431">153</span><span class="sxs-lookup"><span data-stu-id="7c14f-431">153</span></span>

<span data-ttu-id="7c14f-432">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="7c14f-432">ISAPI Filters</span></span>

<span data-ttu-id="7c14f-433">154</span><span class="sxs-lookup"><span data-stu-id="7c14f-433">154</span></span>

<span data-ttu-id="7c14f-434">Fichiers Include côté serveur</span><span class="sxs-lookup"><span data-stu-id="7c14f-434">Server Side Includes</span></span>

<span data-ttu-id="7c14f-435">155</span><span class="sxs-lookup"><span data-stu-id="7c14f-435">155</span></span>

<span data-ttu-id="7c14f-436">Intégrité et diagnostics</span><span class="sxs-lookup"><span data-stu-id="7c14f-436">Health And Diagnostics</span></span>

<span data-ttu-id="7c14f-437">156</span><span class="sxs-lookup"><span data-stu-id="7c14f-437">156</span></span>

<span data-ttu-id="7c14f-438">Journalisation HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-438">HTTP Logging</span></span>

<span data-ttu-id="7c14f-439">157</span><span class="sxs-lookup"><span data-stu-id="7c14f-439">157</span></span>

<span data-ttu-id="7c14f-440">Outils de journalisation</span><span class="sxs-lookup"><span data-stu-id="7c14f-440">Logging Tools</span></span>

<span data-ttu-id="7c14f-441">158</span><span class="sxs-lookup"><span data-stu-id="7c14f-441">158</span></span>

<span data-ttu-id="7c14f-442">Observateur de demandes</span><span class="sxs-lookup"><span data-stu-id="7c14f-442">Request Monitor</span></span>

<span data-ttu-id="7c14f-443">159</span><span class="sxs-lookup"><span data-stu-id="7c14f-443">159</span></span>

<span data-ttu-id="7c14f-444">Traçage</span><span class="sxs-lookup"><span data-stu-id="7c14f-444">Tracing</span></span>

<span data-ttu-id="7c14f-445">160</span><span class="sxs-lookup"><span data-stu-id="7c14f-445">160</span></span>

<span data-ttu-id="7c14f-446">Journalisation personnalisée</span><span class="sxs-lookup"><span data-stu-id="7c14f-446">Custom Logging</span></span>

<span data-ttu-id="7c14f-447">161</span><span class="sxs-lookup"><span data-stu-id="7c14f-447">161</span></span>

<span data-ttu-id="7c14f-448">Journal ODBC</span><span class="sxs-lookup"><span data-stu-id="7c14f-448">ODBC Logging</span></span>

<span data-ttu-id="7c14f-449">162</span><span class="sxs-lookup"><span data-stu-id="7c14f-449">162</span></span>

<span data-ttu-id="7c14f-450">Sécurité</span><span class="sxs-lookup"><span data-stu-id="7c14f-450">Security</span></span>

<span data-ttu-id="7c14f-451">163</span><span class="sxs-lookup"><span data-stu-id="7c14f-451">163</span></span>

<span data-ttu-id="7c14f-452">Authentification de base</span><span class="sxs-lookup"><span data-stu-id="7c14f-452">Basic Authentication</span></span>

<span data-ttu-id="7c14f-453">164</span><span class="sxs-lookup"><span data-stu-id="7c14f-453">164</span></span>

<span data-ttu-id="7c14f-454">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-454">Windows Authentication</span></span>

<span data-ttu-id="7c14f-455">165</span><span class="sxs-lookup"><span data-stu-id="7c14f-455">165</span></span>

<span data-ttu-id="7c14f-456">Authentification Digest</span><span class="sxs-lookup"><span data-stu-id="7c14f-456">Digest Authentication</span></span>

<span data-ttu-id="7c14f-457">166</span><span class="sxs-lookup"><span data-stu-id="7c14f-457">166</span></span>

<span data-ttu-id="7c14f-458">Authentification par mappage de certificat client</span><span class="sxs-lookup"><span data-stu-id="7c14f-458">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="7c14f-459">167</span><span class="sxs-lookup"><span data-stu-id="7c14f-459">167</span></span>

<span data-ttu-id="7c14f-460">Authentification par mappage de certificat client IIS</span><span class="sxs-lookup"><span data-stu-id="7c14f-460">IIS Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="7c14f-461">168</span><span class="sxs-lookup"><span data-stu-id="7c14f-461">168</span></span>

<span data-ttu-id="7c14f-462">Autorisation URL</span><span class="sxs-lookup"><span data-stu-id="7c14f-462">URL Authorization</span></span>

<span data-ttu-id="7c14f-463">169</span><span class="sxs-lookup"><span data-stu-id="7c14f-463">169</span></span>

<span data-ttu-id="7c14f-464">Filtrage des demandes</span><span class="sxs-lookup"><span data-stu-id="7c14f-464">Request Filtering</span></span>

<span data-ttu-id="7c14f-465">170</span><span class="sxs-lookup"><span data-stu-id="7c14f-465">170</span></span>

<span data-ttu-id="7c14f-466">Restrictions IP et de domaine</span><span class="sxs-lookup"><span data-stu-id="7c14f-466">IP And Domain Restrictions</span></span>

<span data-ttu-id="7c14f-467">171</span><span class="sxs-lookup"><span data-stu-id="7c14f-467">171</span></span>

<span data-ttu-id="7c14f-468">Performances</span><span class="sxs-lookup"><span data-stu-id="7c14f-468">Performance</span></span>

<span data-ttu-id="7c14f-469">172</span><span class="sxs-lookup"><span data-stu-id="7c14f-469">172</span></span>

<span data-ttu-id="7c14f-470">Compression de contenu statique</span><span class="sxs-lookup"><span data-stu-id="7c14f-470">Static Content Compression</span></span>

<span data-ttu-id="7c14f-471">173</span><span class="sxs-lookup"><span data-stu-id="7c14f-471">173</span></span>

<span data-ttu-id="7c14f-472">compression du contenu dynamique</span><span class="sxs-lookup"><span data-stu-id="7c14f-472">Dynamic Content Compression</span></span>

<span data-ttu-id="7c14f-473">174</span><span class="sxs-lookup"><span data-stu-id="7c14f-473">174</span></span>

<span data-ttu-id="7c14f-474">Outils des gestion</span><span class="sxs-lookup"><span data-stu-id="7c14f-474">Management Tools</span></span>

<span data-ttu-id="7c14f-475">175</span><span class="sxs-lookup"><span data-stu-id="7c14f-475">175</span></span>

<span data-ttu-id="7c14f-476">Console de gestion d’IIS</span><span class="sxs-lookup"><span data-stu-id="7c14f-476">IIS Management Console</span></span>

<span data-ttu-id="7c14f-477">176</span><span class="sxs-lookup"><span data-stu-id="7c14f-477">176</span></span>

<span data-ttu-id="7c14f-478">Scripts et outils de gestion IIS</span><span class="sxs-lookup"><span data-stu-id="7c14f-478">IIS Management Scripts And Tools</span></span>

<span data-ttu-id="7c14f-479">177</span><span class="sxs-lookup"><span data-stu-id="7c14f-479">177</span></span>

<span data-ttu-id="7c14f-480">Service d'administration</span><span class="sxs-lookup"><span data-stu-id="7c14f-480">Management Service</span></span>

<span data-ttu-id="7c14f-481">178</span><span class="sxs-lookup"><span data-stu-id="7c14f-481">178</span></span>

<span data-ttu-id="7c14f-482">IIS 6 Management Compatibility</span><span class="sxs-lookup"><span data-stu-id="7c14f-482">IIS 6 Management Compatibility</span></span>

<span data-ttu-id="7c14f-483">179</span><span class="sxs-lookup"><span data-stu-id="7c14f-483">179</span></span>

<span data-ttu-id="7c14f-484">Compatibilité avec la métabase de données IIS 6</span><span class="sxs-lookup"><span data-stu-id="7c14f-484">IIS 6 Metabase Compatibility</span></span>

<span data-ttu-id="7c14f-485">180</span><span class="sxs-lookup"><span data-stu-id="7c14f-485">180</span></span>

<span data-ttu-id="7c14f-486">Compatibilité WMI d'IIS 6</span><span class="sxs-lookup"><span data-stu-id="7c14f-486">IIS 6 WMI Compatibility</span></span>

<span data-ttu-id="7c14f-487">181</span><span class="sxs-lookup"><span data-stu-id="7c14f-487">181</span></span>

<span data-ttu-id="7c14f-488">Outils de script IIS 6</span><span class="sxs-lookup"><span data-stu-id="7c14f-488">IIS 6 Scripting Tools</span></span>

<span data-ttu-id="7c14f-489">182</span><span class="sxs-lookup"><span data-stu-id="7c14f-489">182</span></span>

<span data-ttu-id="7c14f-490">Console de gestion IIS 6</span><span class="sxs-lookup"><span data-stu-id="7c14f-490">IIS 6 Management Console</span></span>

<span data-ttu-id="7c14f-491">183</span><span class="sxs-lookup"><span data-stu-id="7c14f-491">183</span></span>

<span data-ttu-id="7c14f-492">Service de publication FTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-492">FTP Publishing Service</span></span><br/>

<span data-ttu-id="7c14f-493">184</span><span class="sxs-lookup"><span data-stu-id="7c14f-493">184</span></span>

<span data-ttu-id="7c14f-494">Serveur FTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-494">FTP Server</span></span>

<span data-ttu-id="7c14f-495">185</span><span class="sxs-lookup"><span data-stu-id="7c14f-495">185</span></span>

<span data-ttu-id="7c14f-496">Console de gestion FTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-496">FTP Management Console</span></span><br/>

<span data-ttu-id="7c14f-497">314</span><span class="sxs-lookup"><span data-stu-id="7c14f-497">314</span></span>

<span data-ttu-id="7c14f-498">Publication WebDAV</span><span class="sxs-lookup"><span data-stu-id="7c14f-498">WebDAV Publishing</span></span>

<span data-ttu-id="7c14f-499">316</span><span class="sxs-lookup"><span data-stu-id="7c14f-499">316</span></span>

<span data-ttu-id="7c14f-500">Service FTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-500">FTP Service</span></span><br/>

<span data-ttu-id="7c14f-501">317</span><span class="sxs-lookup"><span data-stu-id="7c14f-501">317</span></span>

<span data-ttu-id="7c14f-502">Extensibilité FTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-502">FTP Extensibility</span></span><br/>

<span data-ttu-id="7c14f-503">336</span><span class="sxs-lookup"><span data-stu-id="7c14f-503">336</span></span>

<span data-ttu-id="7c14f-504">IIS Hostable Web Core</span><span class="sxs-lookup"><span data-stu-id="7c14f-504">IIS Hostable Web Core</span></span><br/>

<span data-ttu-id="7c14f-505">413</span><span class="sxs-lookup"><span data-stu-id="7c14f-505">413</span></span>

[<span data-ttu-id="7c14f-506">ASP.NET 4.5</span><span class="sxs-lookup"><span data-stu-id="7c14f-506">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="7c14f-507">414</span><span class="sxs-lookup"><span data-stu-id="7c14f-507">414</span></span>

[<span data-ttu-id="7c14f-508">Extensibilité .NET 4.5</span><span class="sxs-lookup"><span data-stu-id="7c14f-508">.NET Extensibility 4.5</span></span>](/windows)

<span data-ttu-id="7c14f-509">445</span><span class="sxs-lookup"><span data-stu-id="7c14f-509">445</span></span>

[<span data-ttu-id="7c14f-510">appialization</span><span class="sxs-lookup"><span data-stu-id="7c14f-510">appialization</span></span>](/windows)

<span data-ttu-id="7c14f-511">446</span><span class="sxs-lookup"><span data-stu-id="7c14f-511">446</span></span>

[<span data-ttu-id="7c14f-512">Prise en charge centralisée des certificats SSL</span><span class="sxs-lookup"><span data-stu-id="7c14f-512">Centralized SSL Certificate Support</span></span>](/windows)

<span data-ttu-id="7c14f-513">447</span><span class="sxs-lookup"><span data-stu-id="7c14f-513">447</span></span>

[<span data-ttu-id="7c14f-514">Protocole WebSocket</span><span class="sxs-lookup"><span data-stu-id="7c14f-514">WebSocket Protocol</span></span>](/windows)

<span data-ttu-id="7c14f-515">Message Queuing-fonctionnalités (49)</span><span class="sxs-lookup"><span data-stu-id="7c14f-515">Message Queuing - Features (49)</span></span>

<span data-ttu-id="7c14f-516">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-516">Value</span></span>

<span data-ttu-id="7c14f-517">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-517">Name</span></span>

<span data-ttu-id="7c14f-518">190</span><span class="sxs-lookup"><span data-stu-id="7c14f-518">190</span></span>

<span data-ttu-id="7c14f-519">Services Message Queuing</span><span class="sxs-lookup"><span data-stu-id="7c14f-519">Message Queuing Services</span></span>

<span data-ttu-id="7c14f-520">191</span><span class="sxs-lookup"><span data-stu-id="7c14f-520">191</span></span>

<span data-ttu-id="7c14f-521">Serveur Message Queuing</span><span class="sxs-lookup"><span data-stu-id="7c14f-521">Message Queuing Server</span></span>

<span data-ttu-id="7c14f-522">192</span><span class="sxs-lookup"><span data-stu-id="7c14f-522">192</span></span>

<span data-ttu-id="7c14f-523">Intégration du service d’annuaire</span><span class="sxs-lookup"><span data-stu-id="7c14f-523">Directory Service Integration</span></span>

<span data-ttu-id="7c14f-524">193</span><span class="sxs-lookup"><span data-stu-id="7c14f-524">193</span></span>

<span data-ttu-id="7c14f-525">Déclencheurs Message Queuing</span><span class="sxs-lookup"><span data-stu-id="7c14f-525">Message Queuing Triggers</span></span>

<span data-ttu-id="7c14f-526">194</span><span class="sxs-lookup"><span data-stu-id="7c14f-526">194</span></span>

<span data-ttu-id="7c14f-527">Prise en charge HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-527">HTTP Support</span></span>

<span data-ttu-id="7c14f-528">195</span><span class="sxs-lookup"><span data-stu-id="7c14f-528">195</span></span>

<span data-ttu-id="7c14f-529">Service de routage</span><span class="sxs-lookup"><span data-stu-id="7c14f-529">Routing Service</span></span>

<span data-ttu-id="7c14f-530">196</span><span class="sxs-lookup"><span data-stu-id="7c14f-530">196</span></span>

[<span data-ttu-id="7c14f-531">Prise en charge des clients Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7c14f-531">Windows 2000 Client Support</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-532">197</span><span class="sxs-lookup"><span data-stu-id="7c14f-532">197</span></span>

<span data-ttu-id="7c14f-533">Message Queuing DCOM Proxy</span><span class="sxs-lookup"><span data-stu-id="7c14f-533">Message Queuing DCOM Proxy</span></span>

<span data-ttu-id="7c14f-534">228</span><span class="sxs-lookup"><span data-stu-id="7c14f-534">228</span></span>

<span data-ttu-id="7c14f-535">Prise en charge de la multidiffusion</span><span class="sxs-lookup"><span data-stu-id="7c14f-535">Multicasting Support</span></span>

<span data-ttu-id="7c14f-536">Services de certificats Active Directory-Services de rôle (16)</span><span class="sxs-lookup"><span data-stu-id="7c14f-536">Active Directory Certificate Services - Role Services (16)</span></span>

<span data-ttu-id="7c14f-537">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-537">Value</span></span>

<span data-ttu-id="7c14f-538">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-538">Name</span></span>

<span data-ttu-id="7c14f-539">200</span><span class="sxs-lookup"><span data-stu-id="7c14f-539">200</span></span>

<span data-ttu-id="7c14f-540">Autorité de certification</span><span class="sxs-lookup"><span data-stu-id="7c14f-540">Certification Authority</span></span>

<span data-ttu-id="7c14f-541">201</span><span class="sxs-lookup"><span data-stu-id="7c14f-541">201</span></span>

<span data-ttu-id="7c14f-542">Inscription de l’autorité de certification via le Web</span><span class="sxs-lookup"><span data-stu-id="7c14f-542">Certification Authority Web Enrollment</span></span>

<span data-ttu-id="7c14f-543">202</span><span class="sxs-lookup"><span data-stu-id="7c14f-543">202</span></span>

<span data-ttu-id="7c14f-544">Répondeur en ligne</span><span class="sxs-lookup"><span data-stu-id="7c14f-544">Online Responder</span></span>

<span data-ttu-id="7c14f-545">204</span><span class="sxs-lookup"><span data-stu-id="7c14f-545">204</span></span>

<span data-ttu-id="7c14f-546">Service d’inscription de périphériques réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-546">Network Device Enrollment Service</span></span>

<span data-ttu-id="7c14f-547">318</span><span class="sxs-lookup"><span data-stu-id="7c14f-547">318</span></span>

[<span data-ttu-id="7c14f-548">Service Web Inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="7c14f-548">Certificate Enrollment Web Service</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-549">319</span><span class="sxs-lookup"><span data-stu-id="7c14f-549">319</span></span>

[<span data-ttu-id="7c14f-550">service Web Stratégie d'inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="7c14f-550">Certificate Enrollment Policy Web Service</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-551">Services de stratégie et d’accès réseau-services de rôle (14)</span><span class="sxs-lookup"><span data-stu-id="7c14f-551">Network Policy and Access Services - Role Services (14)</span></span>

<span data-ttu-id="7c14f-552">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-552">Value</span></span>

<span data-ttu-id="7c14f-553">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-553">Name</span></span>

<span data-ttu-id="7c14f-554">205</span><span class="sxs-lookup"><span data-stu-id="7c14f-554">205</span></span>

[<span data-ttu-id="7c14f-555">Serveur de stratégie réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-555">Network Policy Server</span></span>](/windows)

<span data-ttu-id="7c14f-556">206</span><span class="sxs-lookup"><span data-stu-id="7c14f-556">206</span></span>

[<span data-ttu-id="7c14f-557">VPN</span><span class="sxs-lookup"><span data-stu-id="7c14f-557">VPN</span></span>](#vpn)

<span data-ttu-id="7c14f-558">207</span><span class="sxs-lookup"><span data-stu-id="7c14f-558">207</span></span>

[<span data-ttu-id="7c14f-559">Services d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-559">Remote Access Services</span></span>](/windows)

<span data-ttu-id="7c14f-560">208</span><span class="sxs-lookup"><span data-stu-id="7c14f-560">208</span></span>

[<span data-ttu-id="7c14f-561">Routage</span><span class="sxs-lookup"><span data-stu-id="7c14f-561">Routing</span></span>](#routing)

<span data-ttu-id="7c14f-562">210</span><span class="sxs-lookup"><span data-stu-id="7c14f-562">210</span></span>

[<span data-ttu-id="7c14f-563">Autorité HRA (Health Registration Authority)</span><span class="sxs-lookup"><span data-stu-id="7c14f-563">Health Registration Authority</span></span>](/windows)

<span data-ttu-id="7c14f-564">250</span><span class="sxs-lookup"><span data-stu-id="7c14f-564">250</span></span>

[<span data-ttu-id="7c14f-565">Protocole d’autorisation des informations d’identification de l’hôte</span><span class="sxs-lookup"><span data-stu-id="7c14f-565">Host Credential Authorization Protocol</span></span>](/windows)

<span data-ttu-id="7c14f-566">Services UDDI-services de rôle (11)</span><span class="sxs-lookup"><span data-stu-id="7c14f-566">UDDI Services - Role Services (11)</span></span>

<span data-ttu-id="7c14f-567">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-567">Value</span></span>

<span data-ttu-id="7c14f-568">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-568">Name</span></span>

<span data-ttu-id="7c14f-569">215</span><span class="sxs-lookup"><span data-stu-id="7c14f-569">215</span></span>

[<span data-ttu-id="7c14f-570">Application Web des services UDDI</span><span class="sxs-lookup"><span data-stu-id="7c14f-570">UDDI Services Web Application</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-571">216</span><span class="sxs-lookup"><span data-stu-id="7c14f-571">216</span></span>

[<span data-ttu-id="7c14f-572">Base de données des services UDDI</span><span class="sxs-lookup"><span data-stu-id="7c14f-572">UDDI Services Database</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-573">Service d’activation des processus Windows-Services de rôle (41)</span><span class="sxs-lookup"><span data-stu-id="7c14f-573">Windows Process Activation Service - Role Services (41)</span></span>

<span data-ttu-id="7c14f-574">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-574">Value</span></span>

<span data-ttu-id="7c14f-575">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-575">Name</span></span>

<span data-ttu-id="7c14f-576">217</span><span class="sxs-lookup"><span data-stu-id="7c14f-576">217</span></span>

<span data-ttu-id="7c14f-577">API de configuration</span><span class="sxs-lookup"><span data-stu-id="7c14f-577">Configuration API</span></span>

<span data-ttu-id="7c14f-578">218</span><span class="sxs-lookup"><span data-stu-id="7c14f-578">218</span></span>

<span data-ttu-id="7c14f-579">Environnement .NET</span><span class="sxs-lookup"><span data-stu-id="7c14f-579">.NET Environment</span></span>

<span data-ttu-id="7c14f-580">219</span><span class="sxs-lookup"><span data-stu-id="7c14f-580">219</span></span>

<span data-ttu-id="7c14f-581">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="7c14f-581">Process Model</span></span>

<span data-ttu-id="7c14f-582">.NET Framework 3.5.1-fonctionnalités (36)</span><span class="sxs-lookup"><span data-stu-id="7c14f-582">.NET Framework 3.5.1 - Features (36)</span></span>

<span data-ttu-id="7c14f-583">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-583">Value</span></span>

<span data-ttu-id="7c14f-584">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-584">Name</span></span>

<span data-ttu-id="7c14f-585">220</span><span class="sxs-lookup"><span data-stu-id="7c14f-585">220</span></span>

<span data-ttu-id="7c14f-586">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="7c14f-586">.NET Framework 3.5.1</span></span><br/> [<span data-ttu-id="7c14f-587">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-587">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-588">221</span><span class="sxs-lookup"><span data-stu-id="7c14f-588">221</span></span>

<span data-ttu-id="7c14f-589">Activation de Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="7c14f-589">WCF Activation</span></span>

<span data-ttu-id="7c14f-590">222</span><span class="sxs-lookup"><span data-stu-id="7c14f-590">222</span></span>

<span data-ttu-id="7c14f-591">Activation HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-591">HTTP Activation</span></span>

<span data-ttu-id="7c14f-592">223</span><span class="sxs-lookup"><span data-stu-id="7c14f-592">223</span></span>

<span data-ttu-id="7c14f-593">Activation non-HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-593">Non-HTTP Activation</span></span>

<span data-ttu-id="7c14f-594">227</span><span class="sxs-lookup"><span data-stu-id="7c14f-594">227</span></span>

<span data-ttu-id="7c14f-595">Visionneuse XPS</span><span class="sxs-lookup"><span data-stu-id="7c14f-595">XPS Viewer</span></span><br/>

<span data-ttu-id="7c14f-596">Services SNMP-fonctionnalités (59)</span><span class="sxs-lookup"><span data-stu-id="7c14f-596">SNMP Services - Features (59)</span></span>

<span data-ttu-id="7c14f-597">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-597">Value</span></span>

<span data-ttu-id="7c14f-598">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-598">Name</span></span>

<span data-ttu-id="7c14f-599">224</span><span class="sxs-lookup"><span data-stu-id="7c14f-599">224</span></span>

[<span data-ttu-id="7c14f-600">Service SNMP</span><span class="sxs-lookup"><span data-stu-id="7c14f-600">SNMP Service</span></span>](/windows)

<span data-ttu-id="7c14f-601">225</span><span class="sxs-lookup"><span data-stu-id="7c14f-601">225</span></span>

[<span data-ttu-id="7c14f-602">Fournisseur WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="7c14f-602">SNMP WMI Provider</span></span>](/windows)

<span data-ttu-id="7c14f-603">Services d’application-services de rôle</span><span class="sxs-lookup"><span data-stu-id="7c14f-603">Application Services - Role Services</span></span>

<span data-ttu-id="7c14f-604">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-604">Value</span></span>

<span data-ttu-id="7c14f-605">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-605">Name</span></span>

<span data-ttu-id="7c14f-606">230</span><span class="sxs-lookup"><span data-stu-id="7c14f-606">230</span></span>

[<span data-ttu-id="7c14f-607">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="7c14f-607">.NET Framework 3.5.1</span></span>](/windows)<br/> [<span data-ttu-id="7c14f-608">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-608">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-609">231</span><span class="sxs-lookup"><span data-stu-id="7c14f-609">231</span></span>

[<span data-ttu-id="7c14f-610">Prise en charge de Serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-610">Web Server (IIS) Support</span></span>](/windows)

<span data-ttu-id="7c14f-611">232</span><span class="sxs-lookup"><span data-stu-id="7c14f-611">232</span></span>

[<span data-ttu-id="7c14f-612">Accès réseau COM+</span><span class="sxs-lookup"><span data-stu-id="7c14f-612">COM+ Network Access</span></span>](/windows)

<span data-ttu-id="7c14f-613">233</span><span class="sxs-lookup"><span data-stu-id="7c14f-613">233</span></span>

[<span data-ttu-id="7c14f-614">Partage de port TCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-614">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="7c14f-615">234</span><span class="sxs-lookup"><span data-stu-id="7c14f-615">234</span></span>

[<span data-ttu-id="7c14f-616">Prise en charge du service d’activation des processus Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-616">Windows Process Activation Service Support</span></span>](/windows)

<span data-ttu-id="7c14f-617">235</span><span class="sxs-lookup"><span data-stu-id="7c14f-617">235</span></span>

[<span data-ttu-id="7c14f-618">Activation HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-618">HTTP Activation</span></span>](/windows)

<span data-ttu-id="7c14f-619">236</span><span class="sxs-lookup"><span data-stu-id="7c14f-619">236</span></span>

[<span data-ttu-id="7c14f-620">Activation Message Queuing</span><span class="sxs-lookup"><span data-stu-id="7c14f-620">Message Queuing Activation</span></span>](/windows)

<span data-ttu-id="7c14f-621">237</span><span class="sxs-lookup"><span data-stu-id="7c14f-621">237</span></span>

[<span data-ttu-id="7c14f-622">Activation de TCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-622">TCP Activation</span></span>](/windows)

<span data-ttu-id="7c14f-623">238</span><span class="sxs-lookup"><span data-stu-id="7c14f-623">238</span></span>

[<span data-ttu-id="7c14f-624">Activation des canaux nommés</span><span class="sxs-lookup"><span data-stu-id="7c14f-624">Named Pipes Activation</span></span>](/windows)

<span data-ttu-id="7c14f-625">239</span><span class="sxs-lookup"><span data-stu-id="7c14f-625">239</span></span>

[<span data-ttu-id="7c14f-626">Transactions distribuées</span><span class="sxs-lookup"><span data-stu-id="7c14f-626">Distributed Transactions</span></span>](/windows)

<span data-ttu-id="7c14f-627">240</span><span class="sxs-lookup"><span data-stu-id="7c14f-627">240</span></span>

[<span data-ttu-id="7c14f-628">Transactions distantes entrantes</span><span class="sxs-lookup"><span data-stu-id="7c14f-628">Incoming Remote Transactions</span></span>](/windows)

<span data-ttu-id="7c14f-629">241</span><span class="sxs-lookup"><span data-stu-id="7c14f-629">241</span></span>

[<span data-ttu-id="7c14f-630">Transactions distantes sortantes</span><span class="sxs-lookup"><span data-stu-id="7c14f-630">Outgoing Remote Transactions</span></span>](/windows)

<span data-ttu-id="7c14f-631">242</span><span class="sxs-lookup"><span data-stu-id="7c14f-631">242</span></span>

[<span data-ttu-id="7c14f-632">Transactions WS-Automatic</span><span class="sxs-lookup"><span data-stu-id="7c14f-632">WS-Automatic Transactions</span></span>](/windows)

<span data-ttu-id="7c14f-633">353</span><span class="sxs-lookup"><span data-stu-id="7c14f-633">353</span></span>

[<span data-ttu-id="7c14f-634">Extensions du serveur d’applications pour .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="7c14f-634">Application Server Extensions for .NET 4.0</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-635">Services de déploiement Windows-rôle (19)</span><span class="sxs-lookup"><span data-stu-id="7c14f-635">Windows Deployment Services - Role (19)</span></span>

<span data-ttu-id="7c14f-636">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-636">Value</span></span>

<span data-ttu-id="7c14f-637">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-637">Name</span></span>

<span data-ttu-id="7c14f-638">251</span><span class="sxs-lookup"><span data-stu-id="7c14f-638">251</span></span>

<span data-ttu-id="7c14f-639">Serveur de déploiement</span><span class="sxs-lookup"><span data-stu-id="7c14f-639">Deployment Server</span></span>

<span data-ttu-id="7c14f-640">252</span><span class="sxs-lookup"><span data-stu-id="7c14f-640">252</span></span>

<span data-ttu-id="7c14f-641">Serveur de transport</span><span class="sxs-lookup"><span data-stu-id="7c14f-641">Transport Server</span></span>

<span data-ttu-id="7c14f-642">Services de rôle services AD RMS (Active Directory Rights Management Services) (17)</span><span class="sxs-lookup"><span data-stu-id="7c14f-642">Active Directory Rights Management Services - Role Services (17)</span></span>

<span data-ttu-id="7c14f-643">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-643">Value</span></span>

<span data-ttu-id="7c14f-644">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-644">Name</span></span>

<span data-ttu-id="7c14f-645">253</span><span class="sxs-lookup"><span data-stu-id="7c14f-645">253</span></span>

<span data-ttu-id="7c14f-646">Serveur AD RMS (Active Directory Rights Management Server)</span><span class="sxs-lookup"><span data-stu-id="7c14f-646">Active Directory Rights Management Server</span></span>

<span data-ttu-id="7c14f-647">254</span><span class="sxs-lookup"><span data-stu-id="7c14f-647">254</span></span>

<span data-ttu-id="7c14f-648">Prise en charge de la fédération des identités</span><span class="sxs-lookup"><span data-stu-id="7c14f-648">Identity Federation Support</span></span>

<span data-ttu-id="7c14f-649">Outils d’administration de serveur distant (67)</span><span class="sxs-lookup"><span data-stu-id="7c14f-649">Remote Server Administration Tools (67)</span></span>

<span data-ttu-id="7c14f-650">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-650">Value</span></span>

<span data-ttu-id="7c14f-651">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-651">Name</span></span>

<span data-ttu-id="7c14f-652">256</span><span class="sxs-lookup"><span data-stu-id="7c14f-652">256</span></span>

[<span data-ttu-id="7c14f-653">Outils d’administration de rôles</span><span class="sxs-lookup"><span data-stu-id="7c14f-653">Role Administration Tools</span></span>](/windows)

<span data-ttu-id="7c14f-654">257</span><span class="sxs-lookup"><span data-stu-id="7c14f-654">257</span></span>

[<span data-ttu-id="7c14f-655">Outils AD DS</span><span class="sxs-lookup"><span data-stu-id="7c14f-655">AD DS Tools</span></span>](/windows)<br/> [<span data-ttu-id="7c14f-656">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-656">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-657">258</span><span class="sxs-lookup"><span data-stu-id="7c14f-657">258</span></span>

[<span data-ttu-id="7c14f-658">Outils de Snap-Ins et de Command-Line AD LDS</span><span class="sxs-lookup"><span data-stu-id="7c14f-658">AD LDS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="7c14f-659">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-659">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-660">259</span><span class="sxs-lookup"><span data-stu-id="7c14f-660">259</span></span>

<span data-ttu-id="7c14f-661">Outils de services de certificats Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c14f-661">Active Directory Certificate Services Tools</span></span>

<span data-ttu-id="7c14f-662">260</span><span class="sxs-lookup"><span data-stu-id="7c14f-662">260</span></span>

[<span data-ttu-id="7c14f-663">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-663">Network Policy and Access Services</span></span>](/windows)

<span data-ttu-id="7c14f-664">261</span><span class="sxs-lookup"><span data-stu-id="7c14f-664">261</span></span>

<span data-ttu-id="7c14f-665">Outils de Services d’impression et de numérisation de document</span><span class="sxs-lookup"><span data-stu-id="7c14f-665">Print and Document Services Tools</span></span><br/> [<span data-ttu-id="7c14f-666">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-666">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-667">262</span><span class="sxs-lookup"><span data-stu-id="7c14f-667">262</span></span>

[<span data-ttu-id="7c14f-668">Services AD RMS (Active Directory Rights Management Services)</span><span class="sxs-lookup"><span data-stu-id="7c14f-668">Active Directory Rights Management Services</span></span>](/windows)

<span data-ttu-id="7c14f-669">263</span><span class="sxs-lookup"><span data-stu-id="7c14f-669">263</span></span>

[<span data-ttu-id="7c14f-670">Outils des services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-670">Remote Desktop Services Tools</span></span>](/windows)<br/> [<span data-ttu-id="7c14f-671">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-671">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-672">264</span><span class="sxs-lookup"><span data-stu-id="7c14f-672">264</span></span>

<span data-ttu-id="7c14f-673">Outils des services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-673">Windows Deployment Services Tools</span></span>

<span data-ttu-id="7c14f-674">265</span><span class="sxs-lookup"><span data-stu-id="7c14f-674">265</span></span>

[<span data-ttu-id="7c14f-675">Outils d’administration de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="7c14f-675">Feature Administration Tools</span></span>](/windows)

<span data-ttu-id="7c14f-676">266</span><span class="sxs-lookup"><span data-stu-id="7c14f-676">266</span></span>

<span data-ttu-id="7c14f-677">BitLocker Drive Encryption Tools</span><span class="sxs-lookup"><span data-stu-id="7c14f-677">BitLocker Drive Encryption Tools</span></span>

<span data-ttu-id="7c14f-678">267</span><span class="sxs-lookup"><span data-stu-id="7c14f-678">267</span></span>

<span data-ttu-id="7c14f-679">Outils d’extensions du serveur BITS</span><span class="sxs-lookup"><span data-stu-id="7c14f-679">BITS Server Extensions Tools</span></span>

<span data-ttu-id="7c14f-680">268</span><span class="sxs-lookup"><span data-stu-id="7c14f-680">268</span></span>

[<span data-ttu-id="7c14f-681">Outils de clustering de basculement</span><span class="sxs-lookup"><span data-stu-id="7c14f-681">Failover Clustering Tools</span></span>](/windows)

<span data-ttu-id="7c14f-682">269</span><span class="sxs-lookup"><span data-stu-id="7c14f-682">269</span></span>

<span data-ttu-id="7c14f-683">Outils d'équilibrage de la charge réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-683">Network Load Balancing Tools</span></span>

<span data-ttu-id="7c14f-684">270</span><span class="sxs-lookup"><span data-stu-id="7c14f-684">270</span></span>

<span data-ttu-id="7c14f-685">Outils du serveur SMTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-685">SMTP Server Tools</span></span>

<span data-ttu-id="7c14f-686">273</span><span class="sxs-lookup"><span data-stu-id="7c14f-686">273</span></span>

[<span data-ttu-id="7c14f-687">Outils du serveur DNS</span><span class="sxs-lookup"><span data-stu-id="7c14f-687">DNS Server Tools</span></span>](/windows)

<span data-ttu-id="7c14f-688">277</span><span class="sxs-lookup"><span data-stu-id="7c14f-688">277</span></span>

<span data-ttu-id="7c14f-689">Outils de services de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-689">File Services Tools</span></span>

<span data-ttu-id="7c14f-690">278</span><span class="sxs-lookup"><span data-stu-id="7c14f-690">278</span></span>

<span data-ttu-id="7c14f-691">Outils de système de fichiers DFS</span><span class="sxs-lookup"><span data-stu-id="7c14f-691">Distributed File System Tools</span></span>

<span data-ttu-id="7c14f-692">279</span><span class="sxs-lookup"><span data-stu-id="7c14f-692">279</span></span>

<span data-ttu-id="7c14f-693">Outils de gestion des ressources pour serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-693">File Server Resource Manager Tools</span></span>

<span data-ttu-id="7c14f-694">280</span><span class="sxs-lookup"><span data-stu-id="7c14f-694">280</span></span>

[<span data-ttu-id="7c14f-695">Services pour les outils du système de fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-695">Services For Network File System Tools</span></span>](/windows)

<span data-ttu-id="7c14f-696">281</span><span class="sxs-lookup"><span data-stu-id="7c14f-696">281</span></span>

<span data-ttu-id="7c14f-697">Outils de serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-697">Web Server (IIS) Tools</span></span>

<span data-ttu-id="7c14f-698">284</span><span class="sxs-lookup"><span data-stu-id="7c14f-698">284</span></span>

[<span data-ttu-id="7c14f-699">Outils de l’hôte de session Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-699">Remote Desktop Session Host Tools</span></span>](/windows)<br/> [<span data-ttu-id="7c14f-700">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-700">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-701">285</span><span class="sxs-lookup"><span data-stu-id="7c14f-701">285</span></span>

<span data-ttu-id="7c14f-702">Outils de passerelle Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-702">Remote Desktop Gateway Tools</span></span><br/> [<span data-ttu-id="7c14f-703">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-703">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-704">286</span><span class="sxs-lookup"><span data-stu-id="7c14f-704">286</span></span>

<span data-ttu-id="7c14f-705">Outils de licence Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-705">Remote Desktop Licensing Tools</span></span><br/> [<span data-ttu-id="7c14f-706">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-706">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-707">288</span><span class="sxs-lookup"><span data-stu-id="7c14f-707">288</span></span>

<span data-ttu-id="7c14f-708">Outils du serveur de télécopie</span><span class="sxs-lookup"><span data-stu-id="7c14f-708">Fax Server Tools</span></span>

<span data-ttu-id="7c14f-709">290</span><span class="sxs-lookup"><span data-stu-id="7c14f-709">290</span></span>

<span data-ttu-id="7c14f-710">Outils du serveur WINS</span><span class="sxs-lookup"><span data-stu-id="7c14f-710">WINS Server Tools</span></span>

<span data-ttu-id="7c14f-711">291</span><span class="sxs-lookup"><span data-stu-id="7c14f-711">291</span></span>

[<span data-ttu-id="7c14f-712">Outils des services UDDI</span><span class="sxs-lookup"><span data-stu-id="7c14f-712">UDDI Services Tools</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-713">292</span><span class="sxs-lookup"><span data-stu-id="7c14f-713">292</span></span>

<span data-ttu-id="7c14f-714">Outils de l’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="7c14f-714">Certification Authority Tools</span></span>

<span data-ttu-id="7c14f-715">293</span><span class="sxs-lookup"><span data-stu-id="7c14f-715">293</span></span>

<span data-ttu-id="7c14f-716">Outils de répondeur en ligne</span><span class="sxs-lookup"><span data-stu-id="7c14f-716">Online Responder Tools</span></span>

<span data-ttu-id="7c14f-717">297</span><span class="sxs-lookup"><span data-stu-id="7c14f-717">297</span></span>

[<span data-ttu-id="7c14f-718">Outils de Serveur pour NIS</span><span class="sxs-lookup"><span data-stu-id="7c14f-718">Server for NIS Tools</span></span>](/windows)

<span data-ttu-id="7c14f-719">299</span><span class="sxs-lookup"><span data-stu-id="7c14f-719">299</span></span>

[<span data-ttu-id="7c14f-720">Composants logiciels enfichables et outils en ligne de commande AD DS</span><span class="sxs-lookup"><span data-stu-id="7c14f-720">AD DS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="7c14f-721">changement de nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-721">name change</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-722">300</span><span class="sxs-lookup"><span data-stu-id="7c14f-722">300</span></span>

[<span data-ttu-id="7c14f-723">Centre d’administration Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c14f-723">Active Directory Administrative Center</span></span>](/windows)

<span data-ttu-id="7c14f-724">301</span><span class="sxs-lookup"><span data-stu-id="7c14f-724">301</span></span>

<span data-ttu-id="7c14f-725">Outils Hyper-V</span><span class="sxs-lookup"><span data-stu-id="7c14f-725">Hyper-V Tools</span></span>

<span data-ttu-id="7c14f-726">323</span><span class="sxs-lookup"><span data-stu-id="7c14f-726">323</span></span>

[<span data-ttu-id="7c14f-727">Visionneuse de mot de passe de récupération BitLocker</span><span class="sxs-lookup"><span data-stu-id="7c14f-727">BitLocker Recovery Password Viewer</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-728">326</span><span class="sxs-lookup"><span data-stu-id="7c14f-728">326</span></span>

[<span data-ttu-id="7c14f-729">BitLocker Drive Encryption Administration Utilities</span><span class="sxs-lookup"><span data-stu-id="7c14f-729">BitLocker Drive Encryption Administration Utilities</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-730">329</span><span class="sxs-lookup"><span data-stu-id="7c14f-730">329</span></span>

[<span data-ttu-id="7c14f-731">Outils AD DS et AD LDS</span><span class="sxs-lookup"><span data-stu-id="7c14f-731">AD DS and AD LDS Tools</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-732">330</span><span class="sxs-lookup"><span data-stu-id="7c14f-732">330</span></span>

<span data-ttu-id="7c14f-733">Centre d'administration Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c14f-733">Active Directory Administrative Center</span></span><br/>

<span data-ttu-id="7c14f-734">331</span><span class="sxs-lookup"><span data-stu-id="7c14f-734">331</span></span>

[<span data-ttu-id="7c14f-735">Module Active Directory pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-735">Active Directory module for Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-736">337</span><span class="sxs-lookup"><span data-stu-id="7c14f-736">337</span></span>

[<span data-ttu-id="7c14f-737">Outils du Service Broker Connexion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-737">Remote Desktop Connection Broker Tools</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-738">410</span><span class="sxs-lookup"><span data-stu-id="7c14f-738">410</span></span>

[<span data-ttu-id="7c14f-739">Client gestion des adresses IP (IPAM)</span><span class="sxs-lookup"><span data-stu-id="7c14f-739">IP Address Management (IPAM) Client</span></span>](/windows)

<span data-ttu-id="7c14f-740">450</span><span class="sxs-lookup"><span data-stu-id="7c14f-740">450</span></span>

[<span data-ttu-id="7c14f-741">Module Hyper-V pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-741">Hyper-V Module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="7c14f-742">462</span><span class="sxs-lookup"><span data-stu-id="7c14f-742">462</span></span>

[<span data-ttu-id="7c14f-743">Outils de services AD RMS (Active Directory Rights Management Services)</span><span class="sxs-lookup"><span data-stu-id="7c14f-743">Active Directory Rights Management Services Tools</span></span>](/windows)

<span data-ttu-id="7c14f-744">465</span><span class="sxs-lookup"><span data-stu-id="7c14f-744">465</span></span>

[<span data-ttu-id="7c14f-745">Outil Gestion du partage et du stockage</span><span class="sxs-lookup"><span data-stu-id="7c14f-745">Share and Storage Management Tool</span></span>](/windows)

<span data-ttu-id="7c14f-746">471</span><span class="sxs-lookup"><span data-stu-id="7c14f-746">471</span></span>

[<span data-ttu-id="7c14f-747">Outils de gestion de l’accès à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-747">Remote Access Management Tools</span></span>](/windows)

<span data-ttu-id="7c14f-748">472</span><span class="sxs-lookup"><span data-stu-id="7c14f-748">472</span></span>

[<span data-ttu-id="7c14f-749">Module d’accès à distance pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-749">Remote Access module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="7c14f-750">473</span><span class="sxs-lookup"><span data-stu-id="7c14f-750">473</span></span>

[<span data-ttu-id="7c14f-751">GUI d’accès à distance et outils de Command-Line</span><span class="sxs-lookup"><span data-stu-id="7c14f-751">Remote Access GUI and Command-Line Tools</span></span>](/windows)

<span data-ttu-id="7c14f-752">474</span><span class="sxs-lookup"><span data-stu-id="7c14f-752">474</span></span>

[<span data-ttu-id="7c14f-753">Outils Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-753">Windows Server Update Services Tools</span></span>](/windows)

<span data-ttu-id="7c14f-754">476</span><span class="sxs-lookup"><span data-stu-id="7c14f-754">476</span></span>

[<span data-ttu-id="7c14f-755">Outils de diagnostic du gestionnaire de licences Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-755">Remote Desktop Licensing Diagnoser Tools</span></span>](/windows)

<span data-ttu-id="7c14f-756">479</span><span class="sxs-lookup"><span data-stu-id="7c14f-756">479</span></span>

[<span data-ttu-id="7c14f-757">Outils SNMP</span><span class="sxs-lookup"><span data-stu-id="7c14f-757">SNMP Tools</span></span>](/windows)

<span data-ttu-id="7c14f-758">480</span><span class="sxs-lookup"><span data-stu-id="7c14f-758">480</span></span>

[<span data-ttu-id="7c14f-759">Outils d’activation en volume</span><span class="sxs-lookup"><span data-stu-id="7c14f-759">Volume Activation Tools</span></span>](/windows)

<span data-ttu-id="7c14f-760">Sauvegarde Windows Server-fonctionnalités (39)</span><span class="sxs-lookup"><span data-stu-id="7c14f-760">Windows Server Backup - Features (39)</span></span>

<span data-ttu-id="7c14f-761">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-761">Value</span></span>

<span data-ttu-id="7c14f-762">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-762">Name</span></span>

<span data-ttu-id="7c14f-763">296</span><span class="sxs-lookup"><span data-stu-id="7c14f-763">296</span></span>

[<span data-ttu-id="7c14f-764">Sauvegarde Windows Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-764">Windows Server Backup</span></span>](/windows)

<span data-ttu-id="7c14f-765">297</span><span class="sxs-lookup"><span data-stu-id="7c14f-765">297</span></span>

[<span data-ttu-id="7c14f-766">Outils en ligne de commande</span><span class="sxs-lookup"><span data-stu-id="7c14f-766">Command Line Tools</span></span>](/windows)

<span data-ttu-id="7c14f-767">Services de prise en charge de l’écriture manuscrite-fonctionnalités (310)</span><span class="sxs-lookup"><span data-stu-id="7c14f-767">Ink and Handwriting Services - Features (310)</span></span>

<span data-ttu-id="7c14f-768">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-768">Value</span></span>

<span data-ttu-id="7c14f-769">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-769">Name</span></span>

<span data-ttu-id="7c14f-770">311</span><span class="sxs-lookup"><span data-stu-id="7c14f-770">311</span></span>

[<span data-ttu-id="7c14f-771">Prise en charge de l’encre</span><span class="sxs-lookup"><span data-stu-id="7c14f-771">Ink Support</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-772">312</span><span class="sxs-lookup"><span data-stu-id="7c14f-772">312</span></span>

[<span data-ttu-id="7c14f-773">Reconnaissance de l’écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="7c14f-773">Handwriting Recognition</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-774">Service de transfert intelligent en arrière-plan (BITS)-fonctionnalités (335)</span><span class="sxs-lookup"><span data-stu-id="7c14f-774">Background Intelligent Transfer Service (BITS) - Features (335)</span></span>

<span data-ttu-id="7c14f-775">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-775">Value</span></span>

<span data-ttu-id="7c14f-776">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-776">Name</span></span>

<span data-ttu-id="7c14f-777">54</span><span class="sxs-lookup"><span data-stu-id="7c14f-777">54</span></span>

<span data-ttu-id="7c14f-778">Extension de serveur IIS</span><span class="sxs-lookup"><span data-stu-id="7c14f-778">IIS Server Extension</span></span>

<span data-ttu-id="7c14f-779">332</span><span class="sxs-lookup"><span data-stu-id="7c14f-779">332</span></span>

[<span data-ttu-id="7c14f-780">Compact Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-780">Compact Server</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-781">Prise en charge WOW64-fonctionnalités (340)</span><span class="sxs-lookup"><span data-stu-id="7c14f-781">Wow64 Support - Features (340)</span></span>

<span data-ttu-id="7c14f-782">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-782">Value</span></span>

<span data-ttu-id="7c14f-783">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-783">Name</span></span>

<span data-ttu-id="7c14f-784">341</span><span class="sxs-lookup"><span data-stu-id="7c14f-784">341</span></span>

[<span data-ttu-id="7c14f-785">WoW64</span><span class="sxs-lookup"><span data-stu-id="7c14f-785">WoW64</span></span>](#wow64)<br/>

<span data-ttu-id="7c14f-786">342</span><span class="sxs-lookup"><span data-stu-id="7c14f-786">342</span></span>

[<span data-ttu-id="7c14f-787">WoW64 pour .NET Framework 2,0 et Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-787">WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-788">343</span><span class="sxs-lookup"><span data-stu-id="7c14f-788">343</span></span>

[<span data-ttu-id="7c14f-789">WoW64 pour .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="7c14f-789">WoW64 for .NET Framework 2.0</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-790">344</span><span class="sxs-lookup"><span data-stu-id="7c14f-790">344</span></span>

[<span data-ttu-id="7c14f-791">WoW64 pour PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-791">WoW64 for PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-792">345</span><span class="sxs-lookup"><span data-stu-id="7c14f-792">345</span></span>

[<span data-ttu-id="7c14f-793">WoW64 pour .NET Framework 3,0 et 3,5</span><span class="sxs-lookup"><span data-stu-id="7c14f-793">WoW64 for .NET Framework 3.0 and 3.5</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-794">346</span><span class="sxs-lookup"><span data-stu-id="7c14f-794">346</span></span>

[<span data-ttu-id="7c14f-795">WoW64 pour les services d’impression</span><span class="sxs-lookup"><span data-stu-id="7c14f-795">WoW64 for Print Services</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-796">347</span><span class="sxs-lookup"><span data-stu-id="7c14f-796">347</span></span>

[<span data-ttu-id="7c14f-797">WoW64 pour le clustering de basculement</span><span class="sxs-lookup"><span data-stu-id="7c14f-797">WoW64 for Failover Clustering</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-798">348</span><span class="sxs-lookup"><span data-stu-id="7c14f-798">348</span></span>

[<span data-ttu-id="7c14f-799">WoW64 pour l’éditeur de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="7c14f-799">WoW64 for Input Method Editor</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-800">349</span><span class="sxs-lookup"><span data-stu-id="7c14f-800">349</span></span>

[<span data-ttu-id="7c14f-801">WoW64 pour le sous-système pour les applications UNIX</span><span class="sxs-lookup"><span data-stu-id="7c14f-801">WoW64 for Subsystem for UNIX-based Applications</span></span>](/windows)<br/>

<span data-ttu-id="7c14f-802">Interfaces utilisateur et services de rôle d’infrastructure (447)</span><span class="sxs-lookup"><span data-stu-id="7c14f-802">User Interfaces and Infrastructure - Role Services (447)</span></span>

<span data-ttu-id="7c14f-803">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-803">Value</span></span>

<span data-ttu-id="7c14f-804">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-804">Name</span></span>

<span data-ttu-id="7c14f-805">35</span><span class="sxs-lookup"><span data-stu-id="7c14f-805">35</span></span>

[<span data-ttu-id="7c14f-806">Expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="7c14f-806">Desktop Experience</span></span>](/windows)

<span data-ttu-id="7c14f-807">99</span><span class="sxs-lookup"><span data-stu-id="7c14f-807">99</span></span>

[<span data-ttu-id="7c14f-808">Interpréteur de commandes graphique de serveur</span><span class="sxs-lookup"><span data-stu-id="7c14f-808">Server Graphical Shell</span></span>](/windows)

<span data-ttu-id="7c14f-809">Windows Server Update Services-fonctionnalités (404)</span><span class="sxs-lookup"><span data-stu-id="7c14f-809">Window Server Update Services - Features (404)</span></span>

<span data-ttu-id="7c14f-810">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-810">Value</span></span>

<span data-ttu-id="7c14f-811">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-811">Name</span></span>

<span data-ttu-id="7c14f-812">405</span><span class="sxs-lookup"><span data-stu-id="7c14f-812">405</span></span>

[<span data-ttu-id="7c14f-813">API et applets de commande PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-813">API and PowerShell cmdlets</span></span>](/windows)

<span data-ttu-id="7c14f-814">406</span><span class="sxs-lookup"><span data-stu-id="7c14f-814">406</span></span>

[<span data-ttu-id="7c14f-815">Connectivité SQL Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-815">SQL Server Connectivity</span></span>](/windows)

<span data-ttu-id="7c14f-816">407</span><span class="sxs-lookup"><span data-stu-id="7c14f-816">407</span></span>

[<span data-ttu-id="7c14f-817">Services WSUS</span><span class="sxs-lookup"><span data-stu-id="7c14f-817">WSUS Services</span></span>](/windows)

<span data-ttu-id="7c14f-818">408</span><span class="sxs-lookup"><span data-stu-id="7c14f-818">408</span></span>

[<span data-ttu-id="7c14f-819">Console de gestion de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="7c14f-819">User Interface Management Console</span></span>](/windows)

<span data-ttu-id="7c14f-820">449</span><span class="sxs-lookup"><span data-stu-id="7c14f-820">449</span></span>

[<span data-ttu-id="7c14f-821">Connectivité WID</span><span class="sxs-lookup"><span data-stu-id="7c14f-821">WID Connectivity</span></span>](/windows)

<span data-ttu-id="7c14f-822">Windows PowerShell-fonctionnalités (417)</span><span class="sxs-lookup"><span data-stu-id="7c14f-822">Windows PowerShell - Features (417)</span></span>

<span data-ttu-id="7c14f-823">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-823">Value</span></span>

<span data-ttu-id="7c14f-824">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-824">Name</span></span>

<span data-ttu-id="7c14f-825">411</span><span class="sxs-lookup"><span data-stu-id="7c14f-825">411</span></span>

[<span data-ttu-id="7c14f-826">Moteur Windows PowerShell 2,0</span><span class="sxs-lookup"><span data-stu-id="7c14f-826">Windows PowerShell 2.0 Engine</span></span>](/windows)

<span data-ttu-id="7c14f-827">412</span><span class="sxs-lookup"><span data-stu-id="7c14f-827">412</span></span>

[<span data-ttu-id="7c14f-828">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="7c14f-828">Windows PowerShell 3.0</span></span>](/windows)

<span data-ttu-id="7c14f-829">448</span><span class="sxs-lookup"><span data-stu-id="7c14f-829">448</span></span>

[<span data-ttu-id="7c14f-830">Accès Web Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-830">Windows PowerShell Web Access</span></span>](/windows)

<span data-ttu-id="7c14f-831">1 000</span><span class="sxs-lookup"><span data-stu-id="7c14f-831">1000</span></span>

[<span data-ttu-id="7c14f-832">Service de configuration d’état souhaité Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-832">Windows PowerShell Desired State Configuration Service</span></span>](/windows)

<span data-ttu-id="7c14f-833">.NET Framework 4,5-fonctionnalités (418)</span><span class="sxs-lookup"><span data-stu-id="7c14f-833">.NET Framework 4.5 - Features (418)</span></span>

<span data-ttu-id="7c14f-834">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-834">Value</span></span>

<span data-ttu-id="7c14f-835">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-835">Name</span></span>

<span data-ttu-id="7c14f-836">419</span><span class="sxs-lookup"><span data-stu-id="7c14f-836">419</span></span>

[<span data-ttu-id="7c14f-837">.NET Framework 4,5 étendu</span><span class="sxs-lookup"><span data-stu-id="7c14f-837">.NET Framework 4.5 Extended</span></span>](/windows)

<span data-ttu-id="7c14f-838">420</span><span class="sxs-lookup"><span data-stu-id="7c14f-838">420</span></span>

[<span data-ttu-id="7c14f-839">Services WCF</span><span class="sxs-lookup"><span data-stu-id="7c14f-839">WCF Services</span></span>](/windows)

<span data-ttu-id="7c14f-840">421</span><span class="sxs-lookup"><span data-stu-id="7c14f-840">421</span></span>

[<span data-ttu-id="7c14f-841">Activation HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-841">HTTP Activation</span></span>](/windows)

<span data-ttu-id="7c14f-842">422</span><span class="sxs-lookup"><span data-stu-id="7c14f-842">422</span></span>

[<span data-ttu-id="7c14f-843">Activation d’Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="7c14f-843">Message Queuing (MSMQ) Activation</span></span>](/windows)

<span data-ttu-id="7c14f-844">423</span><span class="sxs-lookup"><span data-stu-id="7c14f-844">423</span></span>

[<span data-ttu-id="7c14f-845">Activation de canaux nommés</span><span class="sxs-lookup"><span data-stu-id="7c14f-845">Named Pipe Activation</span></span>](/windows)

<span data-ttu-id="7c14f-846">424</span><span class="sxs-lookup"><span data-stu-id="7c14f-846">424</span></span>

[<span data-ttu-id="7c14f-847">Activation de TCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-847">TCP Activation</span></span>](/windows)

<span data-ttu-id="7c14f-848">425</span><span class="sxs-lookup"><span data-stu-id="7c14f-848">425</span></span>

[<span data-ttu-id="7c14f-849">Partage de port TCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-849">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="7c14f-850">429</span><span class="sxs-lookup"><span data-stu-id="7c14f-850">429</span></span>

[<span data-ttu-id="7c14f-851">ASP.NET 4.5</span><span class="sxs-lookup"><span data-stu-id="7c14f-851">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="7c14f-852">Accès à distance-rôle (468)</span><span class="sxs-lookup"><span data-stu-id="7c14f-852">Remote Access - Role (468)</span></span>

<span data-ttu-id="7c14f-853">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-853">Value</span></span>

<span data-ttu-id="7c14f-854">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-854">Name</span></span>

<span data-ttu-id="7c14f-855">469</span><span class="sxs-lookup"><span data-stu-id="7c14f-855">469</span></span>

[<span data-ttu-id="7c14f-856">DirectAccess et VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-856">DirectAccess and VPN (RAS)</span></span>](/windows)

<span data-ttu-id="7c14f-857">470</span><span class="sxs-lookup"><span data-stu-id="7c14f-857">470</span></span>

[<span data-ttu-id="7c14f-858">Routage</span><span class="sxs-lookup"><span data-stu-id="7c14f-858">Routing</span></span>](#routing)

<span data-ttu-id="7c14f-859">Services de fichiers et de stockage-rôle (481)</span><span class="sxs-lookup"><span data-stu-id="7c14f-859">File and Storage Services - Role (481)</span></span>

<span data-ttu-id="7c14f-860">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-860">Value</span></span>

<span data-ttu-id="7c14f-861">Nom</span><span class="sxs-lookup"><span data-stu-id="7c14f-861">Name</span></span>

<span data-ttu-id="7c14f-862">482</span><span class="sxs-lookup"><span data-stu-id="7c14f-862">482</span></span>

[<span data-ttu-id="7c14f-863">Services de stockage</span><span class="sxs-lookup"><span data-stu-id="7c14f-863">Storage Services</span></span>](/windows)

<span data-ttu-id="7c14f-864">484</span><span class="sxs-lookup"><span data-stu-id="7c14f-864">484</span></span>

[<span data-ttu-id="7c14f-865">Outils de gestion du cluster de basculement</span><span class="sxs-lookup"><span data-stu-id="7c14f-865">Failover Cluster Management Tools</span></span>](/windows)



 

</dd> <dt>

<span data-ttu-id="7c14f-866">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7c14f-866">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c14f-867">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7c14f-867">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c14f-868">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c14f-868">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7c14f-869">Nom complet de la fonctionnalité serveur, par exemple « serveur de fichiers », « serveur d’impression » ou « expérience utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="7c14f-869">Display name of the server feature, such as "File Server", "Print Server", or "Desktop Experience".</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-870">**ID**</span><span class="sxs-lookup"><span data-stu-id="7c14f-870">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c14f-871">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c14f-871">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c14f-872">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c14f-872">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7c14f-873">Numéro d’identification de la fonctionnalité de serveur parent.</span><span class="sxs-lookup"><span data-stu-id="7c14f-873">ID number of the parent server feature.</span></span> <span data-ttu-id="7c14f-874">Cette propriété est 0 si la fonctionnalité représentée par l’instance actuelle de la classe n’a pas de fonctionnalité parente.</span><span class="sxs-lookup"><span data-stu-id="7c14f-874">This property is 0 if the feature represented by the current instance of the class does not have a parent feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c14f-875">Notes</span><span class="sxs-lookup"><span data-stu-id="7c14f-875">Remarks</span></span>

<span data-ttu-id="7c14f-876">Consultez la [Présentation technique de Windows Server 2008 gestionnaire de serveur](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) pour en savoir plus sur les fonctionnalités du serveur.</span><span class="sxs-lookup"><span data-stu-id="7c14f-876">Read the [Windows Server 2008 Server Manager Technical Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) to learn about server features.</span></span>

<span data-ttu-id="7c14f-877">Les entreprises qui n’utilisent pas de logiciel de gestion qui signale les fonctionnalités serveur, telles que System Center Operations Manager avec les packs d’administration installés, peuvent obtenir ces informations en interrogeant la classe **Win32 \_ ServerFeature** .</span><span class="sxs-lookup"><span data-stu-id="7c14f-877">Enterprises that do not use management software that reports server features, such as System Center Operations Manager with management packs installed, can get that information by querying the **Win32\_ServerFeature** class.</span></span>

<span data-ttu-id="7c14f-878">Vous pouvez utiliser les fonctionnalités de communication à distance de WMI ou WinRM pour récupérer les informations sur les fonctionnalités du serveur à partir des serveurs distants.</span><span class="sxs-lookup"><span data-stu-id="7c14f-878">You can use the remoting features of WMI or WinRM to get server feature information from remote servers.</span></span> <span data-ttu-id="7c14f-879">Pour plus d’informations sur les connexions WMI DCOM à distance, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="7c14f-879">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="7c14f-880">Pour plus d’informations sur WinRM, consultez Gestion à distance de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c14f-880">For more information about WinRM, see Windows Remote Management.</span></span>

<span data-ttu-id="7c14f-881">Windows Server 2012 : **Win32 \_ ServerFeature** est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="7c14f-881">Windows Server 2012: **Win32\_ServerFeature** has been deprecated.</span></span> <span data-ttu-id="7c14f-882">Pour accéder aux informations sur les fonctionnalités de Windows Server par programme, vous pouvez utiliser les [applets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10))de commande gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="7c14f-882">To access windows server feature information programmatically, you can use the [Server Manager Cmdlets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span></span>

### <a name="windows-server-2012-r2"></a><span data-ttu-id="7c14f-883">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7c14f-883">Windows Server 2012 R2</span></span>

<dl> <dt>

<span data-ttu-id="7c14f-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Serveur d’applications</span><span class="sxs-lookup"><span data-stu-id="7c14f-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Application Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-885">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-885">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Media Services de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="7c14f-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Streaming Media Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-887">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-887">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>services de fédération Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory Federation Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-889">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-889">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>Serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-891">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-891">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>Serveur DNS</span><span class="sxs-lookup"><span data-stu-id="7c14f-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-893">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-893">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Remote Desktop Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-895">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-895">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-897">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-897">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Clustering de basculement</span><span class="sxs-lookup"><span data-stu-id="7c14f-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-899">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-899">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Équilibrage de la charge réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network Load Balancing</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-901">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-901">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>Fonctionnalités de .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="7c14f-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 Features</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-903">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-903">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Gestionnaire des ressources système Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-905">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-905">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Fonctionnalités de Sauvegarde Windows Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Server Backup Features</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-907">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-907">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Assistance à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Remote Assistance</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-909">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-909">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Client Telnet</span><span class="sxs-lookup"><span data-stu-id="7c14f-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet Client</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-911">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-911">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Serveur Telnet</span><span class="sxs-lookup"><span data-stu-id="7c14f-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-913">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-913">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Sous-système pour les applications UNIX</span><span class="sxs-lookup"><span data-stu-id="7c14f-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem For Unix-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-915">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-915">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Base de données interne Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows Internal Database</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-917">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-917">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Gestionnaire de stockage pour réseau San</span><span class="sxs-lookup"><span data-stu-id="7c14f-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Storage Manager For SANs</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-919">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-919">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Serveur de noms de stockage Internet</span><span class="sxs-lookup"><span data-stu-id="7c14f-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet Storage Name Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-921">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-921">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>MPIO (Multipath I/O)</span><span class="sxs-lookup"><span data-stu-id="7c14f-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-923">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-923">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Services SNMP</span><span class="sxs-lookup"><span data-stu-id="7c14f-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-925">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-925">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services pour le système de fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-927">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-927">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Protocole PNRP (Peer Name Resolution Protocol)</span><span class="sxs-lookup"><span data-stu-id="7c14f-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution Protocol</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-929">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-929">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="7c14f-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Remote Server Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-931">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-931">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Expérience audio-vidéo haute qualité Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Quality Windows Audio Video Experience</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-933">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-933">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Gestion des stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7c14f-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Group Policy Management</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-935">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-935">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Service d’indexation</span><span class="sxs-lookup"><span data-stu-id="7c14f-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-937">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-937">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>Gestionnaire des ressources de serveur de fichiers (FSRM)</span><span class="sxs-lookup"><span data-stu-id="7c14f-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>File Server Resource Manager (FSRM)</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-939">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-939">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Outils de migration de Windows Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Server Migration Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-941">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-941">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span><span class="sxs-lookup"><span data-stu-id="7c14f-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-943">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-943">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console de gestion DirectAccess</span><span class="sxs-lookup"><span data-stu-id="7c14f-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-945">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-945">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Service de transfert intelligent en arrière-plan (BITS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-947">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-947">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Prise en charge WoW64</span><span class="sxs-lookup"><span data-stu-id="7c14f-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-949">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-949">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Services de mise à jour Windows Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Window Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-951">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-951">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>Serveur de gestion des adresses IP (IPAM)</span><span class="sxs-lookup"><span data-stu-id="7c14f-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP Address Management (IPAM) Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-953">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-953">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-955">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-955">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="7c14f-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4.5</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-957">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-957">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Search Service Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-959">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-959">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client pour NFS</span><span class="sxs-lookup"><span data-stu-id="7c14f-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client for NFS</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-961">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-961">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Déverrouillage réseau BitLocker</span><span class="sxs-lookup"><span data-stu-id="7c14f-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker Network Unlock</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-963">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-963">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Extension IIS Management OData</span><span class="sxs-lookup"><span data-stu-id="7c14f-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Management OData IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-965">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-965">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>Services avancés .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="7c14f-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-967">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-967">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>Fonctionnalités de .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="7c14f-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 Features</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-969">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-969">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfaces utilisateur et infrastructure</span><span class="sxs-lookup"><span data-stu-id="7c14f-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-971">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-971">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Outils et infrastructure de gestion graphique</span><span class="sxs-lookup"><span data-stu-id="7c14f-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Graphical Management Tools and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-973">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-973">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Services de fichiers et de stockage</span><span class="sxs-lookup"><span data-stu-id="7c14f-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>File and Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-975">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-975">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Expérience Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="7c14f-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials Experience</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-977">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-977">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Lecture directe</span><span class="sxs-lookup"><span data-stu-id="7c14f-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direct Play</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-979">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-979">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>système de fichiers DFS</span><span class="sxs-lookup"><span data-stu-id="7c14f-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Distributed File System</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-981">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-981">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>Gestionnaire des ressources du serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>File Server Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-983">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-983">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services pour le système de fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-985">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-985">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Stockage d’instance simple</span><span class="sxs-lookup"><span data-stu-id="7c14f-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Single Instance Storage</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-987">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-987">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Search Service Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-989">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-989">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Service d’indexation</span><span class="sxs-lookup"><span data-stu-id="7c14f-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-991">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-991">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>Fournisseur de stockage cible iSCSI (fournisseurs de matériel VDS et VSS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-993">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-993">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Dossiers de travail</span><span class="sxs-lookup"><span data-stu-id="7c14f-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-995">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-995">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Contrôleur de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c14f-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory Domain Controller</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-997">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-997">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Gestion des identités pour UNIX</span><span class="sxs-lookup"><span data-stu-id="7c14f-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Identity Management For Unix</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-999">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-999">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Serveur pour Network Information Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server For Network Information Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1001">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1001">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Synchronisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="7c14f-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Password Synchronization</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1003">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1003">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Outils d’administration</span><span class="sxs-lookup"><span data-stu-id="7c14f-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1005">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1005">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Serveur Windows Media</span><span class="sxs-lookup"><span data-stu-id="7c14f-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1007">N'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7c14f-1007">No longer supported.</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Administration basée sur le Web</span><span class="sxs-lookup"><span data-stu-id="7c14f-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Web-based Administration</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1009">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1009">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Agent de journalisation</span><span class="sxs-lookup"><span data-stu-id="7c14f-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Logging Agent</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1011">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1011">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>service FS (Federation Service)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Federation Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1013">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1013">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Stratégie de service FS (Federation Service)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Federation Service Policy</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1015">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1015">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>Agents Web AD FS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web Agents</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1017">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1017">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Agent basé sur les jetons Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Token-based Agent</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1019">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1019">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Licences Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Remote Desktop Licensing</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1021">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1021">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>NPS (Network Policy Server)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Network Policy Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1023">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1023">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span><span class="sxs-lookup"><span data-stu-id="7c14f-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1025">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1025">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Services d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Remote Access Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1027">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1027">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Achemine</span><span class="sxs-lookup"><span data-stu-id="7c14f-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1029">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1029">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Autorité d’inscription d’intégrité</span><span class="sxs-lookup"><span data-stu-id="7c14f-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Health Registration Authority</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1031">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1031">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Protocole d’autorisation des informations d’identification de l’hôte</span><span class="sxs-lookup"><span data-stu-id="7c14f-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Host Credential Authorization Protocol</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1033">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1033">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="7c14f-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1035">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1035">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visionneuse XPS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1037">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1037">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Service SNMP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1039">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1039">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>Fournisseur WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI Provider</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1041">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1041">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="7c14f-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1043">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1043">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Prise en charge du serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Web Server (IIS) Support</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1045">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1045">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Accès réseau COM+</span><span class="sxs-lookup"><span data-stu-id="7c14f-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1047">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1047">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Partage de port TCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1049">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1049">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Prise en charge du service d’activation des processus Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Process Activation Service Support</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1051">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1051">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Activation HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1053">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1053">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Activation Message Queuing</span><span class="sxs-lookup"><span data-stu-id="7c14f-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Message Queuing Activation</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1055">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1055">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Activation TCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1057">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1057">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Activation des canaux nommés</span><span class="sxs-lookup"><span data-stu-id="7c14f-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Named Pipes Activation</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1059">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1059">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Transactions distribuées</span><span class="sxs-lookup"><span data-stu-id="7c14f-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Distributed Transactions</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1061">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1061">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Transactions distantes entrantes</span><span class="sxs-lookup"><span data-stu-id="7c14f-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Incoming Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1063">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1063">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Transactions distantes sortantes</span><span class="sxs-lookup"><span data-stu-id="7c14f-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Outgoing Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1065">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1065">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>Transactions WS-Automatic</span><span class="sxs-lookup"><span data-stu-id="7c14f-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-Automatic Transactions</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1067">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1067">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensions du serveur d’applications pour .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="7c14f-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1069">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1069">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Outils d’administration de rôles</span><span class="sxs-lookup"><span data-stu-id="7c14f-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Role Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1071">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1071">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>Outils de AD DS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1073">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1073">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Outils de Snap-Ins et de Command-Line AD LDS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1075">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1075">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Services de stratégie et d’accès réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Network Policy and Access Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1077">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1077">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>services AD RMS (Active Directory Rights Management Services)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1079">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1079">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Outils de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Remote Desktop Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1081">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1081">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Outils d’administration de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="7c14f-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Feature Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1083">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1083">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Outils de clustering de basculement</span><span class="sxs-lookup"><span data-stu-id="7c14f-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Failover Clustering Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1085">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1085">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Outils du serveur DNS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS Server Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1087">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1087">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services pour les outils du système de fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services For Network File System Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1089">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1089">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Outils de serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Web Server (IIS) Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1091">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1091">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Outils de Serveur pour NIS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server for NIS Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1093">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1093">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Outils de Snap-Ins et de Command-Line AD DS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1095">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1095">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Outils de AD DS et de AD LDS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1097">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1097">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Outils du Service Broker Connexion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1099">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1099">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>Client gestion des adresses IP (IPAM)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP Address Management (IPAM) Client</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1101">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1101">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Module Hyper-V pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Hyper-V Module for Windows PowerShell</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7c14f-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Outil services AD RMS (Active Directory Rights Management Services)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Tool</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1104">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1104">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Outil Gestion du partage et du stockage</span><span class="sxs-lookup"><span data-stu-id="7c14f-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Share and Storage Management Tool</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1106">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1106">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Outils de gestion de l’accès à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Remote Access Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1108">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1108">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Module d’accès à distance pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Remote Access module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1110">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1110">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>GUI d’accès à distance et outils de Command-Line</span><span class="sxs-lookup"><span data-stu-id="7c14f-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Remote Access GUI and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1112">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1112">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Outils de Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="7c14f-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1114">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1114">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Outils de diagnostic du gestionnaire de licences Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Remote Desktop Licensing Diagnoser Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1116">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1116">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Outils SNMP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1118">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1118">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Outils d’activation en volume</span><span class="sxs-lookup"><span data-stu-id="7c14f-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Volume Activation Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1120">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1120">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Sauvegarde Windows Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1122">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1122">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Outils en ligne de commande</span><span class="sxs-lookup"><span data-stu-id="7c14f-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Command Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1124">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1124">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Prise en charge de l’encre</span><span class="sxs-lookup"><span data-stu-id="7c14f-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Ink Support</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1126">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1126">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Reconnaissance de l’écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="7c14f-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Handwriting Recognition</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1128">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1128">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Serveur compact</span><span class="sxs-lookup"><span data-stu-id="7c14f-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1130">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1130">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="7c14f-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1132">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1132">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 pour .NET Framework 2,0 et PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 for .NET Framework 2.0 and PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1134">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1134">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 pour .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="7c14f-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1136">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1136">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 pour PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1138">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1138">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 pour .NET Framework 3,0 et 3,5</span><span class="sxs-lookup"><span data-stu-id="7c14f-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1140">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1140">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 pour les services d’impression</span><span class="sxs-lookup"><span data-stu-id="7c14f-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1142">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1142">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 pour le clustering de basculement</span><span class="sxs-lookup"><span data-stu-id="7c14f-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1144">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1144">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 pour l’éditeur de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="7c14f-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1146">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1146">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 pour le sous-système pour les applications UNIX</span><span class="sxs-lookup"><span data-stu-id="7c14f-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1148">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1148">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="7c14f-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Desktop Experience</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1150">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1150">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Interpréteur de commandes graphique de serveur</span><span class="sxs-lookup"><span data-stu-id="7c14f-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Server Graphical Shell</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1152">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1152">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API et applets de commande PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API and PowerShell cmdlets</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1154">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1154">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>Connectivité SQL Server</span><span class="sxs-lookup"><span data-stu-id="7c14f-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1156">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1156">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Services WSUS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1158">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1158">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Console de gestion de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="7c14f-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>User Interface Management Console</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1160">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1160">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Connectivité WID</span><span class="sxs-lookup"><span data-stu-id="7c14f-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1162">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1162">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Moteur Windows PowerShell 2,0</span><span class="sxs-lookup"><span data-stu-id="7c14f-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0 Engine</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1164">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1164">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="7c14f-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1166">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1166">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Accès web Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web Access</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1168">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1168">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Service de configuration d’état souhaité Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1170">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1170">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4,5 étendu</span><span class="sxs-lookup"><span data-stu-id="7c14f-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Extended</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1172">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1172">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Services WCF</span><span class="sxs-lookup"><span data-stu-id="7c14f-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1174">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1174">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Activation HTTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1176">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1176">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Activation d’Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Message Queuing (MSMQ) Activation</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7c14f-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Activation du canal nommé</span><span class="sxs-lookup"><span data-stu-id="7c14f-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Named Pipe Activation</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1179">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1179">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Activation TCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1181">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1181">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Partage de port TCP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1183">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1183">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="7c14f-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1185">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1185">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Extensibilité .NET 4,5</span><span class="sxs-lookup"><span data-stu-id="7c14f-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET Extensibility 4.5</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1187">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1187">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess et VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess and VPN (RAS)</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1189">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1189">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Achemine</span><span class="sxs-lookup"><span data-stu-id="7c14f-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1191">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1191">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Services de stockage</span><span class="sxs-lookup"><span data-stu-id="7c14f-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1193">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1193">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Outils de gestion du cluster de basculement</span><span class="sxs-lookup"><span data-stu-id="7c14f-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Failover Cluster Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1195">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1195">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Outils de services AD RMS (Active Directory Rights Management Services)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1197">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1197">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Initialisation d’application</span><span class="sxs-lookup"><span data-stu-id="7c14f-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Application Initialization</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1199">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1199">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Prise en charge centralisée des certificats SSL</span><span class="sxs-lookup"><span data-stu-id="7c14f-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Centralized SSL Certificate Support</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1201">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1201">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Agent prenant en charge les revendications</span><span class="sxs-lookup"><span data-stu-id="7c14f-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Claims-aware Agent</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1203">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1203">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Outils de l’hôte de session Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Remote Desktop Session Host Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1205">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1205">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Protocole WebSocket</span><span class="sxs-lookup"><span data-stu-id="7c14f-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket Protocol</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1207">n’est plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1207">no longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Accès réseau COM+</span><span class="sxs-lookup"><span data-stu-id="7c14f-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1209">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1209">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Modification du nom des services de fichiers et iSCSI</span><span class="sxs-lookup"><span data-stu-id="7c14f-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>File and iSCSI Services name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1211">Modification des services de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-1211">Changed to File Services</span></span>

</dd> </dl>

### <a name="windows-server-2012"></a><span data-ttu-id="7c14f-1212">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c14f-1212">Windows Server 2012</span></span>

<dl> <dt>

<span data-ttu-id="7c14f-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfaces utilisateur et infrastructure</span><span class="sxs-lookup"><span data-stu-id="7c14f-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1214">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1214">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Serveur pour NFS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server for NFS</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1216">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1216">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Service agent VSS du serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>File Server VSS Agent Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1218">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1218">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>Serveur cible iSCSI</span><span class="sxs-lookup"><span data-stu-id="7c14f-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI Target Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1220">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1220">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Déduplication des données</span><span class="sxs-lookup"><span data-stu-id="7c14f-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Data Deduplication</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1222">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1222">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Dossiers de travail</span><span class="sxs-lookup"><span data-stu-id="7c14f-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1224">Supprimé</span><span class="sxs-lookup"><span data-stu-id="7c14f-1224">Removed</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Services principaux</span><span class="sxs-lookup"><span data-stu-id="7c14f-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Core Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1226">Ajouté pour cette version uniquement.</span><span class="sxs-lookup"><span data-stu-id="7c14f-1226">Added for this version only.</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Graphiques virtuels Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Remote Desktop Virtual Graphics</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1228">Ajouté pour cette version uniquement</span><span class="sxs-lookup"><span data-stu-id="7c14f-1228">Added for this version only</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Accès à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Remote Access</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1230">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1230">Added</span></span>

</dd> </dl>

### <a name="windows-server-2008-r2"></a><span data-ttu-id="7c14f-1231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c14f-1231">Windows Server 2008 R2</span></span>

<dl> <dt>

<span data-ttu-id="7c14f-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Services UDDI</span><span class="sxs-lookup"><span data-stu-id="7c14f-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1233">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1233">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Gestionnaire des ressources système Windows</span><span class="sxs-lookup"><span data-stu-id="7c14f-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1235">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1235">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Gestionnaire de stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7c14f-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Removable Storage Manager</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1237">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1237">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1239">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1239">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Services de prise en charge de l'écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="7c14f-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Ink and Handwriting Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1241">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1241">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Extension WinRM IIS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1243">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1243">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console de gestion DirectAccess</span><span class="sxs-lookup"><span data-stu-id="7c14f-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1245">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1245">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Service de transfert intelligent en arrière-plan (BITS)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1247">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1247">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visionneuse XPS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1249">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1249">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="7c14f-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1251">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1251">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Prise en charge WoW64</span><span class="sxs-lookup"><span data-stu-id="7c14f-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1253">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1253">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Environnement d’écriture de scripts intégré de Windows PowerShell (ISE)</span><span class="sxs-lookup"><span data-stu-id="7c14f-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1255">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1255">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Service de réplication de fichiers</span><span class="sxs-lookup"><span data-stu-id="7c14f-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>File Replication Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1257">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1257">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache pour fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="7c14f-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache for Network Files</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1259">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1259">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Dossiers de travail</span><span class="sxs-lookup"><span data-stu-id="7c14f-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1261">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1261">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Serveur de numérisation distribuée</span><span class="sxs-lookup"><span data-stu-id="7c14f-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Distributed Scan Server</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1263">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1263">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Service de publication FTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP Publishing Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1265">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1265">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Console de gestion FTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP Management Console</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1267">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1267">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Service FTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1269">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1269">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Extensibilité FTP</span><span class="sxs-lookup"><span data-stu-id="7c14f-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP Extensibility</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1271">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1271">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Noyau Web hébergé par IIS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS Hostable Web Core</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7c14f-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Prise en charge des clients Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7c14f-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 Client Support</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1274">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1274">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>service Web Inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="7c14f-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Certificate Enrollment Web Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1276">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1276">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>service Web Stratégie d'inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="7c14f-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Certificate Enrollment Policy Web Service</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1278">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1278">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Application Web des services UDDI</span><span class="sxs-lookup"><span data-stu-id="7c14f-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI Services Web Application</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1280">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1280">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>Base de données des services UDDI</span><span class="sxs-lookup"><span data-stu-id="7c14f-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI Services Database</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1282">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1282">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensions du serveur d’applications pour .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="7c14f-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1284">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1284">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Outils des services UDDI</span><span class="sxs-lookup"><span data-stu-id="7c14f-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1286">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1286">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>Utilitaires d’administration de Chiffrement de lecteur BitLocker</span><span class="sxs-lookup"><span data-stu-id="7c14f-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker Drive Encryption Administration Utilities</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1288">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1288">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Outils de AD DS et de AD LDS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1290">Plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1290">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Outils de AD DS et de AD LDS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1292">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1292">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Centre d'administration Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c14f-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory Administrative Center</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1294">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1294">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Module Active Directory pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Active Directory module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1296">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1296">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Outils du Service Broker Connexion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1298">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1298">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="7c14f-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1300">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1300">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 pour .NET Framework 2,0 et Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1302">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1302">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 pour .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="7c14f-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1304">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1304">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 pour PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c14f-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1306">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1306">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 pour .NET Framework 3,0 et 3,5</span><span class="sxs-lookup"><span data-stu-id="7c14f-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1308">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1308">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 pour les services d’impression</span><span class="sxs-lookup"><span data-stu-id="7c14f-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1310">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1310">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 pour le clustering de basculement</span><span class="sxs-lookup"><span data-stu-id="7c14f-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1312">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1312">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 pour l’éditeur de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="7c14f-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1314">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1314">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 pour le sous-système pour les applications UNIX</span><span class="sxs-lookup"><span data-stu-id="7c14f-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1316">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1316">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Visionneuse de mot de passe de récupération BitLocker</span><span class="sxs-lookup"><span data-stu-id="7c14f-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker Recovery Password Viewer</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1318">Ajout</span><span class="sxs-lookup"><span data-stu-id="7c14f-1318">Added</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Modification du nom de Services d’impression et de numérisation de document</span><span class="sxs-lookup"><span data-stu-id="7c14f-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Print and Document Services name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1320">Services d’impression nommés pour cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1320">named Print Services for this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Modification du nom de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Remote Desktop Services name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1322">Services Terminal Server nommés dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1322">named Terminal Services in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>Modification du nom des fonctionnalités .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="7c14f-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 Features name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1324">Fonctionnalités nommées .NET Framework 3,0 dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1324">Named .NET Framework 3.0 Features in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Modification du nom d’hôte de session Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Remote Desktop Session Host name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1326">Terminal Server nommé dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1326">Named Terminal Server in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Modification du nom du gestionnaire de Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Remote Desktop Licensing name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1328">Licences TS nommées dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1328">Named TS Licensing in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Modification du nom de la passerelle Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Remote Desktop Gateway name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1330">Passerelle TS nommée dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1330">Named TS Gateway in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Modification du nom de l’Connexion Bureau à distance Broker</span><span class="sxs-lookup"><span data-stu-id="7c14f-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Remote Desktop Connection Broker name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1332">Session Broker TS nommée dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1332">Named TS Session Broker in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Modification du nom de la Bureau à distance Accès web</span><span class="sxs-lookup"><span data-stu-id="7c14f-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Remote Desktop Web Access name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1334">Accès web TS nommé dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1334">Named TS Web Access in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>Modification du nom de .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="7c14f-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1336">(220) fonctionnalités .net FX 3,0 nommées dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1336">(220) Named Net FX 3.0 Features in this release</span></span>

<span data-ttu-id="7c14f-1337">(230) nommé Core de serveur d’applications dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1337">(230) Named Application Server Core in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de AD DS</span><span class="sxs-lookup"><span data-stu-id="7c14f-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1339">Outils nommés Active Directory Domain Services dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1339">Named Active Directory Domain Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de AD LDS Snap-Ins et Command-Line</span><span class="sxs-lookup"><span data-stu-id="7c14f-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1341">Outils nommés services AD LDS (Active Directory Lightweight Directory Services) dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1341">Named Active Directory Lightweight Directory Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de Services d’impression et de numérisation de document</span><span class="sxs-lookup"><span data-stu-id="7c14f-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Print and Document Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1343">Outils des services d’impression nommés dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1343">Named Print Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Remote Desktop Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1345">Outils des services Terminal Server dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1345">Named Terminal Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de l’hôte de session Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Remote Desktop Session Host Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1347">Outils nommés Terminal Server dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1347">Named Terminal Server Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de passerelle Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Remote Desktop Gateway Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1349">Outils de passerelle TS nommés dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1349">Named TS Gateway Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de licence Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7c14f-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Remote Desktop Licensing Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1351">Outils de gestion de licences TS nommés dans cette version</span><span class="sxs-lookup"><span data-stu-id="7c14f-1351">Named TS Licensing Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="7c14f-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de AD DS Snap-Ins et Command-Line</span><span class="sxs-lookup"><span data-stu-id="7c14f-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="7c14f-1353">Outils du contrôleur de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c14f-1353">Active Directory Domain Controller Tools</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7c14f-1354">Exemples</span><span class="sxs-lookup"><span data-stu-id="7c14f-1354">Examples</span></span>

<span data-ttu-id="7c14f-1355">Le script suivant affiche les noms de toutes les fonctionnalités du serveur sur l’ordinateur nommé « FABRIKAM ».</span><span class="sxs-lookup"><span data-stu-id="7c14f-1355">The following script displays the names of all the server features on the computer named "FABRIKAM".</span></span> <span data-ttu-id="7c14f-1356">Notez que l’ordinateur cible doit exécuter Windows Server 2008 ou un système d’exploitation serveur ultérieur.</span><span class="sxs-lookup"><span data-stu-id="7c14f-1356">Note that the target computer must be running Windows Server 2008 or a later server operating system.</span></span>


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a><span data-ttu-id="7c14f-1357">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c14f-1357">Requirements</span></span>



| <span data-ttu-id="7c14f-1358">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c14f-1358">Requirement</span></span> | <span data-ttu-id="7c14f-1359">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c14f-1359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c14f-1360">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1360">Minimum supported client</span></span><br/> | <span data-ttu-id="7c14f-1361">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1361">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7c14f-1362">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c14f-1362">Minimum supported server</span></span><br/> | <span data-ttu-id="7c14f-1363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c14f-1363">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7c14f-1364">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7c14f-1364">Namespace</span></span><br/>                | <span data-ttu-id="7c14f-1365">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7c14f-1365">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="7c14f-1366">MOF</span><span class="sxs-lookup"><span data-stu-id="7c14f-1366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c14f-1367"><dt>ServerCompProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c14f-1367"><dt>ServerCompProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c14f-1368">DLL</span><span class="sxs-lookup"><span data-stu-id="7c14f-1368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c14f-1369"><dt>ServerCompProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c14f-1369"><dt>ServerCompProv.dll</dt></span></span> </dl> |



 

