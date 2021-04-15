---
title: Exemple d’application de bureau
description: Exemple d’application de bureau
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Gestionnaire de périphériques Windows Media, exemples
- Gestionnaire de périphériques, exemples
- applications de bureau, exemples
- Windows Media Gestionnaire de périphériques, exemple d’application de bureau
- Gestionnaire de périphériques, exemple d’application de bureau
- exemple d’application wmdmapp
- exemples, applications de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379994"
---
# <a name="sample-desktop-application"></a><span data-ttu-id="538d1-110">Exemple d’application de bureau</span><span class="sxs-lookup"><span data-stu-id="538d1-110">Sample Desktop Application</span></span>

<span data-ttu-id="538d1-111">Le Gestionnaire de périphériques Windows Media est fourni avec un exemple d’application de bureau appelé wmdmapp.</span><span class="sxs-lookup"><span data-stu-id="538d1-111">The Windows Media Device Manager ships with a sample desktop application called wmdmapp.</span></span> <span data-ttu-id="538d1-112">Cette application possède une interface graphique utilisateur qui vous permet de parcourir les appareils connectés, de créer des sélections sur l’appareil et de faire glisser des fichiers multimédias vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="538d1-112">This application has a graphical user interface that allows you to browse connected devices, create playlists on the device, and drag media files to the device.</span></span>

<span data-ttu-id="538d1-113">Cet exemple d’application se compose de deux éléments :</span><span class="sxs-lookup"><span data-stu-id="538d1-113">This sample application consists of two pieces:</span></span>

-   <span data-ttu-id="538d1-114">wmdapp.exe, un fichier exécutable qui affiche une fenêtre et effectue la plupart de l’interface utilisateur et des fonctionnalités de base du programme, et</span><span class="sxs-lookup"><span data-stu-id="538d1-114">wmdapp.exe, an executable that displays a window and performs most of the user interface and basic functionality of the program, and</span></span>
-   <span data-ttu-id="538d1-115">proghelp.dll, DLL d’assistance qui exécute des fonctions utilitaires pour l’application.</span><span class="sxs-lookup"><span data-stu-id="538d1-115">proghelp.dll, a helper DLL that performs utility functions for the application.</span></span> <span data-ttu-id="538d1-116">Vous devez inscrire cette DLL après avoir généré le projet.</span><span class="sxs-lookup"><span data-stu-id="538d1-116">You must register this DLL after building the project.</span></span>

<span data-ttu-id="538d1-117">Pour compiler l’exemple d’application, vous pouvez utiliser Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="538d1-117">To compile the sample application, you can use Visual Studio.</span></span> <span data-ttu-id="538d1-118">La section suivante décrit comment procéder :</span><span class="sxs-lookup"><span data-stu-id="538d1-118">The following section describes how this is done:</span></span>

-   [<span data-ttu-id="538d1-119">Compilation de l’exemple d’application à l’aide de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="538d1-119">Compiling the Sample Application Using Visual Studio</span></span>](compiling-the-sample-application-using-visual-studio.md)

<span data-ttu-id="538d1-120">Après avoir compilé le projet, enregistrez le fichier proghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="538d1-120">After compiling the project, register the proghelp.dll file.</span></span> <span data-ttu-id="538d1-121">Pour inscrire cette DLL, ouvrez une invite de commandes et accédez au répertoire contenant cette DLL et tapez `regsvr32 proghelp.dll` .</span><span class="sxs-lookup"><span data-stu-id="538d1-121">To register this DLL, open a command prompt and browse to the directory containing this DLL and type `regsvr32 proghelp.dll`.</span></span>

 

 




