---
title: Versions de contrôle courantes
description: Cette rubrique répertorie les versions disponibles de la bibliothèque de contrôles communs (ComCtl32.dll), décrit comment identifier la version utilisée par votre application et explique comment cibler votre application pour une version spécifique.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f1a70be183ff0bd3b1f88af548605fece254cfb172f27b247a12a7557c11a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921129"
---
# <a name="common-control-versions"></a>Versions de contrôle courantes

Cette rubrique répertorie les versions disponibles de la bibliothèque de contrôles communs (ComCtl32.dll), décrit comment identifier la version utilisée par votre application et explique comment cibler votre application pour une version spécifique.

Cette rubrique contient les sections suivantes.

-   [Numéros des versions des DLL de contrôle courantes](#common-control-dll-versions-numbers)
-   [Tailles de structure pour différentes versions de contrôle communes](#structure-sizes-for-different-common-control-versions)
-   [Utilisation de DllGetVersion pour déterminer le numéro de version](#using-dllgetversion-to-determine-the-version-number)
-   [Project Versions](#project-versions)
-   [Rubriques connexes](#related-topics)

## <a name="common-control-dll-versions-numbers"></a>Numéros des versions des DLL de contrôle courantes

la prise en charge des contrôles communs est fournie par ComCtl32.dll, qui incluent toutes les versions 32 bits et 64 bits de Windows. Chaque version successive de la DLL prend en charge les fonctionnalités et l’API des versions antérieures et ajoute de nouvelles fonctionnalités.

Étant donné que différentes versions de ComCtl32.dll ont été distribuées avec Internet Explorer, la version qui est active est parfois différente de la version fournie avec le système d’exploitation. Par conséquent, votre application doit déterminer directement la version de ComCtl32.dll présente.

Dans la documentation de référence des contrôles communs, de nombreux éléments de programmation spécifient un numéro de version DLL minimal pris en charge. Ce numéro de version indique que l’élément de programmation est implémenté dans cette version et les versions ultérieures de la DLL, sauf indication contraire. Si aucun numéro de version n’est spécifié, l’élément de programmation est implémenté dans toutes les versions existantes de la DLL.

Le tableau suivant présente les différentes versions des DLL et la façon dont elles ont été distribuées sur les systèmes d’exploitation pris en charge.



ComCtl32.dll

Version

Plateforme de distribution

5,81

Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 et Microsoft Internet Explorer 6

5,82

Windows server 2003, Windows Vista, Windows Server 2008 et Windows 7

6.0

Windows Server 2003

6.10

Windows Vista, Windows Server 2008 et Windows 7



 

## <a name="structure-sizes-for-different-common-control-versions"></a>Tailles de structure pour différentes versions de contrôle communes

L’amélioration continue des contrôles communs a entraîné la nécessité d’étendre un grand nombre de structures. Pour cette raison, la taille des structures a changé entre les différentes versions de commctrl. h. Étant donné que la plupart des structures de contrôle courantes prennent une taille de structure comme l’un des paramètres, un message ou une fonction peut échouer si la taille n’est pas reconnue. Pour y remédier, les constantes de taille de structure ont été définies pour faciliter le ciblage d’une version différente de ComCtl32.dll. La liste suivante définit les constantes de taille de la structure.



|    Taille de la structure, constante                           |     Définition                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| \_Taille HDITEM v1 \_              | Taille de la structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) dans la version 4,0.                           |
| Taille de IMAGELISTDRAWPARAMS \_ v3 \_ | Taille de la structure [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) dans la version 5,9. |
| \_Taille LVCOLUMN v1 \_            | Taille de la structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) dans la version 4,0.                       |
| Taille de LVGROUP \_ v5 \_             | Taille de la structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) dans la version 6,0.                         |
| \_Taille LVHITTESTINFO v1 \_       | Taille de la structure [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) dans la version 4,0.             |
| \_Taille LVITEM v1 \_              | Taille de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dans la version 4,0.                           |
| Taille de LVITEM \_ v5 \_              | Taille de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dans la version 6,0.                           |
| Taille de LVTILEINFO \_ v5 \_          | Taille de la structure [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) dans la version 6,0.                   |
| \_Taille MCHITTESTINFO v1 \_       | Taille de la structure [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) dans la version 4,0.             |
| Taille de NMLVCUSTOMDRAW \_ v3 \_      | Taille de la structure [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) dans la version 4,7.           |
| \_Taille NMTTDISPINFO v1 \_        | Taille de la structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) dans la version 4,0.               |
| Taille de NMTVCUSTOMDRAW \_ v3 \_      | Taille de la structure [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) dans la version 4,7.           |
| \_Taille PROPSHEETHEADER v1 \_     | Taille de la structure [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) dans la version 4,0.         |
| \_Taille PROPSHEETPAGE v1 \_       | Taille de la structure [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) dans la version 4,0.             |
| Taille de REBARBANDINFO \_ v3 \_       | Taille de la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) dans la version 4,7.             |
| Taille de REBARBANDINFO \_ V6 \_       | Taille de la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) dans la version 6,0.             |
| \_Taille TTTOOLINFO v1 \_          | Taille de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) dans la version 4,0.                       |
| Taille de TTTOOLINFO \_ v2 \_          | Taille de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) dans la version 4,7.                       |
| Taille de TTTOOLINFO \_ v3 \_          | Taille de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) dans la version 6,0.                       |
| \_Taille TVINSERTSTRUCT v1 \_      | Taille de la structure [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) dans la version 4,0.           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Utilisation de DllGetVersion pour déterminer le numéro de version

