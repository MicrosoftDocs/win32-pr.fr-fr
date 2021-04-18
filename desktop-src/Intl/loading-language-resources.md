---
description: Chargement des ressources de langue
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Chargement des ressources de langue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6917f03e773a470288fb4c9577812e0b38868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321098"
---
# <a name="loading-language-resources"></a><span data-ttu-id="e96ba-103">Chargement des ressources de langue</span><span class="sxs-lookup"><span data-stu-id="e96ba-103">Loading Language Resources</span></span>

<span data-ttu-id="e96ba-104">Votre application charge toutes les ressources de la langue de l’interface utilisateur, à l’exception de certaines chaînes de Registre redirigées, à l’aide d’appels aux fonctions de chargement de ressources standard, par exemple, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)et [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span><span class="sxs-lookup"><span data-stu-id="e96ba-104">Your application loads all user interface language resources, other than certain redirected registry strings, using calls to standard resource loading functions, for example, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), and [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span></span> <span data-ttu-id="e96ba-105">De nombreuses fonctions de chargement des ressources ont été modifiées pour charger automatiquement des ressources à partir de fichiers de ressources spécifiques à une langue, en traitant les ressources comme si elles étaient contenues dans le fichier LN.</span><span class="sxs-lookup"><span data-stu-id="e96ba-105">Many resource loading functions have been modified to load resources from language-specific resource files automatically, treating resources as if they are contained in the LN file.</span></span> <span data-ttu-id="e96ba-106">L’exemple suivant illustre l’utilisation de **LoadString** pour charger des chaînes de langue pour une application qui suit les paramètres de langue système.</span><span class="sxs-lookup"><span data-stu-id="e96ba-106">The following example illustrates the use of **LoadString** to load language strings for an application that follows system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="e96ba-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e96ba-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e96ba-108">Recherche de ressources Win32 PE</span><span class="sxs-lookup"><span data-stu-id="e96ba-108">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> </dl>

 

 
