---
description: Chargement des ressources de langue
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Chargement des ressources de langue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eebf027476658872fe392fe60699da1a586f9297f39a191898b1e132439962c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106929"
---
# <a name="loading-language-resources"></a>Chargement des ressources de langue

Votre application charge toutes les ressources de la langue de l’interface utilisateur, à l’exception de certaines chaînes de Registre redirigées, à l’aide d’appels aux fonctions de chargement de ressources standard, par exemple, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)et [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea). De nombreuses fonctions de chargement des ressources ont été modifiées pour charger automatiquement des ressources à partir de fichiers de ressources spécifiques à une langue, en traitant les ressources comme si elles étaient contenues dans le fichier LN. L’exemple suivant illustre l’utilisation de **LoadString** pour charger des chaînes de langue pour une application qui suit les paramètres de langue système.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche de ressources Win32 PE](locating-win32-pe-resources.md)
</dt> </dl>

 

 
