---
description: Lorsqu’une application compatible SOAP a été exportée à partir d’un serveur en mode proxy, les clients qui l’importent peuvent accéder automatiquement aux méthodes des composants qu’elle contient, à distance, en tant que services Web proposés par le serveur en mode d’objet activé par le client (CAO). Cela vous permet de déployer très facilement les fonctionnalités d’une application COM+ sur un réseau sous la forme d’un service Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importation d’une application SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524199"
---
# <a name="importing-a-soap-enabled-application"></a><span data-ttu-id="d776c-104">Importation d’une application SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="d776c-104">Importing a SOAP-Enabled Application</span></span>

<span data-ttu-id="d776c-105">Lorsqu’une application compatible SOAP a été [exportée](exporting-a-soap-enabled-application.md) à partir d’un serveur en mode proxy, les clients qui l’importent peuvent accéder automatiquement aux méthodes des composants qu’elle contient, à distance, en tant que services Web proposés par le serveur en mode d’objet activé par le client (CAO).</span><span class="sxs-lookup"><span data-stu-id="d776c-105">When a SOAP-enabled application has been [exported](exporting-a-soap-enabled-application.md) from a server in proxy mode, clients that import it can automatically access the methods of the components it contains, remotely, as web services offered by the server in client-activated object (CAO) mode.</span></span> <span data-ttu-id="d776c-106">Cela vous permet de déployer très facilement les fonctionnalités d’une application COM+ sur un réseau sous la forme d’un service Web XML.</span><span class="sxs-lookup"><span data-stu-id="d776c-106">This allows you to very easily deploy the functionality of a COM+ application across a network as an XML web service.</span></span>

<span data-ttu-id="d776c-107">Lorsque les composants d’une application importés de cette façon sont utilisés sur le client, ils ne s’exécutent pas sur le client, mais sont accessibles à distance à l’aide du service Web XML fourni par le serveur à partir duquel l’application a été exportée.</span><span class="sxs-lookup"><span data-stu-id="d776c-107">When the components of an application imported in this way are used on the client, they do not run on the client but instead are accessed remotely by using the XML web service provided by the server from which the application was exported.</span></span> <span data-ttu-id="d776c-108">Pour plus d’informations sur l’utilisation des composants d’une application importée de cette manière, consultez [accès aux services Web XML en mode CAO](accessing-xml-web-services-in-cao-mode.md).</span><span class="sxs-lookup"><span data-stu-id="d776c-108">For details on using the components of an application imported in this way, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="d776c-109">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="d776c-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="d776c-110">Pour importer une application compatible SOAP dans un client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d776c-110">To import a SOAP-enabled application into a client, use the following steps:</span></span>

1.  <span data-ttu-id="d776c-111">Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier associé à l’ordinateur client sur lequel vous souhaitez installer l’application.</span><span class="sxs-lookup"><span data-stu-id="d776c-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the folder associated with the client computer on which you want to install the application.</span></span>

2.  <span data-ttu-id="d776c-112">Cliquez avec le bouton droit sur le dossier **applications com+** du client, puis choisissez **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="d776c-112">Right-click the client's **COM+ Applications** folder, and then choose **New**.</span></span> <span data-ttu-id="d776c-113">L' **Assistant Installation de l’application com+** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d776c-113">The **COM+ Application Install Wizard** appears.</span></span>

3.  <span data-ttu-id="d776c-114">Dans l' **Assistant Installation de l’application com+**, cliquez sur **installer une ou plusieurs applications prédéfinies**.</span><span class="sxs-lookup"><span data-stu-id="d776c-114">In the **COM+ Application Install Wizard**, click **Install pre-built application(s)**.</span></span>

4.  <span data-ttu-id="d776c-115">Parcourez le réseau pour localiser ou spécifier le chemin d’accès réseau du fichier MSI sur le serveur à partir duquel vous souhaitez installer l’application.</span><span class="sxs-lookup"><span data-stu-id="d776c-115">Browse the network to locate or specify the network path of the MSI file on the server from which you want to install the application.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="d776c-116">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d776c-116">Visual Basic</span></span>

<span data-ttu-id="d776c-117">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="d776c-117">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="d776c-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="d776c-118">C/C++</span></span>

<span data-ttu-id="d776c-119">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="d776c-119">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="d776c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d776c-120">Remarks</span></span>

<span data-ttu-id="d776c-121">Les composants COM sont identifiés par un GUID, qui change si les composants sont recompilés.</span><span class="sxs-lookup"><span data-stu-id="d776c-121">COM components are identified by a GUID, which changes if the components are recompiled.</span></span> <span data-ttu-id="d776c-122">Si un composant COM configuré qui est exposé en tant que service Web XML est recompilé, les applications clientes qui l’utilisent s’arrêteront.</span><span class="sxs-lookup"><span data-stu-id="d776c-122">If a configured COM component that is exposed as an XML web service is recompiled, client applications that use it will break.</span></span> <span data-ttu-id="d776c-123">Par conséquent, lorsqu’un composant qui est exposé en tant que service Web XML est recompilé, les clients doivent réimporter les applications qui utilisent le composant.</span><span class="sxs-lookup"><span data-stu-id="d776c-123">Therefore, when a component that is exposed as an XML web service is recompiled, clients should re-import the applications that use the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d776c-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d776c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d776c-125">Vue d’ensemble du service SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="d776c-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="d776c-126">Création de services Web XML</span><span class="sxs-lookup"><span data-stu-id="d776c-126">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="d776c-127">Exportation d’une application SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="d776c-127">Exporting a SOAP-Enabled Application</span></span>](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



