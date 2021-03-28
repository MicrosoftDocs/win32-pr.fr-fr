---
description: La plupart des extensions d’espace de noms sont un sous-ensemble de l’espace de noms Shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Affichage d’une vue Self-Contained d’une extension d’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973375"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a><span data-ttu-id="f6c70-103">Affichage d’une vue Self-Contained d’une extension d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="f6c70-103">Displaying a Self-Contained View of a Namespace Extension</span></span>

<span data-ttu-id="f6c70-104">La plupart des extensions d’espace de noms sont un sous-ensemble de l’espace de noms Shell.</span><span class="sxs-lookup"><span data-stu-id="f6c70-104">Most namespace extensions are a subset of the Shell namespace.</span></span> <span data-ttu-id="f6c70-105">Lorsque vous créez un point de jonction, comme décrit dans [spécification de l’emplacement d’une extension d’espace de noms, l'](nse-junction.md)Explorateur Windows permet aux utilisateurs de naviguer vers et à partir de votre extension d’espace de noms comme n’importe quel autre dossier.</span><span class="sxs-lookup"><span data-stu-id="f6c70-105">When you create a junction point, as described in [Specifying a Namespace Extension's Location](nse-junction.md), Windows Explorer allows users to navigate into and out of your namespace extension just like any other folder.</span></span> <span data-ttu-id="f6c70-106">Toutefois, il est également possible d’utiliser l’Explorateur Windows pour afficher uniquement le contenu de votre extension d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="f6c70-106">However, it is also possible to use Windows Explorer to display only the contents of your namespace extension.</span></span> <span data-ttu-id="f6c70-107">Cette option d’affichage est parfois appelée vue avec *racine*.</span><span class="sxs-lookup"><span data-stu-id="f6c70-107">This display option is sometimes referred to as a *rooted view*.</span></span> <span data-ttu-id="f6c70-108">Bien qu’elles ne soient pas couramment utilisées, les vues avec racine peuvent être préférables à des vues normales pour certains types d’extensions.</span><span class="sxs-lookup"><span data-stu-id="f6c70-108">Although not commonly used, rooted views might be preferable to normal views for some types of extensions.</span></span>

<span data-ttu-id="f6c70-109">Avec une vue avec racine, une nouvelle instance de l’Explorateur Windows est créée, qui affiche le contenu de l’extension sous la forme d’un espace de noms distinct.</span><span class="sxs-lookup"><span data-stu-id="f6c70-109">With a rooted view, a new instance of Windows Explorer is created that displays the contents of the extension as a separate namespace.</span></span> <span data-ttu-id="f6c70-110">L’arborescence d’une vue racine affiche uniquement les dossiers qui font partie de l’extension.</span><span class="sxs-lookup"><span data-stu-id="f6c70-110">The tree view of a rooted view shows only those folders that are part of the extension.</span></span> <span data-ttu-id="f6c70-111">Les utilisateurs ne peuvent pas naviguer d’une vue enracinée vers d’autres parties de l’espace de noms Shell.</span><span class="sxs-lookup"><span data-stu-id="f6c70-111">Users cannot navigate from a rooted view to other parts of the Shell namespace.</span></span>

<span data-ttu-id="f6c70-112">Les extensions sont implémentées de la même façon pour les vues enracinées qu’elles le sont pour les vues normales.</span><span class="sxs-lookup"><span data-stu-id="f6c70-112">Extensions are implemented in the same way for rooted views as they are for normal views.</span></span> <span data-ttu-id="f6c70-113">La seule différence réside dans le mode d’affichage du contenu de l’extension par l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="f6c70-113">The only difference is in the way the contents of the extension are displayed by Windows Explorer.</span></span> <span data-ttu-id="f6c70-114">Il est même possible d’avoir des vues normales et enracinées de la même extension.</span><span class="sxs-lookup"><span data-stu-id="f6c70-114">It is even possible to have normal and rooted views of the same extension.</span></span>

<span data-ttu-id="f6c70-115">Pour ouvrir une vue d’une extension, vous devez lancer une instance de Explorer.exe avec un indicateur/root.</span><span class="sxs-lookup"><span data-stu-id="f6c70-115">To open a view of an extension, you must launch an instance of Explorer.exe with a /root flag.</span></span> <span data-ttu-id="f6c70-116">Il existe plusieurs façons de lancer une vue avec racine, en fonction de la nature de votre extension.</span><span class="sxs-lookup"><span data-stu-id="f6c70-116">There are several different ways to launch a rooted view, depending on the nature of your extension.</span></span>

-   [<span data-ttu-id="f6c70-117">Comment utiliser un point de jonction pour ouvrir une vue enracinée</span><span class="sxs-lookup"><span data-stu-id="f6c70-117">How To Use a Junction Point to Open a Rooted View</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [<span data-ttu-id="f6c70-118">Comment utiliser un fichier de raccourci pour ouvrir une vue avec racine</span><span class="sxs-lookup"><span data-stu-id="f6c70-118">How To Use a Shortcut File to Open a Rooted View</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [<span data-ttu-id="f6c70-119">Comment afficher une vue enracinée d’un fichier</span><span class="sxs-lookup"><span data-stu-id="f6c70-119">How To Display a Rooted View of a File</span></span>](how-to-display-a-rooted-view-of-a-file.md)

 

 



