---
title: Comment les clients composent le SPN d’un service
description: Pour authentifier un service, une application cliente compose un SPN pour l’instance de service à laquelle il doit se connecter.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Comment les clients composent la publicité SPN d’un service
- nom de principal du service AD, comment les clients composent le SPN d’un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd8aa599b6d8238017897c9383bab188ce144e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939633"
---
# <a name="how-clients-compose-a-services-spn"></a><span data-ttu-id="28f05-105">Comment les clients composent le SPN d’un service</span><span class="sxs-lookup"><span data-stu-id="28f05-105">How Clients Compose a Service's SPN</span></span>

<span data-ttu-id="28f05-106">Pour authentifier un service, une application cliente compose un SPN pour l’instance de service à laquelle il doit se connecter.</span><span class="sxs-lookup"><span data-stu-id="28f05-106">To authenticate a service, a client application composes an SPN for the service instance to which it must connect.</span></span> <span data-ttu-id="28f05-107">L’application cliente peut utiliser la fonction [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) pour composer un SPN.</span><span class="sxs-lookup"><span data-stu-id="28f05-107">The client application can use the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function to compose an SPN.</span></span> <span data-ttu-id="28f05-108">Le client spécifie les composants du SPN à l’aide de données connues ou de données récupérées à partir de sources autres que le service lui-même.</span><span class="sxs-lookup"><span data-stu-id="28f05-108">The client specifies the components of the SPN using known data or data retrieved from sources other than the service itself.</span></span>

<span data-ttu-id="28f05-109">Le format d’un SPN est le suivant :</span><span class="sxs-lookup"><span data-stu-id="28f05-109">The form of an SPN is as shown in the following form:</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="28f05-110">Dans ce formulaire, « &lt; classe &gt; de service » et « &lt; hôte &gt; » sont requis.</span><span class="sxs-lookup"><span data-stu-id="28f05-110">In this form, "&lt;service class&gt;" and "&lt;host&gt;" are required.</span></span> <span data-ttu-id="28f05-111">« &lt; port &gt; » et « &lt; nom du service &gt; » sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="28f05-111">"&lt;port&gt;" and "&lt;service name&gt;" optional.</span></span>

<span data-ttu-id="28f05-112">En règle générale, le client reconnaît la &lt; partie « classe &gt; de service » du nom et reconnaît les composants facultatifs à inclure dans le SPN.</span><span class="sxs-lookup"><span data-stu-id="28f05-112">Typically, the client recognizes the "&lt;service class&gt;" part of the name, and recognizes which of the optional components to include in the SPN.</span></span> <span data-ttu-id="28f05-113">Le client peut récupérer des composants du SPN à partir de sources telles qu’un point de connexion de service (SCP) ou une entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="28f05-113">The client can retrieve components of the SPN from sources such as a service connection point (SCP) or user input.</span></span> <span data-ttu-id="28f05-114">Par exemple, le client peut lire l’attribut **servicednsname** du SCP d’un service pour obtenir le &lt; composant « host &gt; ».</span><span class="sxs-lookup"><span data-stu-id="28f05-114">For example, the client can read the **serviceDNSName** attribute of a service's SCP to get the "&lt;host&gt;" component.</span></span> <span data-ttu-id="28f05-115">L’attribut **servicednsname** contient soit le nom DNS du serveur sur lequel s’exécute l’instance de service, soit le nom DNS des enregistrements SRV contenant les données d’hôte pour les réplicas de service.</span><span class="sxs-lookup"><span data-stu-id="28f05-115">The **serviceDNSName** attribute contains either the DNS name of the server on which the service instance is running or the DNS name of SRV records containing the host data for service replicas.</span></span> <span data-ttu-id="28f05-116">Le &lt; composant « nom du service &gt; », utilisé uniquement pour les services réplicables, peut être le nom unique du SCP du service, le nom DNS du domaine pris en charge par le service ou le nom DNS des enregistrements SRV ou MX.</span><span class="sxs-lookup"><span data-stu-id="28f05-116">The "&lt;service name&gt;" component, used only for replicable services, can be the distinguished name of the service's SCP, the DNS name of the domain served by the service, or the DNS name of SRV or MX records.</span></span>

<span data-ttu-id="28f05-117">Pour plus d’informations et pour obtenir un exemple de code utilisé pour composer un SPN pour un service, consultez [Comment un client authentifie un service Windows Sockets SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span><span class="sxs-lookup"><span data-stu-id="28f05-117">For more information and a code example used to compose an SPN for a service, see [How a Client Authenticates an SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span></span>

<span data-ttu-id="28f05-118">Pour plus d’informations et pour obtenir une description des composants SPN, consultez [formats de noms pour les noms de](name-formats-for-unique-spns.md)principal du service uniques.</span><span class="sxs-lookup"><span data-stu-id="28f05-118">For more information and a description of the SPN components, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

 

 




