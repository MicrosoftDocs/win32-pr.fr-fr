---
description: L’exécution automatique est une fonctionnalité du système d’exploitation Windows.
title: Création d’une application de CD-ROM compatible avec l’exécution automatique
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201282"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a><span data-ttu-id="995bc-103">Création d’une application de CD-ROM compatible avec l’exécution automatique</span><span class="sxs-lookup"><span data-stu-id="995bc-103">Creating an AutoRun-enabled CD-ROM Application</span></span>

<span data-ttu-id="995bc-104">L’exécution automatique est une fonctionnalité du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="995bc-104">AutoRun is a feature of the Windows operating system.</span></span> <span data-ttu-id="995bc-105">Il automatise les procédures d’installation et de configuration des produits conçus pour les plateformes Windows distribuées sur les CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="995bc-105">It automates the procedures for installing and configuring products designed for Windows-based platforms that are distributed on CD-ROMs.</span></span> <span data-ttu-id="995bc-106">Quand les utilisateurs insèrent un disque compact à extension automatique dans leur lecteur de CD-ROM, l’exécution automatique exécute automatiquement une application sur le CD-ROM qui installe, configure ou exécute le produit sélectionné.</span><span class="sxs-lookup"><span data-stu-id="995bc-106">When users insert an AutoRun-enabled compact disc into their CD-ROM drive, AutoRun automatically runs an application on the CD-ROM that installs, configures, or runs the selected product.</span></span>

<span data-ttu-id="995bc-107">L’exécution automatique peut être utilisée pour installer et exécuter des applications de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="995bc-107">AutoRun can be used to install and run CD-ROM applications.</span></span> <span data-ttu-id="995bc-108">Bien que l’exécution automatique soit le plus souvent utilisée pour les applications Windows, elle peut également être utilisée pour installer, configurer ou exécuter des applications MS-DOS dans une session Microsoft MS-DOS Windows.</span><span class="sxs-lookup"><span data-stu-id="995bc-108">Although AutoRun is most commonly used for Windows applications, it can also be used to install, configure, or run MS-DOS-based applications in a Windows Microsoft MS-DOS session.</span></span> <span data-ttu-id="995bc-109">Vous pouvez configurer chaque application ms-dos avec une icône unique, un fichier Config.sys et un fichier Autoexec.bat.</span><span class="sxs-lookup"><span data-stu-id="995bc-109">You can configure each MS-DOS-based application with its own unique icon, Config.sys file, and Autoexec.bat file.</span></span> <span data-ttu-id="995bc-110">Windows crée les fichiers de configuration corrects pour l’application ms-dos.</span><span class="sxs-lookup"><span data-stu-id="995bc-110">Windows creates the correct configuration files for the MS-DOS-based application.</span></span> <span data-ttu-id="995bc-111">L’application de démarrage démarre ensuite l’application ms-dos dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="995bc-111">The startup application then starts the MS-DOS-based application in a window.</span></span>

> [!Note]  
> <span data-ttu-id="995bc-112">Pour que l’exécution automatique fonctionne, le lecteur de CD-ROM doit avoir des pilotes de périphérique 32 ou 64 bits qui détectent quand un utilisateur insère un CD-ROM et notifie le système.</span><span class="sxs-lookup"><span data-stu-id="995bc-112">For AutoRun to work, the CD-ROM drive must have 32 or 64-bit device drivers that detect when a user inserts a compact disc and notify the system.</span></span>

 

<span data-ttu-id="995bc-113">Les sections suivantes expliquent comment implémenter une application de CD-ROM activée pour l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="995bc-113">The following sections discuss how to implement an AutoRun-enabled CD-ROM application.</span></span>

-   [<span data-ttu-id="995bc-114">Création d’une application AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="995bc-114">Creating an AutoRun-Enabled Application</span></span>](autoplay-works.md)
-   [<span data-ttu-id="995bc-115">Entrées autorun. inf</span><span class="sxs-lookup"><span data-stu-id="995bc-115">Autorun.inf Entries</span></span>](autorun-cmds.md)
-   [<span data-ttu-id="995bc-116">Activation et désactivation de l’exécution automatique</span><span class="sxs-lookup"><span data-stu-id="995bc-116">Enabling and Disabling AutoRun</span></span>](autoplay-reg.md)

 

 



