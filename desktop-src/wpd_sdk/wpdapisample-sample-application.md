---
description: Application WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Application WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751181"
---
# <a name="wpdapisample-application"></a><span data-ttu-id="350cb-103">Application WpdApiSample</span><span class="sxs-lookup"><span data-stu-id="350cb-103">WpdApiSample Application</span></span>

<span data-ttu-id="350cb-104">L’exemple d’application WpdApiSample est une application de bureau en ligne de commande qui vous permet d’énumérer des appareils connectés, d’explorer des appareils, de rechercher des propriétés et des attributs, d’envoyer et de récupérer des objets, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="350cb-104">The WpdApiSample sample application is a command-line desktop application that enables you to enumerate connected devices, explore devices, query objects for properties and attributes, send and retrieve objects, and so on.</span></span> <span data-ttu-id="350cb-105">Au démarrage, l’application ouvre une fenêtre de commande qui répertorie les tâches que vous pouvez effectuer.</span><span class="sxs-lookup"><span data-stu-id="350cb-105">On startup, the application opens a command window that lists the tasks you can perform.</span></span>

<span data-ttu-id="350cb-106">L’exemple d’application WpdApiSample comprend les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="350cb-106">The WpdApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="350cb-107">**File**</span><span class="sxs-lookup"><span data-stu-id="350cb-107">**File**</span></span>               | <span data-ttu-id="350cb-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="350cb-108">**Description**</span></span>                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="350cb-109">ContentEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="350cb-109">ContentEnumeration.cpp</span></span> | <span data-ttu-id="350cb-110">Contient des fonctions qui énumèrent tous les objets sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="350cb-110">Contains functions that enumerate all the objects on a device.</span></span>                                                                                                                                            |
| <span data-ttu-id="350cb-111">ContentProperties. cpp</span><span class="sxs-lookup"><span data-stu-id="350cb-111">ContentProperties.cpp</span></span>  | <span data-ttu-id="350cb-112">Contient des fonctions qui lisent et écrivent des propriétés d’objet et effectuent des requêtes de jeu de propriétés en bloc.</span><span class="sxs-lookup"><span data-stu-id="350cb-112">Contains functions that read and write object properties and make bulk property set/get requests.</span></span>                                                                                                         |
| <span data-ttu-id="350cb-113">ContentTransfer. cpp</span><span class="sxs-lookup"><span data-stu-id="350cb-113">ContentTransfer.cpp</span></span>    | <span data-ttu-id="350cb-114">Contient des fonctions qui transfèrent du contenu vers ou à partir de l’appareil, lisent les exigences de type d’objet et créent un dossier sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="350cb-114">Contains functions that transfer content to or from the device, read object type requirements, and create a folder on the device.</span></span>                                                                         |
| <span data-ttu-id="350cb-115">DeviceCapabilities. cpp</span><span class="sxs-lookup"><span data-stu-id="350cb-115">DeviceCapabilities.cpp</span></span> | <span data-ttu-id="350cb-116">Contient des fonctions permettant de répertorier les types d’objets fonctionnels sur l’appareil, de répertorier les types de contenu pris en charge par chaque type d’objet fonctionnel et d’afficher des profils d’objet de rendu.</span><span class="sxs-lookup"><span data-stu-id="350cb-116">Contains functions to list the functional object types on the device, list the content types supported by each functional object type, and display rendering object profiles.</span></span>                             |
| <span data-ttu-id="350cb-117">DeviceEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="350cb-117">DeviceEnumeration.cpp</span></span>  | <span data-ttu-id="350cb-118">Répertorie les noms conviviaux, les fabricants et les descriptions de tous les appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="350cb-118">Lists the friendly names, manufacturers, and descriptions of all connected devices.</span></span>                                                                                                                       |
| <span data-ttu-id="350cb-119">DeviceEvents. cpp</span><span class="sxs-lookup"><span data-stu-id="350cb-119">DeviceEvents.cpp</span></span>       | <span data-ttu-id="350cb-120">Contient des fonctions qui journalisent des événements de périphérique et leurs paramètres chaque fois que des événements sont déclenchés.</span><span class="sxs-lookup"><span data-stu-id="350cb-120">Contains functions that log device events and their parameters whenever events are fired.</span></span>                                                                                                                 |
| <span data-ttu-id="350cb-121">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="350cb-121">Stdafx.cpp</span></span>             | <span data-ttu-id="350cb-122">Comprend les fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="350cb-122">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="350cb-123">WpdApiSample. cpp</span><span class="sxs-lookup"><span data-stu-id="350cb-123">WpdApiSample.cpp</span></span>       | <span data-ttu-id="350cb-124">Héberge la fonction de démarrage **\_ tmain** , qui appelle la fonction de **menu contextuel** locale, qui affiche une liste des périphériques et des tâches disponibles et appelle la fonction appropriée pour la sélection de menu de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="350cb-124">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="350cb-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="350cb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="350cb-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="350cb-126">Sample</span></span>](sample.md)
</dt> </dl>

 

 



