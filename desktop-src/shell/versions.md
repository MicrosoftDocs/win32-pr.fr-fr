---
description: Cette section décrit comment déterminer la version des dll Shell sur laquelle votre application s’exécute et comment cibler votre application pour une version spécifique.
title: Versions des DLL Shell et Shlwapi
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220316"
---
# <a name="shell-and-shlwapi-dll-versions"></a>Versions des DLL Shell et Shlwapi

Cette section décrit comment déterminer la version des dll Shell sur laquelle votre application s’exécute et comment cibler votre application pour une version spécifique.

-   [Numéros de version des DLL](#dll-version-numbers)
-   [Utilisation de DllGetVersion pour déterminer le numéro de version](#using-dllgetversion-to-determine-the-version-number)
    -   [Utilisation de DllGetVersion](#using-dllgetversion)
-   [Project Versions](#project-versions)

## <a name="dll-version-numbers"></a>Numéros de version des DLL

Tous les éléments de programmation, à l’exception de quelques-uns, décrits dans la documentation de l’interpréteur de commandes sont contenus dans deux dll : Shell32.dll et Shlwapi.dll. En raison des améliorations en cours, différentes versions de ces dll implémentent des fonctionnalités différentes. Tout au long de la documentation de référence du shell, chaque élément de programmation spécifie un numéro de version DLL minimal pris en charge. Ce numéro de version indique que l’élément de programmation est implémenté dans cette version et les versions ultérieures de la DLL, sauf indication contraire. Si aucun numéro de version n’est spécifié, l’élément de programmation est implémenté dans toutes les versions existantes de la DLL.

avant Windows XP, de nouvelles versions de Shell32.dll et de Shlwapi.dll étaient parfois fournies avec les nouvelles versions de Windows Internet Explorer. à partir de Windows XP, ces dll n’étaient plus fournies en tant que fichiers redistribuables en dehors des nouvelles versions de Windows elles-mêmes. le tableau suivant présente les différentes versions des DLL et la façon dont elles ont été distribuées à nouveau vers microsoft Internet Explorer 3,0, Windows 95 et microsoft Windows NT 4,0.

Shell32.dll version 4,0 est disponible dans les versions d’origine de Windows 95 et Microsoft Windows NT 4,0. L’interpréteur de commandes n’a pas été mis à jour avec la version 3,0 d’Internet Explorer, donc Shell32.dll n’a pas de version 4,70. Les versions 4,71 et 4,72 de Shell32.dll étaient fournies avec les versions d’Internet Explorer correspondantes, mais elles n’étaient pas nécessairement installées (voir la remarque 1). pour les versions ultérieures à Microsoft Internet Explorer 4,01 et Windows 98, les numéros de version pour Shell32.dll et Shlwapi.dll divergent. En général, vous devez supposer que les dll ont des numéros de version différents et tester chacune d’elles séparément.

#### <a name="shell32dll"></a>Shell32.dll

| Version | Plateforme de distribution                                                       |
|---------|-----------------------------------------------------------------------------|
| 4.0     | Windows 95 et Microsoft Windows NT 4,0                                     |
| 4.71    | Microsoft Internet Explorer 4,0. Consultez la remarque 1.                                |
| 4.72    | Internet Explorer 4,01 et Windows 98. Consultez la remarque 1.                          |
| 5.0     | Windows 2000 et Windows Millennium edition (Windows Me). Voir la remarque 2.       |
| 6.0     | Windows XP                                                                  |
| 6.0.1   | Windows Vista                                                               |
| 6.1     | Windows 7                                                                   |

#### <a name="shlwapidll"></a>Shlwapi.dll

| Version | Plateforme de distribution                                                       |
|---------|-----------------------------------------------------------------------------|
| 4.0     | Windows 95 et Microsoft Windows NT 4,0                                     |
| 4.71    | Internet Explorer 4,0. Consultez la remarque 1.                                          |
| 4.72    | Internet Explorer 4,01 et Windows 98. Consultez la remarque 1.                          |
| 4,7     | Internet Explorer 3. x                                                       |
| 5.0     | Microsoft Internet Explorer 5 et Windows 98 SE. Voir la remarque 2.                |
| 5.5     | Microsoft Internet Explorer 5,5 et Windows Millennium edition (Windows Me) |
| 6.0     | Windows XP et Windows Vista                                                |



**Remarque 1 :** Tous les systèmes avec Internet Explorer 4,0 ou 4,01 avaient la version associée de Shlwapi.dll (respectivement 4,71 ou 4,72). toutefois, pour les systèmes antérieurs à Windows 98, Internet Explorer 4,0 et 4,01 peuvent être installés avec ou sans ce qui était connu comme le *Shell intégré*. Si Internet Explorer a été installé avec l’interpréteur de commandes intégré, la version associée de Shell32.dll (4,71 ou 4,72) a également été installée. Si Internet Explorer a été installé sans l’interpréteur de commandes intégré, Shell32.dll est resté en version 4,0. En d’autres termes, la présence de la version 4,71 ou 4,72 de Shlwapi.dll sur un système ne garantit pas que Shell32.dll a le même numéro de version. tous les systèmes Windows 98 disposent de la version 4,72 de Shell32.dll.

**Remarque 2 :** la Version 5,0 de Shlwapi.dll a été distribuée avec internet explorer 5 et a été trouvée sur tous les systèmes sur lesquels internet explorer 5 a été installé, à l’exception de Windows 2000. la version 5,0 de Shell32.dll a été distribuée en mode natif avec Windows 2000 et Windows Millennium edition (Windows), ainsi que la version 5,0 de Shlwapi.dll.

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Utilisation de DllGetVersion pour déterminer le numéro de version

Depuis la version 4,71, les dll de l’interpréteur de commandes, entre autres, ont commencé à exporter [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Cette fonction peut être appelée par une application pour déterminer la version de la DLL qui est présente sur le système.

> [!Note]  
> Les dll n’exportent pas nécessairement [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Testez toujours ce dernier avant de tenter de l’utiliser.

pour les versions Windows antérieures à Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) retourne une structure [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) qui contient les numéros de version principale et secondaire, le numéro de build et un ID de plateforme. pour les systèmes Windows 2000 et versions ultérieures, **DllGetVersion** peut retourner une structure [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) . En plus des informations fournies via **DLLVERSIONINFO**, **DLLVERSIONINFO2** fournit également le numéro de correctif qui identifie le dernier Service Pack installé, ce qui offre un moyen plus robuste de comparer les numéros de version. Étant donné que le premier membre de **DLLVERSIONINFO2** est une structure **DLLVERSIONINFO** , la structure la plus récente est à compatibilité descendante.

### <a name="using-dllgetversion"></a>Utilisation de DllGetVersion

L’exemple de fonction suivant `GetVersion` charge une DLL spécifiée et tente d’appeler sa fonction [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) . En cas de réussite, elle utilise une macro pour empaqueter les numéros de version majeure et mineure de la structure [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) dans une **valeur DWORD** qui est retournée à l’application appelante. Si la DLL n’exporte pas **DllGetVersion**, la fonction retourne la valeur zéro. avec les systèmes Windows 2000 et versions ultérieures, vous pouvez modifier la fonction pour gérer la possibilité que **DllGetVersion** retourne une structure [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) . Dans ce cas, utilisez les informations contenues dans le membre **ullVersion** de la structure **DLLVERSIONINFO2** pour comparer les versions, les numéros de build et les versions de Service Pack. La macro [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) simplifie la tâche de comparaison de ces valeurs à celles de **ullVersion**.

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut poser des risques de sécurité. Reportez-vous à la documentation de **LoadLibrary** pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Windows.


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


L’exemple de code suivant montre comment vous pouvez utiliser `GetVersion` pour tester si Shell32.dll est la version 6,0 ou une version ultérieure.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a>Project Versions

Pour vous assurer que votre application est compatible avec les différentes versions ciblées d’un fichier .dll, les macros de version sont présentes dans les fichiers d’en-tête. Ces macros permettent de définir, d’exclure ou de redéfinir certaines définitions pour les différentes versions de la DLL. pour une description détaillée de ces macros, consultez [utilisation des en-têtes de Windows](../winprog/using-the-windows-headers.md) .

Par exemple, le nom de macro **\_ Win32 \_ IE** se trouve généralement dans les en-têtes plus anciens. Vous êtes responsable de la définition de la macro sous la forme d’un nombre hexadécimal. Ce numéro de version définit la version cible de l’application qui utilise la DLL. Le tableau suivant répertorie les numéros de version disponibles et l’effet de chacun d’entre eux sur votre application.


| Version | Description                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0200  | L’application est compatible avec Shell32.dll version 4,00 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,00.                                              |
| 0x0300  | L’application est compatible avec Shell32.dll version 4,70 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,70.                                              |
| 0x0400  | L’application est compatible avec Shell32.dll version 4,71 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,71.                                              |
| 0x0401  | L’application est compatible avec Shell32.dll version 4,72 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,72.                                              |
| 0x0500  | L’application est compatible avec Shell32.dll et Shlwapi.dll version 5,0 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 5,0 de Shell32.dll et Shlwapi.dll. |
| 0x0501  | L’application est compatible avec Shell32.dll et Shlwapi.dll version 5,0 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 5,0 de Shell32.dll et Shlwapi.dll. |
| 0x0600  | L’application est compatible avec Shell32.dll et Shlwapi.dll version 6,0 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 6,0 de Shell32.dll et Shlwapi.dll. |


Si vous ne définissez pas la macro **\_ Win32 \_ IE** dans votre projet, elle est automatiquement définie en tant que 0x0500. Pour définir une valeur différente, vous pouvez ajouter les éléments suivants aux directives de compilateur dans votre fichier Make ; Remplacez 0x0400 par le numéro de version de votre choix.

```
/D _WIN32_IE=0x0400
```

Une autre méthode consiste à ajouter une ligne semblable à la suivante dans votre code source avant d’inclure les fichiers d’en-tête de Shell. Remplacez 0x0400 par le numéro de version de votre choix.

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
