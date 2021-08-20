---
description: cette rubrique décrit comment l’application charge un module de ressources Win32 PE sur Windows Vista et versions ultérieures ou sur un système d’exploitation antérieur. Des appels sont inclus pour libérer le module de ressources.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Chargement d’un module de ressources Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: affcd1cf582d81aafd70f208531e03723ea44b314f92848f35dfd391f950b0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145841"
---
# <a name="loading-a-win32-pe-resource-module"></a>Chargement d’un module de ressources Win32 PE

cette rubrique décrit comment l’application charge un module de ressources Win32 PE sur Windows Vista et versions ultérieures ou sur un système d’exploitation antérieur. Des appels sont inclus pour libérer le module de ressources.

## <a name="load-the-resource-module-on-windows-vista-and-later"></a>charger le Module de ressources sur Windows Vista et versions ultérieures

sur Windows Vista et versions ultérieures, l’application charge le module de ressources à l’aide d’un appel à [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa). L’opération recommandée consiste à appeler cette fonction avec les deux indicateurs spécifiés. Voici un exemple de code d’application qui charge un module en fonction des paramètres de langue du système.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a>charger le Module de ressources sur les systèmes d’exploitation antérieurs à Windows Vista

sur les systèmes d’exploitation antérieurs à Windows Vista, l’application charge un module de ressources en fonction d’un paramètre de langue qui est compatible avec le système d’exploitation cible, ainsi que Windows Vista et versions ultérieures. Pour ce type de chargement de module, l’application doit appeler les fonctions MUI [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche de ressources Win32 PE](locating-win32-pe-resources.md)
</dt> <dt>

[MUI : exemple de Paramètres Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI : exemple de Paramètres Application-Specific (pré-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
