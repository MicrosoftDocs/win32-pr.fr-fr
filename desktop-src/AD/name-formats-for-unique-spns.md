---
title: Formats de noms pour les SPN uniques
description: Un nom principal de service doit être unique dans la forêt dans laquelle il est enregistré.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formats de noms pour les noms de principal du service (SPN) uniques
- Nom du principal du service AD, formats de noms pour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda13cf5a095f8f2fd7ef1a209c6f3aeebd6654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190752"
---
# <a name="name-formats-for-unique-spns"></a><span data-ttu-id="a0cb1-105">Formats de noms pour les SPN uniques</span><span class="sxs-lookup"><span data-stu-id="a0cb1-105">Name Formats for Unique SPNs</span></span>

<span data-ttu-id="a0cb1-106">Un nom principal de service doit être unique dans la forêt dans laquelle il est enregistré.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-106">An SPN must be unique in the forest in which it is registered.</span></span> <span data-ttu-id="a0cb1-107">S’il n’est pas unique, l’authentification échoue.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-107">If it is not unique, authentication will fail.</span></span> <span data-ttu-id="a0cb1-108">La syntaxe du SPN comporte quatre éléments : deux éléments obligatoires et deux éléments supplémentaires que vous pouvez utiliser, si nécessaire, pour produire un nom unique comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-108">The SPN syntax has four elements: two required elements and two additional elements that you can use, if necessary, to produce a unique name as listed in the following table.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0cb1-109">Élément</span><span class="sxs-lookup"><span data-stu-id="a0cb1-109">Element</span></span></th>
<th><span data-ttu-id="a0cb1-110">Description</span><span class="sxs-lookup"><span data-stu-id="a0cb1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0cb1-111">&quot;&lt;classe de service&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="a0cb1-111">&quot;&lt;service class&gt;&quot;</span></span></td>
<td><span data-ttu-id="a0cb1-112">Chaîne qui identifie la classe générale du service ; par exemple, &quot; SqlServer &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0cb1-112">A string that identifies the general class of service; for example, &quot;SqlServer&quot;.</span></span> <span data-ttu-id="a0cb1-113">Il existe des noms de classe de service bien connus, tels que &quot; www &quot; pour un service Web ou &quot; LDAP &quot; pour un service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-113">There are well-known service class names, such as &quot;www&quot; for a web service or &quot;ldap&quot; for a directory service.</span></span> <span data-ttu-id="a0cb1-114">En général, il peut s’agir de n’importe quelle chaîne propre à la classe de service.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-114">In general, this can be any string that is unique to the service class.</span></span> <span data-ttu-id="a0cb1-115">Sachez que la syntaxe du SPN utilise une barre oblique (/) pour séparer les éléments, de sorte que ce caractère ne peut pas figurer dans un nom de classe de service.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-115">Be aware that the SPN syntax uses a forward slash (/) to separate elements, so this character cannot appear in a service class name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0cb1-116">&quot;&lt;HBA&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="a0cb1-116">&quot;&lt;host&gt;&quot;</span></span></td>
<td><span data-ttu-id="a0cb1-117">Nom de l’ordinateur sur lequel le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-117">The name of the computer on which the service is running.</span></span> <span data-ttu-id="a0cb1-118">Il peut s’agir d’un nom DNS complet ou d’un nom NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-118">This can be a fully qualified DNS name or a NetBIOS name.</span></span> <span data-ttu-id="a0cb1-119">Sachez qu'il n'existe aucune garantie que les noms NetBIOS soient uniques dans une forêt ; par conséquent, un SPN qui contient un nom NetBIOS peut ne pas être unique.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-119">Be aware that NetBIOS names are not guaranteed to be unique in a forest, so an SPN that contains a NetBIOS name may not be unique.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0cb1-120">&quot;&lt;port&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="a0cb1-120">&quot;&lt;port&gt;&quot;</span></span></td>
<td><span data-ttu-id="a0cb1-121">Numéro de port facultatif permettant de faire la distinction entre plusieurs instances de la même classe de service sur un seul ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-121">An optional port number to differentiate between multiple instances of the same service class on a single host computer.</span></span> <span data-ttu-id="a0cb1-122">Omettez ce composant si le service utilise le port par défaut pour sa classe de service.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-122">Omit this component if the service uses the default port for its service class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0cb1-123">&quot;&lt;nom du service&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="a0cb1-123">&quot;&lt;service name&gt;&quot;</span></span></td>
<td><span data-ttu-id="a0cb1-124">Nom facultatif utilisé dans les noms de principal du service d’un service réplicable pour identifier les données ou services fournis par le service ou le domaine pris en charge par le service.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-124">An optional name used in the SPNs of a replicable service to identify the data or services provided by the service or the domain served by the service.</span></span> <span data-ttu-id="a0cb1-125">Ce composant peut avoir l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="a0cb1-125">This component can have one of the following formats:</span></span>
<ul>
<li><span data-ttu-id="a0cb1-126">Nom unique ou objectGUID d’un objet dans Active Directory Domain Services, tel qu’un point de connexion de service (SCP).</span><span class="sxs-lookup"><span data-stu-id="a0cb1-126">The distinguished name or objectGUID of an object in Active Directory Domain Services, such as a service connection point (SCP).</span></span></li>
<li><span data-ttu-id="a0cb1-127">Nom DNS du domaine pour un service qui fournit un service spécifié pour un domaine dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-127">The DNS name of the domain for a service that provides a specified service for a domain as a whole.</span></span></li>
<li><span data-ttu-id="a0cb1-128">Nom DNS d’un enregistrement SRV ou MX.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-128">The DNS name of an SRV or MX record.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a0cb1-129">Les composants présents dans les SPN d’un service dépendent de la façon dont le service est identifié et répliqué.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-129">The components present in a service's SPNs depend on how the service is identified and replicated.</span></span> <span data-ttu-id="a0cb1-130">Il existe deux scénarios de base : les services basés sur l’hôte et les services réplicables.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-130">There are two basic scenarios: host-based services and replicable services.</span></span>

