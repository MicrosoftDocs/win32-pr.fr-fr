---
title: Configuration du service de noms
description: À compter de Windows 2000, lorsque vous installez le SDK Windows, le programme d’installation sélectionne automatiquement Microsoft Locator comme fournisseur de services de noms. Vous pouvez modifier le nom du fournisseur de services par le biais du panneau de configuration.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462202"
---
# <a name="configuring-the-name-service"></a><span data-ttu-id="b42cb-104">Configuration du service de noms</span><span class="sxs-lookup"><span data-stu-id="b42cb-104">Configuring the Name Service</span></span>

<span data-ttu-id="b42cb-105">À compter de Windows 2000, lorsque vous installez le SDK Windows, le programme d’installation sélectionne automatiquement Microsoft Locator comme fournisseur de services de noms.</span><span class="sxs-lookup"><span data-stu-id="b42cb-105">Starting with Windows 2000, when you install the Windows SDK, the setup program automatically selects Microsoft Locator as the name service provider.</span></span> <span data-ttu-id="b42cb-106">Vous pouvez modifier le nom du fournisseur de services par le biais du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b42cb-106">You can change the name service provider through Control Panel.</span></span>

<span data-ttu-id="b42cb-107">L’ordinateur hôte qui exécute le NSID joue le rôle de passerelle vers le service d’annuaire de cellules/service d’annuaires de cellules DCE, en passant les appels de fonction NSI entre les ordinateurs qui exécutent des systèmes d’exploitation Microsoft et des ordinateurs DCE.</span><span class="sxs-lookup"><span data-stu-id="b42cb-107">The host computer that runs the nsid acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="b42cb-108">Une adresse réseau peut contenir jusqu’à 80 caractères, par exemple, 11.1.9.169 est une adresse valide.</span><span class="sxs-lookup"><span data-stu-id="b42cb-108">A network address can be up to 80 characters—for example, 11.1.9.169 is a valid address.</span></span>

> [!Note]  
> <span data-ttu-id="b42cb-109">Vous devez disposer du produit CDS (Digital Equipment) DCE pour configurer les CDS DCE en tant que fournisseur de services de noms.</span><span class="sxs-lookup"><span data-stu-id="b42cb-109">You must have the Digital Equipment Corporation DCE CDS product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="b42cb-110">Consultez la documentation fournie par Digital Equipment Corporation pour plus d’informations sur les CDS DCE.</span><span class="sxs-lookup"><span data-stu-id="b42cb-110">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

 

<span data-ttu-id="b42cb-111">**Pour reconfigurer le fournisseur de services de noms**</span><span class="sxs-lookup"><span data-stu-id="b42cb-111">**To reconfigure the name service provider**</span></span>

1.  <span data-ttu-id="b42cb-112">Dans le panneau de configuration, cliquez sur l’icône **connexions réseau** .</span><span class="sxs-lookup"><span data-stu-id="b42cb-112">In Control Panel, click the **Network Connections** icon.</span></span> <span data-ttu-id="b42cb-113">La fenêtre **connexions réseau** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b42cb-113">The **Network Connections** window appears.</span></span>
2.  <span data-ttu-id="b42cb-114">Sélectionnez la connexion réseau à configurer, cliquez avec le bouton droit, puis sélectionnez **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="b42cb-114">Select the network connection to configure, right-click, and select **Properties** from the context menu.</span></span> <span data-ttu-id="b42cb-115">La boîte de dialogue **Propriétés de connexion** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b42cb-115">The **Connection Properties** dialog appears.</span></span>
3.  <span data-ttu-id="b42cb-116">Dans la boîte de dialogue **Propriétés de connexion** , sélectionnez **client pour les réseaux Microsoft** , puis cliquez sur le bouton **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="b42cb-116">In the **Connection Properties** dialog, select **Client for Microsoft Networks** and click the **Properties** button.</span></span> <span data-ttu-id="b42cb-117">La boîte **de dialogue Propriétés du client pour Microsoft Network** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b42cb-117">The **Client for Microsoft Network Properties** dialog appears.</span></span>
4.  <span data-ttu-id="b42cb-118">Dans la boîte de dialogue **Propriétés du client pour Microsoft Network** , ouvrez la liste déroulante **fournisseur de services de noms** et sélectionnez un fournisseur de noms dans la liste.</span><span class="sxs-lookup"><span data-stu-id="b42cb-118">In the **Client for Microsoft Network Properties** dialog, open the **Name service provider** drop-down and select a name provider from the list.</span></span>
    1.  <span data-ttu-id="b42cb-119">Lorsque vous sélectionnez Microsoft Locator, cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="b42cb-119">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="b42cb-120">Le processus de configuration est alors terminé.</span><span class="sxs-lookup"><span data-stu-id="b42cb-120">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="b42cb-121">Lorsque vous sélectionnez le service d’annuaire de cellules/service d’annuaires de cellules DCE, dans la zone **adresse réseau** , tapez le nom de l’ordinateur hôte qui exécute le démon NSI (NSID), puis cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="b42cb-121">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

<span data-ttu-id="b42cb-122">**Pour reconfigurer le fournisseur de services de noms pour Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="b42cb-122">**To reconfigure the name service provider for Windows 2000**</span></span>

1.  <span data-ttu-id="b42cb-123">Dans le panneau de configuration, cliquez sur l’icône **réseau** .</span><span class="sxs-lookup"><span data-stu-id="b42cb-123">In Control Panel, click the **Network** icon.</span></span>

    <span data-ttu-id="b42cb-124">La boîte de dialogue **réseau** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b42cb-124">The **Network** dialog box appears.</span></span>

2.  <span data-ttu-id="b42cb-125">Dans la boîte de dialogue **réseau** , cliquez sur **configurer**.</span><span class="sxs-lookup"><span data-stu-id="b42cb-125">In the **Network** dialog box, click **Configure**.</span></span>
3.  <span data-ttu-id="b42cb-126">Dans la liste **NetworkSoftware** , sélectionnez **configuration RPC**.</span><span class="sxs-lookup"><span data-stu-id="b42cb-126">In the **NetworkSoftware** list, select **RPC Configuration**.</span></span>

    <span data-ttu-id="b42cb-127">La boîte de dialogue **configuration du fournisseur de services de noms RPC** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b42cb-127">The **RPC Name Service Provider Configuration** dialog box appears.</span></span>

4.  <span data-ttu-id="b42cb-128">Dans la boîte de dialogue **configuration du fournisseur de services de noms RPC** , sélectionnez un fournisseur de services de noms dans la liste.</span><span class="sxs-lookup"><span data-stu-id="b42cb-128">In the **RPC Name Service Provider Configuration** dialog box, select a name service provider from the list.</span></span>
    1.  <span data-ttu-id="b42cb-129">Lorsque vous sélectionnez Microsoft Locator, cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="b42cb-129">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="b42cb-130">Le processus de configuration est alors terminé.</span><span class="sxs-lookup"><span data-stu-id="b42cb-130">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="b42cb-131">Lorsque vous sélectionnez le service d’annuaire de cellules/service d’annuaires de cellules DCE, dans la zone **adresse réseau** , tapez le nom de l’ordinateur hôte qui exécute le démon NSI (NSID), puis cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="b42cb-131">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

 

 




