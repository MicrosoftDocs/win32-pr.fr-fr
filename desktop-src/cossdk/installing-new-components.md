---
description: Pour ajouter des composants au dossier composants d’une application COM+, vous pouvez soit utiliser l’Assistant Installation de composant COM+, soit faire glisser des fichiers. dll contenant les composants de l’Explorateur Windows et les déposer dans l’application.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Installation de nouveaux composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033720"
---
# <a name="installing-new-components"></a><span data-ttu-id="cfb6e-103">Installation de nouveaux composants</span><span class="sxs-lookup"><span data-stu-id="cfb6e-103">Installing New Components</span></span>

<span data-ttu-id="cfb6e-104">Pour ajouter des composants au dossier **composants** d’une application com+, vous pouvez soit utiliser l’Assistant Installation de composant com+, soit faire glisser des fichiers. dll contenant les composants de l’Explorateur Windows et les déposer dans l’application.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-104">To add components to the **Components** folder of a COM+ application, you can either use the COM+ Component Install Wizard or drag .dll files that contain the components from the Windows Explorer and drop them in the application.</span></span>

<span data-ttu-id="cfb6e-105">Si vous utilisez l’Assistant Installation de composant COM+, vous pouvez installer un nouveau composant, qui inscrit le composant sur l’ordinateur, ou importer des composants qui ont déjà été inscrits.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-105">If you use the COM+ Component Install Wizard, you can either install a new component, which registers the component on the computer, or import components that have already been registered.</span></span> <span data-ttu-id="cfb6e-106">Des composants peuvent être ajoutés à des applications vides ou à des applications existantes.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-106">Components can be added to empty applications or existing applications.</span></span>

<span data-ttu-id="cfb6e-107">**Pour ajouter un composant à une application COM+**</span><span class="sxs-lookup"><span data-stu-id="cfb6e-107">**To add a component to a COM+ application**</span></span>

1.  <span data-ttu-id="cfb6e-108">Dans l’arborescence de la console de l’outil d’administration Services de composants, sélectionnez l’ordinateur qui héberge l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-108">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="cfb6e-109">Ouvrez le dossier **applications com+** pour cet ordinateur, puis sélectionnez l’application dans laquelle vous souhaitez installer le ou les composants.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-109">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component(s).</span></span>

3.  <span data-ttu-id="cfb6e-110">Ouvrez le dossier de l’application et sélectionnez **composants**.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-110">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="cfb6e-111">Dans le menu **action** , pointez sur **nouveau**, puis cliquez sur **composant**.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-111">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="cfb6e-112">Vous pouvez également cliquer avec le bouton droit sur le dossier **composants** , pointer sur **nouveau**, puis cliquer sur **composant**.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-112">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="cfb6e-113">Sur la page d' **Accueil** de l’Assistant Installation de l’application com+, cliquez sur **suivant**, puis dans la boîte de dialogue **importer ou installer un composant** , cliquez sur **installer de nouveaux composants** .</span><span class="sxs-lookup"><span data-stu-id="cfb6e-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Install new components** .</span></span>

6.  <span data-ttu-id="cfb6e-114">Dans la boîte de dialogue **installer les nouveaux composants** , cliquez sur **Ajouter** pour rechercher le composant que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-114">In the **Install new components** dialog box, click **Add** to browse for the component you want to add.</span></span>

7.  <span data-ttu-id="cfb6e-115">Dans la boîte de dialogue **Sélectionner les fichiers à installer** , tapez le nom du fichier du composant à installer ou sélectionnez un nom de fichier dans la liste affichée.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-115">In the **Select files to install** dialog box, type the filename of the component to install or select a filename from the displayed list.</span></span> <span data-ttu-id="cfb6e-116">Cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-116">Click **Open**.</span></span>

    <span data-ttu-id="cfb6e-117">Une fois que vous avez ajouté les fichiers, la boîte de dialogue **installer les nouveaux composants** affiche les fichiers que vous avez ajoutés et leurs composants associés.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-117">After you add the files, the **Install new components** dialog box displays the files you have added and their associated components.</span></span> <span data-ttu-id="cfb6e-118">Si vous activez la case à cocher **Détails** , vous obtenez plus d’informations sur le contenu du fichier et les composants qui ont été trouvés.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-118">If you select the **Details** check box, you will see more information about file contents and the components that were found.</span></span>

    > [!Note]  
    > <span data-ttu-id="cfb6e-119">Les composants COM non configurés doivent avoir une bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-119">Unconfigured COM components must have a type library.</span></span> <span data-ttu-id="cfb6e-120">Si COM+ ne trouve pas la bibliothèque de types de votre composant, votre composant n’apparaîtra pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-120">If COM+ cannot find your component's type library, your component will not appear in the list.</span></span> <span data-ttu-id="cfb6e-121">Vous pouvez également supprimer un fichier de la liste **fichiers à installer** en le sélectionnant et en cliquant sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-121">You can also remove a file from the **Files to install** list by selecting it and clicking **Remove**.</span></span>

     

8.  <span data-ttu-id="cfb6e-122">Cliquez sur **suivant**, puis sur **Terminer** pour installer le composant.</span><span class="sxs-lookup"><span data-stu-id="cfb6e-122">Click **Next**, and then click **Finish** to install the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfb6e-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cfb6e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfb6e-124">Copier des composants</span><span class="sxs-lookup"><span data-stu-id="cfb6e-124">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="cfb6e-125">Création d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="cfb6e-125">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="cfb6e-126">Suppression d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="cfb6e-126">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="cfb6e-127">Importation de composants</span><span class="sxs-lookup"><span data-stu-id="cfb6e-127">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="cfb6e-128">Déplacement des composants</span><span class="sxs-lookup"><span data-stu-id="cfb6e-128">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="cfb6e-129">Suppression d’un composant d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="cfb6e-129">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



