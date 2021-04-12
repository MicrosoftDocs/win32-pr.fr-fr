---
description: À mesure que des applications existantes deviennent obsolètes ou ne sont plus utilisées, vous devrez peut-être les supprimer.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Suppression d’une application COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393131"
---
# <a name="deleting-a-com-application"></a><span data-ttu-id="a321d-103">Suppression d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="a321d-103">Deleting a COM+ Application</span></span>

<span data-ttu-id="a321d-104">À mesure que des applications existantes deviennent obsolètes ou ne sont plus utilisées, vous devrez peut-être les supprimer.</span><span class="sxs-lookup"><span data-stu-id="a321d-104">As existing applications become dated or are no longer being used, you may need to remove them.</span></span>

<span data-ttu-id="a321d-105">**Pour supprimer une application COM+**</span><span class="sxs-lookup"><span data-stu-id="a321d-105">**To delete a COM+ application**</span></span>

1.  <span data-ttu-id="a321d-106">Dans l’arborescence de la console de l’outil d’administration Services de composants, sélectionnez l’ordinateur pour lequel vous souhaitez supprimer une application.</span><span class="sxs-lookup"><span data-stu-id="a321d-106">In the console tree of the Component Services administrative tool, select the computer for which you want to delete an application.</span></span>

2.  <span data-ttu-id="a321d-107">Ouvrez le dossier **applications com+** pour l’ordinateur spécifié afin d’afficher toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="a321d-107">Open the **COM+ Applications** folder for the specified computer to display all the applications.</span></span>

3.  <span data-ttu-id="a321d-108">Sélectionnez l’application que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a321d-108">Select the application you want to remove.</span></span>

4.  <span data-ttu-id="a321d-109">Si vous avez sélectionné une application serveur, arrêtez l’application.</span><span class="sxs-lookup"><span data-stu-id="a321d-109">If you selected a server application, shut down the application.</span></span> <span data-ttu-id="a321d-110">Vous pouvez arrêter une application en la sélectionnant dans l’outil d’administration Services de composants, en cliquant avec le bouton droit, puis en cliquant sur **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="a321d-110">You can shut down an application by selecting it in the Component Services administrative tool, right-clicking, and then clicking **Shut down**.</span></span> <span data-ttu-id="a321d-111">Si vous avez sélectionné une application de bibliothèque, assurez-vous que tous les processus qui utilisent actuellement cette application de bibliothèque sont arrêtés.</span><span class="sxs-lookup"><span data-stu-id="a321d-111">If you selected a library application, make sure that all processes currently using this library application are shut down.</span></span>

5.  <span data-ttu-id="a321d-112">Dans le menu **Action**, cliquez sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="a321d-112">On the **Action** menu, click **Delete**.</span></span> <span data-ttu-id="a321d-113">Vous pouvez également cliquer avec le bouton droit sur le nom de l’application, puis cliquer sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="a321d-113">You can also right-click the application name and then click **Delete**.</span></span> <span data-ttu-id="a321d-114">Vous pouvez également supprimer une application en la sélectionnant dans l’outil d’administration Services de composants et en appuyant sur la touche **Suppr** , ou vous pouvez sélectionner l’application, cliquer avec le bouton droit, puis cliquer sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="a321d-114">You can also delete an application by selecting it in the Component Services administrative tool and pressing the **Delete** key, or you can select the application, right-click, and then click **Delete**.</span></span>

6.  <span data-ttu-id="a321d-115">Cliquez sur **Oui** lorsque vous êtes invité à confirmer votre action.</span><span class="sxs-lookup"><span data-stu-id="a321d-115">Click **Yes** when prompted to confirm your action.</span></span>

<span data-ttu-id="a321d-116">En outre, si une application serveur ou un proxy d’application a été installé sur un ordinateur à l’aide de Windows Installer (comme décrit dans la section « installation d’applications COM+ » du Guide d’administration des services de composants), vous pouvez la supprimer via l’utilitaire ajout/suppression de programmes du panneau de configuration de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a321d-116">In addition, if a server application or application proxy has been installed on a computer using Windows Installer (as described in "Installing COM+ Applications" in the Component Services Administration Guide), you can delete it through the Add/Remove Programs utility in the Microsoft Windows Control Panel.</span></span> <span data-ttu-id="a321d-117">Ou vous pouvez supprimer une application serveur installée ou un proxy d’application à l’aide de la syntaxe de ligne de commande Windows Installer :</span><span class="sxs-lookup"><span data-stu-id="a321d-117">Or you can delete an installed server application or application proxy by using the Windows Installer command line syntax:</span></span>

<span data-ttu-id="a321d-118">nom de l’application **msiexec-x** *\_ \* *. msi**</span><span class="sxs-lookup"><span data-stu-id="a321d-118">**msiexec -x** *application\_name\*\*\*.msi*\*</span></span>

<span data-ttu-id="a321d-119">Ces méthodes sont particulièrement utiles pour supprimer des applications COM+ sur des ordinateurs clients qui n’exécutent pas l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="a321d-119">These methods are especially useful for deleting COM+ applications on client machines that are not running the Component Services administrative tool.</span></span>

<span data-ttu-id="a321d-120">La suppression de l’application supprime également tous les composants contenus dans l’application.</span><span class="sxs-lookup"><span data-stu-id="a321d-120">Deleting the application also deletes any components contained in the application.</span></span> <span data-ttu-id="a321d-121">Si ces composants dépendent de ressources supplémentaires (connexions à la base de données, fichiers de données ou de texte, configuration de la racine virtuelle IIS, etc.), ces ressources doivent être supprimées par des mécanismes autres que l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="a321d-121">If these components depend on additional resources (database connections, data or text files, IIS virtual root configuration, and so on), these resources must be removed through mechanisms other than the Component Services administrative tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a321d-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a321d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a321d-123">Copier des composants</span><span class="sxs-lookup"><span data-stu-id="a321d-123">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="a321d-124">Création d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="a321d-124">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="a321d-125">Importation de composants</span><span class="sxs-lookup"><span data-stu-id="a321d-125">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="a321d-126">Installation de nouveaux composants</span><span class="sxs-lookup"><span data-stu-id="a321d-126">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="a321d-127">Déplacement des composants</span><span class="sxs-lookup"><span data-stu-id="a321d-127">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="a321d-128">Suppression d’un composant d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="a321d-128">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



