---
title: Qu’est-ce que le modèle objet de point de contrôle ?
description: L’illustration suivante montre le modèle d’objet de point de contrôle de base.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e491d3ec89b1074fb09a9f7632a886fb67b59863
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311362"
---
# <a name="what-is-the-control-point-object-model"></a><span data-ttu-id="433fc-103">Qu’est-ce que le modèle objet de point de contrôle ?</span><span class="sxs-lookup"><span data-stu-id="433fc-103">What is the Control Point Object Model?</span></span>

<span data-ttu-id="433fc-104">L’illustration suivante montre le modèle d’objet de point de contrôle de base.</span><span class="sxs-lookup"><span data-stu-id="433fc-104">The following illustration shows the basic Control Point object model.</span></span>

![modèle d’objet de point de contrôle](images/upnp-object-model.png)

<span data-ttu-id="433fc-106">La recherche d’appareils avec l’interface de recherche d’appareils crée un regroupement de périphériques.</span><span class="sxs-lookup"><span data-stu-id="433fc-106">Searching for devices with the Device Finder interface creates a Devices collection.</span></span> <span data-ttu-id="433fc-107">Une collection Devices contient zéro ou plusieurs objets Device.</span><span class="sxs-lookup"><span data-stu-id="433fc-107">A Devices collection contains zero or more Device objects.</span></span> <span data-ttu-id="433fc-108">Les applications peuvent utiliser les différentes méthodes de collecte des appareils pour accéder à des objets d’appareil individuels.</span><span class="sxs-lookup"><span data-stu-id="433fc-108">Applications can use the various Devices collection methods to access individual Device objects.</span></span>

<span data-ttu-id="433fc-109">Les objets périphérique contiennent toujours une collection de services qui contient un ou plusieurs objets de service.</span><span class="sxs-lookup"><span data-stu-id="433fc-109">Device objects always contain a Services collection that contains one or more Service objects.</span></span> <span data-ttu-id="433fc-110">Ces objets de service sont utilisés par les applications pour communiquer avec et contrôler les appareils.</span><span class="sxs-lookup"><span data-stu-id="433fc-110">These service objects are used by applications to communicate with and control devices.</span></span>

 

 




