---
description: Un composant est une partie de l’application ou du produit à installer.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Composants Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952279"
---
# <a name="windows-installer-components"></a><span data-ttu-id="dda14-103">Composants Windows Installer</span><span class="sxs-lookup"><span data-stu-id="dda14-103">Windows Installer Components</span></span>

<span data-ttu-id="dda14-104">Un composant est une partie de l’application ou du produit à installer.</span><span class="sxs-lookup"><span data-stu-id="dda14-104">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="dda14-105">Exemples de composants : fichiers uniques, groupe de fichiers associés, objets COM, inscription, clés de Registre, raccourcis, ressources, bibliothèques regroupées dans un répertoire ou parties partagées de code, telles que MFC ou DAO.</span><span class="sxs-lookup"><span data-stu-id="dda14-105">Examples of components include single files, a group of related files, COM objects, registration, registry keys, shortcuts, resources, libraries grouped into a directory, or shared pieces of code such as MFC or DAO.</span></span>

<span data-ttu-id="dda14-106">Le service d’installation installe ou supprime un composant en tant qu’élément cohérent unique.</span><span class="sxs-lookup"><span data-stu-id="dda14-106">The installer service installs or removes a component as a single coherent piece.</span></span> <span data-ttu-id="dda14-107">Il effectue le suivi de chaque composant par le GUID d’ID de composant respectif spécifié dans la colonne ComponentId de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="dda14-107">It tracks every component by the respective component ID GUID specified in the ComponentId column of the [Component table](component-table.md).</span></span>

> [!Note]  
> <span data-ttu-id="dda14-108">Deux composants qui partagent le même ID de composant sont traités comme plusieurs instances du même composant, quel que soit leur contenu réel.</span><span class="sxs-lookup"><span data-stu-id="dda14-108">Two components that share the same component ID are treated as multiple instances of the same component regardless of their actual content.</span></span> <span data-ttu-id="dda14-109">Une seule instance de n’importe quel composant est installée sur l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dda14-109">Only a single instance of any component is installed on a user's computer.</span></span> <span data-ttu-id="dda14-110">Plusieurs fonctionnalités ou applications peuvent donc partager certains composants.</span><span class="sxs-lookup"><span data-stu-id="dda14-110">Several features or applications may therefore share some components.</span></span>

 

<span data-ttu-id="dda14-111">Étant donné que les composants sont généralement partagés, l’auteur d’un package d’installation doit respecter des règles strictes lors de la spécification des composants d’une fonctionnalité ou d’une application.</span><span class="sxs-lookup"><span data-stu-id="dda14-111">Because components are commonly shared, the author of an installation package must follow strict rules when specifying the components of a feature or application.</span></span> <span data-ttu-id="dda14-112">Cela est essentiel pour le bon fonctionnement du mécanisme de décompte de références Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="dda14-112">This is essential for the correct operation of the Windows Installer reference-counting mechanism.</span></span> <span data-ttu-id="dda14-113">Pour plus d’informations, consultez [Organisation des applications dans des composants](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="dda14-113">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="dda14-114">En résumé, ces règles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dda14-114">In brief, these rules are:</span></span>

-   <span data-ttu-id="dda14-115">Chaque composant doit être stocké dans un dossier unique.</span><span class="sxs-lookup"><span data-stu-id="dda14-115">Each component must be stored in a single folder.</span></span>
-   <span data-ttu-id="dda14-116">Aucun fichier, entrée de Registre, raccourci ou autre ressource ne doit être fourni en tant que membre de plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="dda14-116">No file, registry entry, shortcut, or other resources should ever be shipped as a member of more than one component.</span></span> <span data-ttu-id="dda14-117">Cela s’applique à tous les produits, versions de produits et entreprises.</span><span class="sxs-lookup"><span data-stu-id="dda14-117">This applies across products, product versions, and companies.</span></span>

<span data-ttu-id="dda14-118">Pour plus d’informations sur l’utilisation des composants, consultez.</span><span class="sxs-lookup"><span data-stu-id="dda14-118">For more information about using components, see</span></span>

-   [<span data-ttu-id="dda14-119">Installation d’un composant manquant</span><span class="sxs-lookup"><span data-stu-id="dda14-119">Installing a Missing Component</span></span>](installing-a-missing-component.md)
-   [<span data-ttu-id="dda14-120">Installation des composants permanents, des fichiers, des polices, des clés de Registre</span><span class="sxs-lookup"><span data-stu-id="dda14-120">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
-   [<span data-ttu-id="dda14-121">Utilisation des composants qualifiés</span><span class="sxs-lookup"><span data-stu-id="dda14-121">Using Qualified Components</span></span>](using-qualified-components.md)
-   [<span data-ttu-id="dda14-122">Utilisation de composants transitifs</span><span class="sxs-lookup"><span data-stu-id="dda14-122">Using Transitive Components</span></span>](using-transitive-components.md)
-   [<span data-ttu-id="dda14-123">Utilisation des fonctionnalités et des composants</span><span class="sxs-lookup"><span data-stu-id="dda14-123">Working with Features and Components</span></span>](working-with-features-and-components.md)
-   [<span data-ttu-id="dda14-124">Création d’un package volumineux</span><span class="sxs-lookup"><span data-stu-id="dda14-124">Authoring a Large Package</span></span>](authoring-a-large-package.md)
-   [<span data-ttu-id="dda14-125">Vérification de l’installation des fonctionnalités, des composants, des fichiers</span><span class="sxs-lookup"><span data-stu-id="dda14-125">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
-   [<span data-ttu-id="dda14-126">Recherche d’une fonctionnalité ou d’un composant endommagé</span><span class="sxs-lookup"><span data-stu-id="dda14-126">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
-   [<span data-ttu-id="dda14-127">Publication de produits, de fonctionnalités et de composants</span><span class="sxs-lookup"><span data-stu-id="dda14-127">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)

 

 