La fonction [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) peut être appelée par une application pour déterminer la version de la dll qui est présente sur le système.

[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) retourne une structure [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . En plus des informations fournies via [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** fournit également le numéro de correctif qui identifie le dernier Service Pack installé, ce qui offre un moyen plus robuste de comparer les numéros de version. Étant donné que le premier membre de **DLLVERSIONINFO2** est une structure **DLLVERSIONINFO** , la structure la plus récente est à compatibilité descendante.


L’exemple de fonction suivant `GetVersion` charge une DLL spécifiée et tente d’appeler sa fonction [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) . En cas de réussite, elle utilise une macro pour empaqueter les numéros de version majeure et mineure de la structure [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) dans une **valeur DWORD** qui est retournée à l’application appelante. Si la DLL n’exporte pas **DllGetVersion**, la fonction retourne la valeur zéro. Vous pouvez modifier la fonction pour gérer la possibilité que **DllGetVersion** retourne une structure [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . Dans ce cas, utilisez les informations contenues dans le membre **ullVersion** de la structure **DLLVERSIONINFO2** pour comparer les versions, les numéros de build et les versions de Service Pack. La macro [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) simplifie la tâche de comparaison de ces valeurs à celles de **ullVersion**.

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut poser des risques de sécurité. Reportez-vous à la documentation de **LoadLibrary** pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Windows.

 


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

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

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



L’exemple de code suivant montre comment vous pouvez utiliser `GetVersion` pour tester si ComCtl32.dll est la version 6,0 ou une version ultérieure.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a>Project Versions

Pour vous assurer que votre application est compatible avec les différentes versions ciblées d’un fichier .dll, les macros de version sont présentes dans les fichiers d’en-tête. Ces macros permettent de définir, d’exclure ou de redéfinir certaines définitions pour les différentes versions de la DLL. pour une description détaillée de ces macros, consultez [utilisation des en-têtes de Windows](/windows/desktop/WinProg/using-the-windows-headers) .

Par exemple, le nom de macro **\_ Win32 \_ IE** se trouve généralement dans les en-têtes plus anciens. Vous êtes responsable de la définition de la macro sous la forme d’un nombre hexadécimal. Ce numéro de version définit la version cible de l’application qui utilise la DLL. Le tableau suivant répertorie les numéros de version disponibles et l’effet de chacun d’entre eux sur votre application.



| Version | Description                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0300  | L’application est compatible avec ComCtl32.dll version 4,70 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,70. |
| 0x0400  | L’application est compatible avec ComCtl32.dll version 4,71 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,71. |
| 0x0401  | L’application est compatible avec ComCtl32.dll version 4,72 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,72. |
| 0x0500  | L’application est compatible avec ComCtl32.dll version 5,80 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 5,80. |
| 0x0501  | L’application est compatible avec ComCtl32.dll version 5,81 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 5,81. |
| 0x0600  | L’application est compatible avec ComCtl32.dll version 6,0 et versions ultérieures. L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 6,0.   |



 

Si vous ne définissez pas la macro **\_ Win32 \_ IE** dans votre projet, elle est automatiquement définie en tant que 0x0500. Pour définir une valeur différente, vous pouvez ajouter les éléments suivants aux directives de compilateur dans votre fichier Make ; Remplacez 0x0400 par le numéro de version de votre choix.


```C++
/D _WIN32_IE=0x0400
```



Une autre méthode consiste à ajouter une ligne semblable à la suivante dans votre code source avant d’inclure les fichiers d’en-tête de Shell. Remplacez 0x0400 par le numéro de version de votre choix.


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles communs](common-controls-intro.md)
</dt> </dl>

 

 