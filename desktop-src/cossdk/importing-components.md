---
description: Vous pouvez utiliser l’outil d’administration Services de composants pour importer dans des applications spécifiques des composants qui ont déjà été inscrits sur votre ordinateur en tant que composants COM dans le Registre Windows.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importation de composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483033"
---
# <a name="importing-components"></a><span data-ttu-id="8aa3d-103">Importation de composants</span><span class="sxs-lookup"><span data-stu-id="8aa3d-103">Importing Components</span></span>

<span data-ttu-id="8aa3d-104">Vous pouvez utiliser l’outil d’administration Services de composants pour importer dans des applications spécifiques des composants qui ont déjà été inscrits sur votre ordinateur en tant que composants COM dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-104">You can use the Component Services administrative tool to import into applications specific components that have already been registered on your computer as COM components in the Windows registry.</span></span> <span data-ttu-id="8aa3d-105">L’importation d’un composant n’installe pas les informations d’interface ou de méthode requises pour définir les propriétés de l’interface ou pour configurer l’accès au composant à partir d’un client distant.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-105">Importing a component does not install the interface or method information required to set interface properties or to configure access to the component from a remote client.</span></span> <span data-ttu-id="8aa3d-106">Par conséquent, si possible, vous devez installer plutôt que d’importer des composants non configurés.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-106">Therefore, if possible, you should install rather than import unconfigured components.</span></span>

> [!Note]  
> <span data-ttu-id="8aa3d-107">Lorsque vous importez un composant dans une application COM+, COM+ ne remplit pas les informations d’interface et de méthode du composant.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-107">When importing a component into a COM+ application, COM+ does not populate interface and method information for the component.</span></span> <span data-ttu-id="8aa3d-108">Lors de l’exportation d’un proxy d’application, COM+ ne fournit pas d’informations de marshaling (bibliothèques de types ou proxy/stubs) pour une partie ou l’ensemble des interfaces.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-108">During the export of an application proxy, COM+ will not provide marshaling information (type libraries or proxy/stubs) for some or all of the interfaces.</span></span> <span data-ttu-id="8aa3d-109">L’exportation de proxys d’application contenant des composants importés échouera ou entraînera l’émission d’un avertissement.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-109">Exporting application proxies that contain imported components will fail or cause a warning to be issued.</span></span>

 

<span data-ttu-id="8aa3d-110">**Pour importer un composant dans une application COM+**</span><span class="sxs-lookup"><span data-stu-id="8aa3d-110">**To import a component into a COM+ application**</span></span>

1.  <span data-ttu-id="8aa3d-111">Dans l’arborescence de la console de l’outil d’administration Services de composants, sélectionnez l’ordinateur qui héberge l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-111">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="8aa3d-112">Ouvrez le dossier **applications com+** pour cet ordinateur, puis sélectionnez l’application dans laquelle vous souhaitez installer le composant.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-112">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component.</span></span>

3.  <span data-ttu-id="8aa3d-113">Ouvrez le dossier de l’application et sélectionnez **composants**.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-113">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="8aa3d-114">Dans le menu **action** , pointez sur **nouveau**, puis cliquez sur **composant**.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-114">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="8aa3d-115">Vous pouvez également cliquer avec le bouton droit sur le dossier **composants** , pointer sur **nouveau**, puis cliquer sur **composant**.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-115">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="8aa3d-116">Sur la page d' **Accueil** de l’Assistant Installation de l’application com+, cliquez sur **suivant**, puis dans la boîte de dialogue **importer ou installer un composant** , cliquez sur **importer des composants qui sont déjà inscrits**.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-116">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Import component(s) that are already registered**.</span></span>

6.  <span data-ttu-id="8aa3d-117">Dans la boîte de dialogue **choisir les composants à importer** , activez la case à cocher **Détails** pour afficher des informations complètes sur les composants déjà inscrits.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-117">In the **Choose Components to Import** dialog box, select the **Details** check box to see complete information about the components that are already registered.</span></span> <span data-ttu-id="8aa3d-118">Sélectionnez le ou les composants que vous souhaitez importer dans la liste affichée, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-118">Select the component(s) you want to import from the displayed list, and click **Next**.</span></span>

7.  <span data-ttu-id="8aa3d-119">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="8aa3d-119">Click **Finish**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8aa3d-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8aa3d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aa3d-121">Copier des composants</span><span class="sxs-lookup"><span data-stu-id="8aa3d-121">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="8aa3d-122">Création d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="8aa3d-122">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="8aa3d-123">Suppression d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="8aa3d-123">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="8aa3d-124">Installation de nouveaux composants</span><span class="sxs-lookup"><span data-stu-id="8aa3d-124">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="8aa3d-125">Déplacement des composants</span><span class="sxs-lookup"><span data-stu-id="8aa3d-125">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="8aa3d-126">Suppression d’un composant d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="8aa3d-126">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



