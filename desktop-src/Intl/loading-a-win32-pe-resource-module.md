---
description: Cette rubrique décrit comment l’application charge un module de ressources Win32 PE sur Windows Vista et versions ultérieures, ou sur un système d’exploitation antérieur. Des appels sont inclus pour libérer le module de ressources.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Chargement d’un module de ressources Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c4c1906a4fc09dc39b805e8ad5a875d96fae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529482"
---
# <a name="loading-a-win32-pe-resource-module"></a><span data-ttu-id="28887-104">Chargement d’un module de ressources Win32 PE</span><span class="sxs-lookup"><span data-stu-id="28887-104">Loading a Win32 PE Resource Module</span></span>

<span data-ttu-id="28887-105">Cette rubrique décrit comment l’application charge un module de ressources Win32 PE sur Windows Vista et versions ultérieures, ou sur un système d’exploitation antérieur.</span><span class="sxs-lookup"><span data-stu-id="28887-105">This topic describes how the application loads a Win32 PE resource module on either Windows Vista and later or on an earlier operating system.</span></span> <span data-ttu-id="28887-106">Des appels sont inclus pour libérer le module de ressources.</span><span class="sxs-lookup"><span data-stu-id="28887-106">Calls are included for releasing the resource module.</span></span>

## <a name="load-the-resource-module-on-windows-vista-and-later"></a><span data-ttu-id="28887-107">Charger le module de ressources sur Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="28887-107">Load the Resource Module on Windows Vista and Later</span></span>

<span data-ttu-id="28887-108">Sur Windows Vista et versions ultérieures, l’application charge le module de ressources à l’aide d’un appel à [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="28887-108">On Windows Vista and later, the application loads the resource module using a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span> <span data-ttu-id="28887-109">L’opération recommandée consiste à appeler cette fonction avec les deux indicateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="28887-109">The recommended operation is to call this function with both flags specified.</span></span> <span data-ttu-id="28887-110">Voici un exemple de code d’application qui charge un module en fonction des paramètres de langue du système.</span><span class="sxs-lookup"><span data-stu-id="28887-110">The following is an example of application code that loads a module based on system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="28887-111">Charger le module de ressources sur les systèmes d’exploitation antérieurs à Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28887-111">Load the Resource Module on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="28887-112">Sur les systèmes d’exploitation antérieurs à Windows Vista, l’application charge un module de ressources en fonction d’un paramètre de langue qui est compatible avec le système d’exploitation cible, ainsi que Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="28887-112">On pre-Windows Vista operating systems, the application loads a resource module based on a language setting that is compatible with the target operating system, as well as Windows Vista and later.</span></span> <span data-ttu-id="28887-113">Pour ce type de chargement de module, l’application doit appeler les fonctions MUI [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span><span class="sxs-lookup"><span data-stu-id="28887-113">For this type of module loading, the application must call the MUI functions [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span></span>


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="28887-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28887-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28887-115">Recherche de ressources Win32 PE</span><span class="sxs-lookup"><span data-stu-id="28887-115">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> <dt>

[<span data-ttu-id="28887-116">MUI : exemple de paramètres Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="28887-116">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="28887-117">MUI : exemple de paramètres de Application-Specific (antérieur à Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="28887-117">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
