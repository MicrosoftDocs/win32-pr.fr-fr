---
description: La préparation des ressources pour une application MUI prend en charge les modèles PE Win32 et non Win32.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Préparation des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536598"
---
# <a name="preparing-resources"></a><span data-ttu-id="76899-103">Préparation des ressources</span><span class="sxs-lookup"><span data-stu-id="76899-103">Preparing Resources</span></span>

<span data-ttu-id="76899-104">La préparation des ressources pour une application MUI prend en charge les modèles PE Win32 et non Win32.</span><span class="sxs-lookup"><span data-stu-id="76899-104">Resource preparation for a MUI application supports both Win32 PE and non-Win32 PE models.</span></span> <span data-ttu-id="76899-105">Les ressources Win32 PE sont fournies dans des fichiers PE, tels que des fichiers. dll,. exe ou. sys.</span><span class="sxs-lookup"><span data-stu-id="76899-105">Win32 PE resources are provided in PE-based files, such as .dll, .exe, or .sys files.</span></span> <span data-ttu-id="76899-106">Les ressources PE non Win32 sont fournies dans un module personnalisé de votre choix.</span><span class="sxs-lookup"><span data-stu-id="76899-106">Non-Win32 PE resources are furnished in a customized module of your choosing.</span></span>

> [!Note]  
> <span data-ttu-id="76899-107">Il est fortement recommandé d’utiliser des ressources Win32 PE pour les applications MUI Win32, car ces ressources sont entièrement prises en charge par la technologie de ressources MUI.</span><span class="sxs-lookup"><span data-stu-id="76899-107">It is highly recommended for you to use Win32 PE resources for Win32 MUI applications, as these resources are completely supported by the MUI resource technology.</span></span> <span data-ttu-id="76899-108">Les fichiers de ressources PE non Win32 peuvent être localisés en appelant la fonction [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) , comme décrit dans [recherche de ressources PE non Win32](locating-non-win32-pe-resources.md), mais l’application doit fournir ses propres fonctionnalités pour rechercher et charger les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="76899-108">Non-Win32 PE resource files can be located by calling the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function as described in [Locating Non-Win32 PE Resources](locating-non-win32-pe-resources.md), but the application must provide its own functionality to find and load the required resources.</span></span>

 

<span data-ttu-id="76899-109">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="76899-109">This section contains the following topics:</span></span>

-   [<span data-ttu-id="76899-110">Création du fichier de ressources de la langue de base</span><span class="sxs-lookup"><span data-stu-id="76899-110">Creating the Base Language Resource File</span></span>](creating-the-base-language-resource-file.md)
-   [<span data-ttu-id="76899-111">Utilisation de la redirection de chaînes de Registre</span><span class="sxs-lookup"><span data-stu-id="76899-111">Using Registry String Redirection</span></span>](using-registry-string-redirection.md)
-   [<span data-ttu-id="76899-112">Préparation d’un fichier de configuration de ressource</span><span class="sxs-lookup"><span data-stu-id="76899-112">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)

 

 



