---
description: L’exemple suivant montre comment lancer un fichier HTML à la fin d’une installation.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Utilisation d’une action personnalisée pour lancer un fichier installé à la fin de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203769"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a><span data-ttu-id="3609c-103">Utilisation d’une action personnalisée pour lancer un fichier installé à la fin de l’installation</span><span class="sxs-lookup"><span data-stu-id="3609c-103">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>

<span data-ttu-id="3609c-104">L’exemple suivant montre comment lancer un fichier HTML à la fin d’une installation.</span><span class="sxs-lookup"><span data-stu-id="3609c-104">The following example illustrates how to launch an HTML file at the end of an installation.</span></span> <span data-ttu-id="3609c-105">Le programme d’installation installe le composant qui contient le fichier, puis publie un événement de contrôle à la fin de l’installation pour exécuter une action personnalisée qui ouvre le fichier.</span><span class="sxs-lookup"><span data-stu-id="3609c-105">The Installer installs the component that contains the file, and then publishes a control event at the end of the installation to run a custom action that opens the file.</span></span> <span data-ttu-id="3609c-106">Cette approche peut être utilisée pour lancer un didacticiel d’aide à la fin de la première installation d’une application.</span><span class="sxs-lookup"><span data-stu-id="3609c-106">This approach may be used to launch a help tutorial at the end of the first installation of an application.</span></span>

<span data-ttu-id="3609c-107">L’exemple doit respecter les spécifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="3609c-107">The sample must meet the following specifications.</span></span>

-   <span data-ttu-id="3609c-108">Le programme d’installation exécute l’action personnalisée uniquement si le niveau d' [*interface utilisateur complet*](f-gly.md) est utilisé pour installer une application.</span><span class="sxs-lookup"><span data-stu-id="3609c-108">The Installer executes the custom action only if the [*full UI*](f-gly.md) level is used to install an application.</span></span>
-   <span data-ttu-id="3609c-109">Le programme d’installation exécute l’action personnalisée uniquement si le composant qui contient le fichier HTML est installé pour s’exécuter localement sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3609c-109">The Installer executes the custom action only if the component that contains the HTML file is installed to run locally on the computer.</span></span>
-   <span data-ttu-id="3609c-110">L’action personnalisée s’exécute uniquement lors de la première installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="3609c-110">The custom action only runs on the first installation of the application.</span></span>
-   <span data-ttu-id="3609c-111">L’installation n’échoue pas si l’action personnalisée échoue.</span><span class="sxs-lookup"><span data-stu-id="3609c-111">The installation does not fail if the custom action fails.</span></span>

<span data-ttu-id="3609c-112">L’exemple comprend un composant hypothétique nommé Tutorial qui contrôle au moins une ressource, un fichier nommé tutorial.htm.</span><span class="sxs-lookup"><span data-stu-id="3609c-112">The sample includes a hypothetical component named Tutorial that controls at least one resource, a file named tutorial.htm.</span></span> <span data-ttu-id="3609c-113">L’identificateur de ce fichier dans la colonne fichier de la table file est Tutorial.</span><span class="sxs-lookup"><span data-stu-id="3609c-113">The identifier for this file in the File column of the File table is Tutorial.</span></span> <span data-ttu-id="3609c-114">La discussion suivante suppose que vous avez déjà créé les ressources requises par le didacticiel et que vous avez effectué toutes les entrées nécessaires dans les tables [Feature](feature-table.md), [Component](component-table.md), [file](file-table.md), [Directory](directory-table.md)et [FeatureComponents](featurecomponents-table.md) pour installer ce composant.</span><span class="sxs-lookup"><span data-stu-id="3609c-114">The following discussion assumes that you have already created the resources required by Tutorial, and have made all the necessary entries in the [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md), and [FeatureComponents](featurecomponents-table.md) tables to install this component.</span></span> <span data-ttu-id="3609c-115">Pour plus d’informations, consultez [un exemple d’installation](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="3609c-115">For more information, see [An Installation Example](an-installation-example.md).</span></span>

<span data-ttu-id="3609c-116">Les rubriques suivantes contiennent des informations sur la façon de créer des actions personnalisées requises et de les ajouter à un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="3609c-116">The following topics contain information about how to create required custom actions and add them to an installation package.</span></span>

-   [<span data-ttu-id="3609c-117">Création de l’action personnalisée de lancement</span><span class="sxs-lookup"><span data-stu-id="3609c-117">Authoring the Launch Custom Action</span></span>](authoring-the-launch-custom-action.md)
-   [<span data-ttu-id="3609c-118">Ajout d’un lancement aux tables CustomAction et binaires</span><span class="sxs-lookup"><span data-stu-id="3609c-118">Adding Launch to the CustomAction and Binary Tables</span></span>](adding-launch-to-the-customaction-and-binary-tables.md)
-   [<span data-ttu-id="3609c-119">Ajout d’un événement de contrôle à la fin de l’installation pour exécuter le lancement</span><span class="sxs-lookup"><span data-stu-id="3609c-119">Adding a Control Event at the End of the Installation to Run Launch</span></span>](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



