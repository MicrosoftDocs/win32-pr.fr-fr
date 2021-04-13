---
description: Pour utiliser le modèle de script WIA (Windows Image Acquisition), le fichier Wiascr.dll doit être installé et enregistré sur l’ordinateur.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Configuration de l’environnement de développement du modèle de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201485"
---
# <a name="setting-up-the-scripting-model-development-environment"></a><span data-ttu-id="7f264-103">Configuration de l’environnement de développement du modèle de script</span><span class="sxs-lookup"><span data-stu-id="7f264-103">Setting up the Scripting Model Development Environment</span></span>

<span data-ttu-id="7f264-104">Pour utiliser le modèle de script WIA (Windows Image Acquisition), le fichier Wiascr.dll doit être installé et enregistré sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f264-104">To use the Windows Image Acquisition (WIA) scripting model, you must have the file Wiascr.dll installed and registered on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="7f264-105">Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="7f264-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="7f264-106">Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="7f264-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="7f264-107">Copiez ce fichier à partir du kit de développement logiciel (SDK) WIA dans le répertoire *% windir%*/system32 (par exemple, c : \\ Windows \\ system32).</span><span class="sxs-lookup"><span data-stu-id="7f264-107">Copy this file from the WIA SDK into the *%windir%*/System32 (for example, c:\\windows\\System32) directory.</span></span> <span data-ttu-id="7f264-108">Sur la ligne de commande, accédez à ce répertoire, puis tapez **regsvr32 Wiascr.dll**.</span><span class="sxs-lookup"><span data-stu-id="7f264-108">At the command line, navigate to this directory, and type **regsvr32 Wiascr.dll**.</span></span>

<span data-ttu-id="7f264-109">Cela a pour conséquence d’entrer les informations nécessaires dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="7f264-109">This enters the necessary information in the system registry.</span></span>

<span data-ttu-id="7f264-110">Vous êtes maintenant prêt à utiliser le modèle de script WIA.</span><span class="sxs-lookup"><span data-stu-id="7f264-110">You are now ready to use the WIA scripting model.</span></span>

 

 
