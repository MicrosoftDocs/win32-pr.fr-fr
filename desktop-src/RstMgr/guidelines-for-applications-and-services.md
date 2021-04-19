---
title: Instructions pour les applications et les services
description: Pour réduire le nombre de redémarrages du système lors de l’installation et de la maintenance des applications sur Windows Vista ou Windows Server 2008, vous devez respecter les consignes suivantes pour permettre à votre application ou service d’être arrêté correctement et redémarré.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510603"
---
# <a name="guidelines-for-applications-and-services"></a><span data-ttu-id="8f8fe-103">Instructions pour les applications et les services</span><span class="sxs-lookup"><span data-stu-id="8f8fe-103">Guidelines for Applications and Services</span></span>

<span data-ttu-id="8f8fe-104">Pour réduire le nombre de redémarrages du système lors de l’installation et de la maintenance des applications sur Windows Vista ou Windows Server 2008, vous devez respecter les consignes suivantes pour permettre à votre application ou service d’être arrêté correctement et redémarré.</span><span class="sxs-lookup"><span data-stu-id="8f8fe-104">To reduce the number of system restarts when installing and servicing applications on Windows Vista or Windows Server 2008, you should observe the following guidelines to enable your application or service to be shut down cleanly and restarted.</span></span>

-   <span data-ttu-id="8f8fe-105">Vos applications et services doivent être prêts à être arrêtés et redémarrés par le système lorsque cela est nécessaire pour installer une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8f8fe-105">Your applications and services should be prepared to be shut down and restarted by the system when this is necessary to install an update.</span></span> <span data-ttu-id="8f8fe-106">En général, lorsqu’une mise à jour est installée, une application ou un service doit être arrêté, car il contient actuellement un fichier affecté en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8f8fe-106">Typically, when an update is installed, an application or service needs to be shut down because it currently holds an affected file in use.</span></span> <span data-ttu-id="8f8fe-107">Toutes les applications ou tous les services qui peuvent contenir un fichier en cours d’utilisation pendant une mise à jour doivent être prêts à s’arrêter correctement.</span><span class="sxs-lookup"><span data-stu-id="8f8fe-107">All applications or services that can hold a file in use during an update should be prepared to shut down cleanly.</span></span>
-   <span data-ttu-id="8f8fe-108">Vos applications doivent enregistrer les données utilisateur et les informations d’État nécessaires après un redémarrage. elles doivent respecter les instructions décrites dans la section [instructions pour les applications](guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8f8fe-108">Your applications should save user data and state information that are needed after a restart and should adhere to the guidelines that are described in the section [Guidelines for Applications](guidelines-for-applications.md).</span></span>
-   <span data-ttu-id="8f8fe-109">Vos services doivent respecter les instructions décrites dans la section [instructions pour les services](guidelines-for-services.md).</span><span class="sxs-lookup"><span data-stu-id="8f8fe-109">Your services should adhere to the guidelines that are described in the section [Guidelines for Services](guidelines-for-services.md).</span></span>
-   <span data-ttu-id="8f8fe-110">Le gestionnaire de redémarrage n’arrête pas les [services système critiques](critical-system-services.md); par conséquent, ces services doivent limiter le nombre de dll dont ils dépendent.</span><span class="sxs-lookup"><span data-stu-id="8f8fe-110">Restart Manager does not shut down [critical system services](critical-system-services.md); therefore, these services should limit the number of DLLs they depend on.</span></span>

 

 




