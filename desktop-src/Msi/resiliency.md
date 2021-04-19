---
description: La résilience est la capacité d’une application à effectuer une récupération normale à partir de situations dans lesquelles un composant vital est manquant ou a été remplacée par une version incompatible.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Résilience
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524397"
---
# <a name="resiliency"></a><span data-ttu-id="b4e30-103">Résilience</span><span class="sxs-lookup"><span data-stu-id="b4e30-103">Resiliency</span></span>

<span data-ttu-id="b4e30-104">La résilience est la capacité d’une application à effectuer une récupération normale à partir de situations dans lesquelles un composant vital est manquant ou a été remplacée par une version incompatible.</span><span class="sxs-lookup"><span data-stu-id="b4e30-104">Resiliency is the ability of an application to recover gracefully from situations in which a vital component is missing, or has been replaced by an incompatible version.</span></span> <span data-ttu-id="b4e30-105">En créant un package d’installation et en utilisant les [fonctions du programme](installer-functions.md)d’installation, les développeurs peuvent utiliser le Windows Installer pour produire des applications résilientes capables de récupérer à partir de ces situations.</span><span class="sxs-lookup"><span data-stu-id="b4e30-105">By authoring an installation package and using the [Installer Functions](installer-functions.md), developers can use the Windows Installer to produce resilient applications capable of recovering from such situations.</span></span>

-   <span data-ttu-id="b4e30-106">Utilisez la liste source du programme d’installation pour augmenter la résilience des applications qui reposent sur les ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="b4e30-106">Use the installer's source list to increase the resiliency of applications that rely on network resources.</span></span> <span data-ttu-id="b4e30-107">Pour plus d’informations, consultez [résilience source](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="b4e30-107">For more information, see [Source Resiliency](source-resiliency.md).</span></span>
-   <span data-ttu-id="b4e30-108">Utilisez l’API du programme d’installation pour vérifier si une fonctionnalité, un composant, un fichier ou une version de fichier critique est installé.</span><span class="sxs-lookup"><span data-stu-id="b4e30-108">Use the installer's API to check whether a vital feature, component, file, or file version is installed.</span></span>
-   <span data-ttu-id="b4e30-109">Utilisez l’API du programme d’installation pour vérifier le chemin d’accès à un composant au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b4e30-109">Use the installer's API to check the path to a component at run time.</span></span> <span data-ttu-id="b4e30-110">Cela réduit la dépendance de votre application vis-à-vis des chemins d’accès de fichiers statiques, qui sont souvent différents entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="b4e30-110">This reduces your application's dependency on static file paths, which commonly differ between computers.</span></span>
-   <span data-ttu-id="b4e30-111">Utilisez le programme d’installation pour réinstaller des raccourcis endommagés, des entrées de Registre et d’autres composants sans avoir à réexécuter l’installation.</span><span class="sxs-lookup"><span data-stu-id="b4e30-111">Use the installer to reinstall damaged shortcuts, registry entries, and other components without having to rerun setup.</span></span>
-   <span data-ttu-id="b4e30-112">Augmentez la résilience de l’installation de votre produit en laissant la fonctionnalité d’annulation du programme d’installation activée.</span><span class="sxs-lookup"><span data-stu-id="b4e30-112">Increase the resiliency of your product's installation by leaving the rollback capability of the installer enabled.</span></span> <span data-ttu-id="b4e30-113">Pour plus d’informations, consultez [restauration de l’installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="b4e30-113">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



