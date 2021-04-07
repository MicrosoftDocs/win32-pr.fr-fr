---
title: Publication avec des points de connexion de service
description: Le schéma Active Directory définit une classe d’objet serviceConnectionPoint (SCP) pour permettre à un service de publier facilement des données spécifiques au service dans l’annuaire.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Publication avec les points de connexion de service AD
- points de connexion de service AD
- points de connexion de service AD, publication avec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671250"
---
# <a name="publishing-with-service-connection-points"></a><span data-ttu-id="d90ce-106">Publication avec des points de connexion de service</span><span class="sxs-lookup"><span data-stu-id="d90ce-106">Publishing with Service Connection Points</span></span>

<span data-ttu-id="d90ce-107">Le schéma Active Directory définit une classe d’objet **serviceConnectionPoint** (SCP) pour permettre à un service de publier facilement des données spécifiques au service dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d90ce-107">The Active Directory Schema defines a **serviceConnectionPoint** (SCP) object class to make it easy for a service to publish service-specific data in the directory.</span></span> <span data-ttu-id="d90ce-108">Les clients du service utilisent les données d’un SCP pour rechercher, se connecter à une instance de votre service et l’authentifier.</span><span class="sxs-lookup"><span data-stu-id="d90ce-108">Clients of the service use the data in an SCP to locate, connect to, and authenticate an instance of your service.</span></span>

<span data-ttu-id="d90ce-109">Cette section fournit une vue d’ensemble des points de connexion de service et des exemples de code qui montrent comment une application client/service utilise les SCP.</span><span class="sxs-lookup"><span data-stu-id="d90ce-109">This section provides an overview of service connection points and code examples that show how a client/service application uses SCPs.</span></span>

<span data-ttu-id="d90ce-110">L’exemple de code suit ces étapes pour implémenter la publication de service avec SCP.</span><span class="sxs-lookup"><span data-stu-id="d90ce-110">The code example follows these steps to implement service publication with SCPs.</span></span>

