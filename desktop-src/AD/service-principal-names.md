---
title: Noms des principaux du service
description: Un nom de principal du service (SPN) est un identificateur unique d’une instance de service.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Noms des principaux du service
- SPN voir noms de principal du service
- nom de principal du service AD
- nom de principal du service AD, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842022"
---
# <a name="service-principal-names"></a><span data-ttu-id="b0867-107">Noms des principaux du service</span><span class="sxs-lookup"><span data-stu-id="b0867-107">Service Principal Names</span></span>

<span data-ttu-id="b0867-108">Un nom de principal du service (SPN) est un identificateur unique d’une instance de service.</span><span class="sxs-lookup"><span data-stu-id="b0867-108">A service principal name (SPN) is a unique identifier of a service instance.</span></span> <span data-ttu-id="b0867-109">Les SPN sont utilisés par [l’authentification Kerberos](mutual-authentication-using-kerberos.md) pour associer une instance de service à un compte d’ouverture de session de service.</span><span class="sxs-lookup"><span data-stu-id="b0867-109">SPNs are used by [Kerberos authentication](mutual-authentication-using-kerberos.md) to associate a service instance with a service logon account.</span></span> <span data-ttu-id="b0867-110">Cela permet à une application cliente de demander que le service authentifie un compte même si le client n’a pas le nom du compte.</span><span class="sxs-lookup"><span data-stu-id="b0867-110">This allows a client application to request that the service authenticate an account even if the client does not have the account name.</span></span>

<span data-ttu-id="b0867-111">Si vous installez plusieurs instances d'un service sur les ordinateurs d'une forêt, chaque instance doit posséder son propre SPN.</span><span class="sxs-lookup"><span data-stu-id="b0867-111">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="b0867-112">Une instance de service donnée peut posséder plusieurs noms SPN si les clients peuvent utiliser plusieurs noms pour l'authentification.</span><span class="sxs-lookup"><span data-stu-id="b0867-112">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="b0867-113">Par exemple, un nom de principal du service (SPN) comprend toujours le nom de l’ordinateur hôte sur lequel l’instance de service s’exécute, de sorte qu’une instance de service peut inscrire un SPN pour chaque nom ou alias de son hôte.</span><span class="sxs-lookup"><span data-stu-id="b0867-113">For example, an SPN always includes the name of the host computer on which the service instance is running, so a service instance might register an SPN for each name or alias of its host.</span></span> <span data-ttu-id="b0867-114">Pour plus d’informations sur le format SPN et la composition d’un nom principal de service unique, consultez [formats de noms pour les noms de principal du service uniques](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="b0867-114">For more information about SPN format and composing a unique SPN, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

<span data-ttu-id="b0867-115">Avant que le service d’authentification Kerberos puisse utiliser un nom de principal du service pour authentifier un service, le SPN doit être inscrit sur l’objet de compte utilisé par l’instance de service pour ouvrir une session.</span><span class="sxs-lookup"><span data-stu-id="b0867-115">Before the Kerberos authentication service can use an SPN to authenticate a service, the SPN must be registered on the account object that the service instance uses to log on.</span></span> <span data-ttu-id="b0867-116">Un SPN donné peut être inscrit sur un seul compte.</span><span class="sxs-lookup"><span data-stu-id="b0867-116">A given SPN can be registered on only one account.</span></span> <span data-ttu-id="b0867-117">Pour les services Win32, un programme d’installation de service spécifie le compte d’ouverture de session lorsqu’une instance du service est installée.</span><span class="sxs-lookup"><span data-stu-id="b0867-117">For Win32 services, a service installer specifies the logon account when an instance of the service is installed.</span></span> <span data-ttu-id="b0867-118">Le programme d’installation compose ensuite les noms de principal du service et les écrit en tant que propriété de l’objet de compte dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b0867-118">The installer then composes the SPNs and writes them as a property of the account object in Active Directory Domain Services.</span></span> <span data-ttu-id="b0867-119">Si le compte d’ouverture de session d’une instance de service change, les SPN doivent être réinscrits sous le nouveau compte.</span><span class="sxs-lookup"><span data-stu-id="b0867-119">If the logon account of a service instance changes, the SPNs must be re-registered under the new account.</span></span> <span data-ttu-id="b0867-120">Pour plus d’informations, consultez [Comment un service enregistre ses SPN](how-a-service-registers-its-spns.md).</span><span class="sxs-lookup"><span data-stu-id="b0867-120">For more information, see [How a Service Registers its SPNs](how-a-service-registers-its-spns.md).</span></span>

<span data-ttu-id="b0867-121">Pour se connecter à un service, le client localise une instance du service, compose le nom principal du service pour cette instance, se connecte au service et présente le nom principal de service pour que le service s'authentifie.</span><span class="sxs-lookup"><span data-stu-id="b0867-121">When a client wants to connect to a service, it locates an instance of the service, composes an SPN for that instance, connects to the service, and presents the SPN for the service to authenticate.</span></span> <span data-ttu-id="b0867-122">Pour plus d’informations, consultez [Comment les clients composent le SPN d’un service](how-clients-compose-a-serviceampaposs-spn.md).</span><span class="sxs-lookup"><span data-stu-id="b0867-122">For more information, see [How Clients Compose a Service's SPN](how-clients-compose-a-serviceampaposs-spn.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b0867-123">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b0867-123">In this Section</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b0867-124">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b0867-124">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b0867-125">Formats de noms pour les SPN uniques</span><span class="sxs-lookup"><span data-stu-id="b0867-125">Name Formats for Unique SPNs</span></span>](name-formats-for-unique-spns.md)
</dt> <dt>

[<span data-ttu-id="b0867-126">Comment un service compose ses SPN</span><span class="sxs-lookup"><span data-stu-id="b0867-126">How a Service Composes its SPNs</span></span>](how-a-service-composes-its-spns.md)
</dt> <dt>

[<span data-ttu-id="b0867-127">Comment un service enregistre ses SPN</span><span class="sxs-lookup"><span data-stu-id="b0867-127">How a Service Registers its SPNs</span></span>](how-a-service-registers-its-spns.md)
</dt> <dt>

[<span data-ttu-id="b0867-128">Comment les clients composent le SPN d’un service</span><span class="sxs-lookup"><span data-stu-id="b0867-128">How Clients Compose a Service's SPN</span></span>](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="b0867-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0867-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0867-130">Qu’est-ce qu’un SPN et Pourquoi devez-vous vous en soucier ?</span><span class="sxs-lookup"><span data-stu-id="b0867-130">What is an SPN and why should you care?</span></span>](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[<span data-ttu-id="b0867-131">Authentification mutuelle à l'aide de Kerberos</span><span class="sxs-lookup"><span data-stu-id="b0867-131">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 