---
title: Application de point de contrôle utilisateur générique
description: L’application de point de contrôle utilisateur générique (UCP) vous permet de découvrir des appareils, de contrôler ces appareils détectés et d’afficher les informations d’événement connexes, à l’aide d’une interface graphique.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104567646"
---
# <a name="generic-user-control-point-application"></a><span data-ttu-id="1a2d1-103">Application de point de contrôle utilisateur générique</span><span class="sxs-lookup"><span data-stu-id="1a2d1-103">Generic User Control Point Application</span></span>

<span data-ttu-id="1a2d1-104">L’application de point de contrôle utilisateur générique (UCP) vous permet de découvrir des appareils, de contrôler ces appareils détectés et d’afficher les informations d’événement connexes, à l’aide d’une interface graphique.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-104">The generic user control point (UCP) application allows you to discover devices, control those discovered devices, and view the related eventing information, all using a graphical interface.</span></span>

<span data-ttu-id="1a2d1-105">**Pour démarrer l’application générique UCP**</span><span class="sxs-lookup"><span data-stu-id="1a2d1-105">**To start the generic UCP application**</span></span>

1.  <span data-ttu-id="1a2d1-106">Créez et configurez \\ le \\ \\ \\ fichier d'devtype.txt netds UPnP GenericUCP CPP \\ (ou le \\ \\ fichierdevtype.txt VisualBasic) avec les informations de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-106">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\devtype.txt file (or the \\VisualBasic\\devtype.txt file) with device information.</span></span> <span data-ttu-id="1a2d1-107">Ce fichier vous permet de configurer les UCP génériques pour les recherches « Rechercher par type » et « recherche asynchrone ».</span><span class="sxs-lookup"><span data-stu-id="1a2d1-107">This file allows you to configure the generic UCP for the "find by type" and "async find" searches.</span></span> <span data-ttu-id="1a2d1-108">Chaque ligne du fichier doit contenir un type d’appareil et la description associée.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-108">Each line of the file must contain a device type and the related description.</span></span> <span data-ttu-id="1a2d1-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="1a2d1-109">For example:</span></span>

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    <span data-ttu-id="1a2d1-110">Cet exemple est destiné à un périphérique de lecteur multimédia fictif.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-110">This example is for a fictitious media player device.</span></span> <span data-ttu-id="1a2d1-111">Le « lecteur multimédia » à la fin de la deuxième ligne ne fait pas partie du type d’appareil. il est fourni à titre d’information dans l’application UCP générique.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-111">The "Media Player" at the end of the second line is not a part of the device type, it is for informational purposes in the Generic UCP application.</span></span> <span data-ttu-id="1a2d1-112">Il en va de même pour « tous les appareils racine » sur la première ligne.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-112">The same applies to "All Root Devices" in the first line.</span></span>

    <span data-ttu-id="1a2d1-113">Ajoutez une ligne qui contient le type et la description de votre appareil spécifique pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-113">Add a line that contains your specific device type and description for each device.</span></span>

2.  <span data-ttu-id="1a2d1-114">Créez et configurez \\ le \\ fichier d'udn.txt netds UPnP \\ GenericUCP \\ CPP \\ (ou le \\ \\ fichierudn.txt VisualBasic) avec des informations UDN pour vos appareils.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-114">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\udn.txt file (or the \\VisualBasic\\udn.txt file) with UDN information for your devices.</span></span> <span data-ttu-id="1a2d1-115">Ce fichier vous permet de configurer le UCP générique pour la recherche « Rechercher par UDN ».</span><span class="sxs-lookup"><span data-stu-id="1a2d1-115">This file allows you to configure the generic UCP for the "find by UDN" search.</span></span> <span data-ttu-id="1a2d1-116">Chaque ligne utilise la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="1a2d1-116">Each line uses the following form:</span></span>

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    <span data-ttu-id="1a2d1-117">Ajoutez une ligne qui contient vos UDN spécifiques pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-117">Add a line that contains your specific UDN for each device.</span></span>

3.  <span data-ttu-id="1a2d1-118">Exécutez GenericUCP.exe.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-118">Run GenericUCP.exe.</span></span> <span data-ttu-id="1a2d1-119">La fenêtre **UCP générique** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-119">The **Generic UCP** window appears.</span></span>

    ![fenêtre UCP générique](images/generic-ucp.png)

> [!Note]  
> <span data-ttu-id="1a2d1-121">Les fonctionnalités **afficher la présentation** et afficher le **service DESC.** ne sont pas implémentées dans l’exemple de code C++.</span><span class="sxs-lookup"><span data-stu-id="1a2d1-121">The **View Presentation** and **View Service Desc.** functionality is not implemented in the C++ sample code.</span></span>

 

 

 