<span data-ttu-id="d90ce-111">Pour plus d’informations et pour obtenir un exemple de code qui effectue ces étapes, consultez [création d’un point de connexion de service](creating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="d90ce-111">For more information and a code example that performs these steps, see [Creating a Service Connection Point](creating-a-service-connection-point.md).</span></span>

<span data-ttu-id="d90ce-112">**Pour créer des SCP dans le répertoire lors de l’installation du service**</span><span class="sxs-lookup"><span data-stu-id="d90ce-112">**To create SCPs in the directory at service installation**</span></span>

1.  <span data-ttu-id="d90ce-113">Établissez une liaison avec l’objet ordinateur pour l’ordinateur hôte sur lequel l’instance de service est installée.</span><span class="sxs-lookup"><span data-stu-id="d90ce-113">Bind to the computer object for the host computer on which the service instance is installed.</span></span>
2.  <span data-ttu-id="d90ce-114">Créez un objet SCP en tant qu’enfant de l’objet ordinateur, en spécifiant les valeurs initiales des attributs du SCP.</span><span class="sxs-lookup"><span data-stu-id="d90ce-114">Create an SCP object as a child of the computer object, specifying the initial values for the attributes of the SCP.</span></span>
3.  <span data-ttu-id="d90ce-115">Définissez des entrées de contrôle d’accès (ACE) dans le descripteur de sécurité de l’objet SCP pour permettre au service de modifier les propriétés SCP au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d90ce-115">Set access control entries (ACEs) in the security descriptor of the SCP object to enable the service to modify SCP properties at run time.</span></span>
4.  <span data-ttu-id="d90ce-116">Mettez en cache l' **objectGUID** du SCP dans le registre sur l’ordinateur hôte du service.</span><span class="sxs-lookup"><span data-stu-id="d90ce-116">Cache the **objectGUID** of the SCP in the registry on the service's host computer.</span></span>

<span data-ttu-id="d90ce-117">Pour plus d’informations et pour obtenir un exemple de code qui effectue ces étapes, consultez [mise à jour d’un point de connexion de service](updating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="d90ce-117">For more information and a code example that performs these steps, see [Updating a Service Connection Point](updating-a-service-connection-point.md).</span></span>

<span data-ttu-id="d90ce-118">**Pour mettre à jour les attributs SCP au démarrage du service**</span><span class="sxs-lookup"><span data-stu-id="d90ce-118">**To update the SCP attributes at service startup**</span></span>

1.  <span data-ttu-id="d90ce-119">Récupérez l' **objectGUID** à partir du Registre et utilisez-le pour établir une liaison avec le SCP.</span><span class="sxs-lookup"><span data-stu-id="d90ce-119">Retrieve the **objectGUID** from the registry and use it to bind to the SCP.</span></span>
2.  <span data-ttu-id="d90ce-120">Récupérez les attributs, tels que **servicednsname** et **serviceBindingInformation**, à partir du SCP.</span><span class="sxs-lookup"><span data-stu-id="d90ce-120">Retrieve attributes, such as **serviceDNSName** and **serviceBindingInformation**, from the SCP.</span></span> <span data-ttu-id="d90ce-121">Comparez ces valeurs aux valeurs actuelles et mettez à jour le SCP si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d90ce-121">Compare these values to the current values and update the SCP if necessary.</span></span>

<span data-ttu-id="d90ce-122">Pour plus d’informations et pour obtenir un exemple de code qui effectue ces étapes, consultez [Comment les clients recherchent et utilisent un point de connexion de service](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="d90ce-122">For more information and a code example that performs these steps, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="d90ce-123">**Pour rechercher et utiliser un SCP par une application cliente**</span><span class="sxs-lookup"><span data-stu-id="d90ce-123">**To find and use an SCP by a client application**</span></span>

1.  <span data-ttu-id="d90ce-124">Établissez une liaison avec le catalogue global et recherchez des objets dont l’attribut **Keywords** correspond au GUID du produit du service.</span><span class="sxs-lookup"><span data-stu-id="d90ce-124">Bind to the Global Catalog and search for objects with a **keywords** attribute that matches the service's product GUID.</span></span> <span data-ttu-id="d90ce-125">Chaque objet trouvé est une instance du service.</span><span class="sxs-lookup"><span data-stu-id="d90ce-125">Each object found is an instance of the service.</span></span> <span data-ttu-id="d90ce-126">Sélectionnez une instance et récupérez le nom unique du SCP.</span><span class="sxs-lookup"><span data-stu-id="d90ce-126">Select an instance and retrieve the distinguished name of the SCP.</span></span>
2.  <span data-ttu-id="d90ce-127">Utilisez le nom unique pour effectuer une liaison au point de connexion de service.</span><span class="sxs-lookup"><span data-stu-id="d90ce-127">Use the distinguished name to bind to the SCP.</span></span>
3.  <span data-ttu-id="d90ce-128">Récupérez les valeurs de différents attributs du SCP, par exemple **servicednsname** et **serviceBindingInformation**.</span><span class="sxs-lookup"><span data-stu-id="d90ce-128">Retrieve the values of various attributes from the SCP, such as **serviceDNSName** and **serviceBindingInformation**.</span></span> <span data-ttu-id="d90ce-129">Utilisez ces valeurs pour la connexion et l'authentification auprès de l'instance de service.</span><span class="sxs-lookup"><span data-stu-id="d90ce-129">Use these values to connect to and authenticate the service instance.</span></span>

<span data-ttu-id="d90ce-130">Pour plus d’informations sur les rôles qui peuvent créer et mettre à jour un SCP, consultez [problèmes de sécurité pour la publication de service](security-issues-for-service-publication.md).</span><span class="sxs-lookup"><span data-stu-id="d90ce-130">For more information about what roles can create and update an SCP, see [Security Issues for Service Publication](security-issues-for-service-publication.md).</span></span>

<span data-ttu-id="d90ce-131">Pour plus d’informations sur l’emplacement de la création d’un SCP, consultez [où créer un point de connexion de service](where-to-create-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="d90ce-131">For more information about where to create an SCP, see [Where to Create a Service Connection Point](where-to-create-a-service-connection-point.md).</span></span>

<span data-ttu-id="d90ce-132">Pour plus d’informations sur le type de données à stocker dans un SCP, consultez [Propriétés du point de connexion de service](service-connection-point-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d90ce-132">For more information about the kind of data to store in an SCP, see [Service Connection Point Properties](service-connection-point-properties.md).</span></span>

<span data-ttu-id="d90ce-133">Pour plus d’informations sur la façon dont un programme d’installation de service et le service fonctionnent ensemble pour gérer les données actuelles dans un SCP, consultez [création et gestion d’un point de connexion de service](creating-and-maintaining-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="d90ce-133">For more information about how a service installer and the service work together to maintain current data in an SCP, see [Creating and Maintaining a Service Connection Point](creating-and-maintaining-a-service-connection-point.md).</span></span>

 

 