## <a name="host-based-services"></a><span data-ttu-id="a0cb1-131">Services basés sur l’hôte</span><span class="sxs-lookup"><span data-stu-id="a0cb1-131">Host-based services</span></span>

<span data-ttu-id="a0cb1-132">Pour un service basé sur l’hôte, le &lt; composant « nom du service &gt; » est omis, car le service est identifié de manière unique par la classe de service et par le nom de l’ordinateur hôte sur lequel le service est installé.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-132">For a host-based service, the "&lt;service name&gt;" component is omitted because the service is uniquely identified by the service class and the name of the host computer on which the service is installed.</span></span>


```C++
<service class>/<host>
```



<span data-ttu-id="a0cb1-133">La classe de service seule est suffisante pour identifier les fonctionnalités fournies par le service pour les clients.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-133">The service class alone is sufficient to identify for clients the features that the service provides.</span></span> <span data-ttu-id="a0cb1-134">Vous pouvez installer des instances de la classe de service sur de nombreux ordinateurs et chaque instance fournit des services identifiés avec son ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-134">You can install instances of the service class on many computers and each instance provides services that are identified with its host computer.</span></span> <span data-ttu-id="a0cb1-135">FTP et Telnet sont des exemples de services basés sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-135">FTP and Telnet are examples of host-based services.</span></span> <span data-ttu-id="a0cb1-136">Les noms principaux de service d’une instance de service basée sur l’hôte peuvent inclure le numéro de port si le service utilise un port autre que celui par défaut ou s’il existe plusieurs instances du service sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-136">The SPNs of a host-based service instance can include the port number if the service uses a non-default port or there are multiple instances of the service on the host.</span></span>


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a><span data-ttu-id="a0cb1-137">Services réplicables</span><span class="sxs-lookup"><span data-stu-id="a0cb1-137">Replicable services</span></span>

<span data-ttu-id="a0cb1-138">Pour un service réplicable, il peut y avoir une ou plusieurs instances du service (réplicas), et les clients ne différencient pas le réplica auquel ils se connectent, car chacun fournit le même service.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-138">For a replicable service there can be one or many instances of the service (replicas), and clients do not differentiate which replica they connect to because each provides the same service.</span></span> <span data-ttu-id="a0cb1-139">Les SPN pour chaque réplica ont les mêmes « &lt; classe de service &gt; » et « &lt; nom de service &gt; », où « &lt; nom &gt; de service » identifie plus précisément les fonctionnalités fournies par le service.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-139">The SPNs for each replica have the same "&lt;service class&gt;" and "&lt;service name&gt;" components, where "&lt;service name&gt;" identifies more specifically the features provided by the service.</span></span> <span data-ttu-id="a0cb1-140">Seuls les &lt; composants « host &gt; » et « &lt; port » facultatifs &gt; varient d’un SPN à l’autres.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-140">Only the "&lt;host&gt;" and optional "&lt;port&gt;" components would vary from SPN to SPN.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="a0cb1-141">Par exemple, un service réplicable est une instance d’un service de base de données qui permet d’accéder à une base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-141">An example of a replicable service would be an instance of a database service that provides access to a specified database.</span></span> <span data-ttu-id="a0cb1-142">Dans ce cas, « &lt; classe &gt; de service » identifie l’application de base de données et « &lt; nom &gt; du service » identifie la base de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-142">In this case, "&lt;service class&gt;" identifies the database application and "&lt;service name&gt;" identifies the specific database.</span></span> <span data-ttu-id="a0cb1-143">« &lt; nom &gt; du service » peut être le nom unique d’un point de connexion de service (SCP) contenant les données de connexion de la base de données.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-143">"&lt;service name&gt;" could be the distinguished name of a service connection point (SCP) containing connection data for the database.</span></span>


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="a0cb1-144">Si les clients utilisent le nom NetBIOS pour composer le SPN d’un service, chaque réplica doit également inscrire un SPN contenant le nom NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-144">If clients will use the NetBIOS name to compose a service's SPN, each replica must also register an SPN containing the NetBIOS name.</span></span>


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="a0cb1-145">Un autre exemple de service réplicable est un service qui fournit des services à un domaine entier.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-145">Another example of a replicable service is one that provides services to an entire domain.</span></span> <span data-ttu-id="a0cb1-146">Dans ce cas, le &lt; composant « nom du service &gt; » est le nom DNS du domaine pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-146">In this case, the "&lt;service name&gt;" component is the DNS name of the domain being served.</span></span> <span data-ttu-id="a0cb1-147">Un KDC Kerberos est un exemple de ce type de service réplicable.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-147">A Kerberos KDC is an example of this type of replicable service.</span></span>

<span data-ttu-id="a0cb1-148">Sachez que si le nom DNS d’un ordinateur change, le système met à jour l' &lt; élément « host &gt; » pour tous les noms de principal du service (SPN) inscrits pour cet ordinateur hôte dans la forêt.</span><span class="sxs-lookup"><span data-stu-id="a0cb1-148">Be aware that if the DNS name of a computer changes, the system updates the "&lt;host&gt;" element for all registered SPNs for that host in the forest.</span></span>

 

 




