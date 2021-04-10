---
description: Les assemblys privés côte à côte peuvent être utilisés pour créer des composants qui peuvent être facilement mis à jour sans mettre à jour également l’application d’hébergement.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Mise à jour des composants d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951094"
---
# <a name="updating-application-components"></a><span data-ttu-id="05fce-103">Mise à jour des composants d’application</span><span class="sxs-lookup"><span data-stu-id="05fce-103">Updating Application Components</span></span>

<span data-ttu-id="05fce-104">Les assemblys privés côte à côte peuvent être utilisés pour créer des composants qui peuvent être facilement mis à jour sans mettre à jour également l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="05fce-104">Side-by-side private assemblies can be used to create components that can be easily updated without also updating the hosting application.</span></span> <span data-ttu-id="05fce-105">Cela permet à un service de mise à jour d’installer les composants mis à jour de l’application, de redémarrer l’application et de faire en sorte que l’application utilise les modifications.</span><span class="sxs-lookup"><span data-stu-id="05fce-105">This allows an updating service to install the application's updated components, restart the application, and have the application use the changes.</span></span> <span data-ttu-id="05fce-106">Lors de l’utilisation de manifestes d’application, les fonctionnalités des composants hébergés par une application peuvent être mises à jour sans avoir à modifier le code de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="05fce-106">When using application manifests, the functionality of components hosted by an application can be updated without having to change the hosting application's code.</span></span>

<span data-ttu-id="05fce-107">Cette méthode peut être utilisée pour mettre à jour la version des ressources d’une application.</span><span class="sxs-lookup"><span data-stu-id="05fce-107">This method can be used to update the version of an application's resources.</span></span> <span data-ttu-id="05fce-108">Par exemple, si une application contient un assembly, le manifeste de l’application peut spécifier une dépendance sur cet assembly.</span><span class="sxs-lookup"><span data-stu-id="05fce-108">For example, if an application contains an assembly, the application's manifest can specify a dependency on this assembly.</span></span> <span data-ttu-id="05fce-109">L’application peut obtenir l’assembly en appelant [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) pour rechercher et charger les fichiers dont il a besoin.</span><span class="sxs-lookup"><span data-stu-id="05fce-109">The application can get the assembly by calling [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) to find and load the files it requires.</span></span> <span data-ttu-id="05fce-110">Un programme de mise à jour doit simplement mettre en avant les derniers bits de l’assembly, qui peuvent exister côte à côte avec une version antérieure de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="05fce-110">An updater simply has to bring down the newest bits for the assembly, which can exist side-by-side with an earlier version of the assembly.</span></span>

 

 
