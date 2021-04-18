---
description: Après avoir créé un fichier INF, vous allez généralement écrire le code source de votre application d’installation. Vous appelez les fonctions d’installation à partir de votre application d’installation pour effectuer de nombreuses opérations d’installation.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Création d’applications d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536387"
---
# <a name="creating-setup-applications"></a><span data-ttu-id="ec944-104">Création d’applications d’installation</span><span class="sxs-lookup"><span data-stu-id="ec944-104">Creating Setup Applications</span></span>

<span data-ttu-id="ec944-105">Après avoir créé un fichier INF, vous allez généralement écrire le code source de votre application d’installation.</span><span class="sxs-lookup"><span data-stu-id="ec944-105">After you create an INF file, you will typically write the source code for your setup application.</span></span> <span data-ttu-id="ec944-106">Vous appelez les fonctions d’installation à partir de votre application d’installation pour effectuer de nombreuses opérations d’installation.</span><span class="sxs-lookup"><span data-stu-id="ec944-106">You call the setup functions from your setup application to perform many installation operations.</span></span>

<span data-ttu-id="ec944-107">Les étapes suivantes décrivent une façon d’utiliser les fonctions de configuration pour créer une application d’installation.</span><span class="sxs-lookup"><span data-stu-id="ec944-107">The following steps cover one way to use the setup functions to create a setup application.</span></span> <span data-ttu-id="ec944-108">Vous pouvez utiliser cet exemple comme point de départ ou développer votre propre algorithme d’installation.</span><span class="sxs-lookup"><span data-stu-id="ec944-108">You can use this example as a starting point, or develop your own installation algorithm.</span></span>

<span data-ttu-id="ec944-109">**D’initialisation**</span><span class="sxs-lookup"><span data-stu-id="ec944-109">**Initialization**</span></span>

-   [<span data-ttu-id="ec944-110">Ouvrez le fichier INF et, le cas échéant, ajoutez d’autres fichiers INF.</span><span class="sxs-lookup"><span data-stu-id="ec944-110">Open the INF and, if appropriate, append other INF files.</span></span>](opening-the-inf-file.md)
-   [<span data-ttu-id="ec944-111">Extrayez les informations de fichier à partir du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="ec944-111">Extract file information from the INF file.</span></span>](extracting-file-information-from-the-inf-file.md)
-   [<span data-ttu-id="ec944-112">Rassemblez les informations d’installation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec944-112">Gather setup information from the user.</span></span>](gathering-setup-information-from-the-user.md)
-   [<span data-ttu-id="ec944-113">Créez une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ec944-113">Create a queue.</span></span>](creating-a-queue-and-queuing-file-operations.md)

<span data-ttu-id="ec944-114">**Fichiers d’installation**</span><span class="sxs-lookup"><span data-stu-id="ec944-114">**Install files**</span></span>

-   [<span data-ttu-id="ec944-115">Validez la file d’attente, en spécifiant une routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="ec944-115">Commit the queue, specifying a callback routine.</span></span>](committing-the-queue.md)
-   [<span data-ttu-id="ec944-116">Mettre à jour les informations du Registre.</span><span class="sxs-lookup"><span data-stu-id="ec944-116">Update registry information.</span></span>](updating-registry-information.md)

<span data-ttu-id="ec944-117">**Nettoyage**</span><span class="sxs-lookup"><span data-stu-id="ec944-117">**Clean up**</span></span>

-   [<span data-ttu-id="ec944-118">Fermez la file d’attente de fichiers et le fichier INF.</span><span class="sxs-lookup"><span data-stu-id="ec944-118">Close the file queue and INF.</span></span>](closing-the-file-queue-and-inf-file.md)
-   [<span data-ttu-id="ec944-119">Libérez toutes les autres ressources système et mettez fin au programme.</span><span class="sxs-lookup"><span data-stu-id="ec944-119">Release any other system resources and end the program.</span></span>](releasing-other-system-resources.md)

 

 



