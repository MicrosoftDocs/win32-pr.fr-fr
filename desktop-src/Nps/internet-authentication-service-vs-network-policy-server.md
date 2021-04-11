---
title: Service d’authentification Internet & le serveur NPS (Network Policy Server)
description: Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca657da17e823caa51e8401905a8a0a3e307e975
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104032007"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="968ff-103">Service d’authentification Internet & le serveur NPS (Network Policy Server)</span><span class="sxs-lookup"><span data-stu-id="968ff-103">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="968ff-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server).</span><span class="sxs-lookup"><span data-stu-id="968ff-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="968ff-105">Service d'authentification Internet</span><span class="sxs-lookup"><span data-stu-id="968ff-105">Internet Authentication Service</span></span>

<span data-ttu-id="968ff-106">Le service d’authentification Internet est l’implémentation Microsoft d’un serveur et d’un proxy RADIUS.</span><span class="sxs-lookup"><span data-stu-id="968ff-106">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="968ff-107">Le service d’authentification Internet prend en charge deux ensembles d’API : l’API des [extensions du serveur de stratégie réseau](ias-extensions.md) et l' [API des objets de données serveur](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="968ff-107">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="968ff-108">Pour plus d’informations sur IAS, voir [TechNet : service d’authentification Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="968ff-108">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="968ff-109">Serveur de stratégie réseau</span><span class="sxs-lookup"><span data-stu-id="968ff-109">Network Policy Server</span></span>

<span data-ttu-id="968ff-110">Le serveur NPS (Network Policy Server) est l’implémentation Microsoft d’un serveur et d’un proxy RADIUS et est disponible sur les serveurs Windows à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="968ff-110">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="968ff-111">NPS prend en charge les deux mêmes jeux d’API que IAS : [API d’extension de serveur de stratégie réseau](ias-extensions.md) et [API d’objets de données serveur](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="968ff-111">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="968ff-112">En outre, NPS contient un ensemble de nouvelles fonctionnalités qui étendent les fonctionnalités d’IAS.</span><span class="sxs-lookup"><span data-stu-id="968ff-112">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="968ff-113">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="968ff-113">Feature</span></span></th>
<th><span data-ttu-id="968ff-114">Nouveautés du serveur NPS</span><span class="sxs-lookup"><span data-stu-id="968ff-114">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="968ff-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Protection d’accès réseau (NAP)</a></span><span class="sxs-lookup"><span data-stu-id="968ff-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="968ff-116">NPS est le serveur central de la protection d’accès réseau.</span><span class="sxs-lookup"><span data-stu-id="968ff-116">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="968ff-117">NPS prend en charge la création de stratégies à l’aide des conditions supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="968ff-117">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="968ff-118">Expiration de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="968ff-118">Policy expiration.</span></span></li>
<li><span data-ttu-id="968ff-119">Version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="968ff-119">Operating system version.</span></span></li>
<li><span data-ttu-id="968ff-120">Accédez à l’adresse IP du client.</span><span class="sxs-lookup"><span data-stu-id="968ff-120">Access client IP address.</span></span></li>
<li><span data-ttu-id="968ff-121">Stratégies de contrôle d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="968ff-121">Health policies.</span></span></li>
<li><span data-ttu-id="968ff-122">Types EAP autorisés.</span><span class="sxs-lookup"><span data-stu-id="968ff-122">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="968ff-123">HCAP.</span><span class="sxs-lookup"><span data-stu-id="968ff-123">HCAP.</span></span></li>
</ul>
<span data-ttu-id="968ff-124">NPS prend en charge la création de stratégies à l’aide des paramètres supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="968ff-124">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="968ff-125">Accompli.</span><span class="sxs-lookup"><span data-stu-id="968ff-125">Probation.</span></span></li>
<li><span data-ttu-id="968ff-126">Accès limité.</span><span class="sxs-lookup"><span data-stu-id="968ff-126">Limited access.</span></span></li>
<li><span data-ttu-id="968ff-127">État étendu pour un accès limité.</span><span class="sxs-lookup"><span data-stu-id="968ff-127">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="968ff-128">NPS, via NAP, interagit avec CISCO NAC.</span><span class="sxs-lookup"><span data-stu-id="968ff-128">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="968ff-129">IAS ne prend pas en charge la protection d’accès réseau.</span><span class="sxs-lookup"><span data-stu-id="968ff-129">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="968ff-130"><a href="/windows/win32/eap/eap-start-page">Protocole EAP</a> Prise en charge des stratégies et <a href="/windows/win32/eaphost/portal">EAPHost</a></span><span class="sxs-lookup"><span data-stu-id="968ff-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="968ff-131">NPS utilise EAPHost pour l’extensibilité de la méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="968ff-131">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="968ff-132">En outre, les administrateurs peuvent configurer la stratégie d’accès réseau pour le protocole EAP.</span><span class="sxs-lookup"><span data-stu-id="968ff-132">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="968ff-133">IAS ne prend pas en charge l’intégration EAPHost ou les conditions de filtre de type EAP pour les stratégies.</span><span class="sxs-lookup"><span data-stu-id="968ff-133">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="968ff-134">Prise en charge D’ipv6</span><span class="sxs-lookup"><span data-stu-id="968ff-134">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="968ff-135">NPS prend en charge le déploiement dans les environnements IPv6.</span><span class="sxs-lookup"><span data-stu-id="968ff-135">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="968ff-136">IAS ne prend pas en charge les adresses réseau IPv6.</span><span class="sxs-lookup"><span data-stu-id="968ff-136">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="968ff-137">Configuration XML</span><span class="sxs-lookup"><span data-stu-id="968ff-137">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="968ff-138">La configuration NPS peut être importée et exportée au format XML.</span><span class="sxs-lookup"><span data-stu-id="968ff-138">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="968ff-139">IAS utilise une base de données Jet pour stocker la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="968ff-139">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="968ff-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Critères communs</a> Supporter</span><span class="sxs-lookup"><span data-stu-id="968ff-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="968ff-141">NPS a été mis à jour pour prendre en charge son déploiement dans des environnements qui doivent respecter les normes de sécurité critères communs.</span><span class="sxs-lookup"><span data-stu-id="968ff-141">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="968ff-142"><a href="ias-extensions.md">API des extensions NPS</a></span><span class="sxs-lookup"><span data-stu-id="968ff-142"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="968ff-143">Les dll d’extension NPS s’exécutent dans un processus distinct du service NPS.</span><span class="sxs-lookup"><span data-stu-id="968ff-143">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="968ff-144">En cas de panne d’une DLL d’extension, NPS continue à s’exécuter et les demandes futures seront rejetées.</span><span class="sxs-lookup"><span data-stu-id="968ff-144">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="968ff-145">Les dll d’extension IAS s’exécutent dans le même processus que le service IAS et peuvent avoir un impact négatif sur le service.</span><span class="sxs-lookup"><span data-stu-id="968ff-145">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="968ff-146">Interface utilisateur de gestion</span><span class="sxs-lookup"><span data-stu-id="968ff-146">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="968ff-147">La console de gestion NPS (NPS. msc) a une nouvelle apparence, une plus grande facilité d’utilisation et couvre toutes les nouvelles fonctionnalités ajoutées à NPS.</span><span class="sxs-lookup"><span data-stu-id="968ff-147">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="968ff-148">IAS utilise la console de gestion IAS. msc.</span><span class="sxs-lookup"><span data-stu-id="968ff-148">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="968ff-149">Outil de gestion des rôles et intégration des Gestionnaire de serveur</span><span class="sxs-lookup"><span data-stu-id="968ff-149">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="968ff-150">NPS est intégré au Gestionnaire de serveur et à l’outil de gestion des rôles.</span><span class="sxs-lookup"><span data-stu-id="968ff-150">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="968ff-151">Cette intégration facilite la configuration et la gestion du serveur NPS et des scénarios associés.</span><span class="sxs-lookup"><span data-stu-id="968ff-151">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="968ff-152">Gestionnaire de serveur n’est pas disponible sur les ordinateurs exécutant IAS.</span><span class="sxs-lookup"><span data-stu-id="968ff-152">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="968ff-153">Mise à jour des scripts de ligne de commande avec <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.</span><span class="sxs-lookup"><span data-stu-id="968ff-153">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="968ff-154">NPS prend en charge l' &quot; interface de ligne de commande netsh nps &quot; .</span><span class="sxs-lookup"><span data-stu-id="968ff-154">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="968ff-155">&quot;Netsh nps &quot; contient de nouvelles commandes qui permettent de configurer entièrement NPS, y compris les fonctionnalités NAP.</span><span class="sxs-lookup"><span data-stu-id="968ff-155">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="968ff-156">IAS prend en charge l' &quot; interface de ligne de commande netsh aaaa &quot; .</span><span class="sxs-lookup"><span data-stu-id="968ff-156">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="968ff-157">Isolation de la stratégie</span><span class="sxs-lookup"><span data-stu-id="968ff-157">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="968ff-158">NPS permet l’implémentation de l’isolation de la stratégie en définissant la source de la stratégie réseau.</span><span class="sxs-lookup"><span data-stu-id="968ff-158">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="968ff-159">Il est possible de configurer des stratégies qui s’appliquent uniquement à un type NAS prédéterminé.</span><span class="sxs-lookup"><span data-stu-id="968ff-159">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="968ff-160">IAS ne prend pas en charge l’isolation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="968ff-160">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="968ff-161">Pour plus d’informations sur NPS, voir [TechNet : serveur NPS (Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) ).</span><span class="sxs-lookup"><span data-stu-id="968ff-161">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="968ff-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="968ff-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="968ff-163">Authentification, autorisation et gestion des comptes RADIUS</span><span class="sxs-lookup"><span data-stu-id="968ff-163">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="968ff-164">Journalisation avec le serveur NPS</span><span class="sxs-lookup"><span data-stu-id="968ff-164">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="968ff-165">Utilisation d’un serveur d’État</span><span class="sxs-lookup"><span data-stu-id="968ff-165">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

