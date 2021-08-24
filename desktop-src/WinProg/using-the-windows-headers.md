---
title: utilisation des en-têtes de Windows
description: utilisez les fichiers d’en-tête Windows pour créer des applications qui utilisent l’API Windows.
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- Windows API, fichiers d’en-tête
- C2065
- WINVER
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 886c5601683cc03fb2486f8be3b69f31c4619b721276babbc2c3e31e28c0a022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643589"
---
# <a name="using-the-windows-headers"></a>utilisation des en-têtes de Windows

les fichiers d’en-tête de l’API Windows vous permettent de créer des applications 32 et 64 bits. Elles incluent des déclarations pour les versions Unicode et ANSI de l’API. pour plus d’informations, consultez [Unicode dans l’API Windows](/windows/desktop/Intl/unicode-in-the-windows-api). Ils utilisent des [types de données](windows-data-types.md) qui vous permettent de générer des versions 32 et 64 bits de votre application à partir d’une base de code source unique. Pour plus d’informations, consultez [préparation à la Windows 64 bits](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows). Les fonctionnalités supplémentaires incluent les [annotations d’en-tête](header-annotations.md) et la [vérification stricte des types](strict-type-checking.md).

-   [Visual C++ et les fichiers d’en-tête Windows](#visual-c-and-the-windows-header-files)
-   [Macros pour les déclarations conditionnelles](#macros-for-conditional-declarations)
-   [Définition de WINVER ou de \_ Win32 \_ winnt](#setting-winver-or-_win32_winnt)
-   [Contrôle de la compression de structure](#controlling-structure-packing)
-   [Builds plus rapides avec des fichiers d’en-tête plus petits](#faster-builds-with-smaller-header-files)
-   [Rubriques connexes](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a>Visual C++ et les fichiers d’en-tête Windows

Microsoft Visual C++ contient des copies des fichiers d’en-tête Windows qui étaient en cours au moment où Visual C++ a été libéré. par conséquent, si vous installez des fichiers d’en-tête mis à jour à partir d’un kit de développement logiciel (SDK), vous pouvez vous retrouver avec plusieurs versions des fichiers d’en-tête Windows sur votre ordinateur. Si vous ne vous assurez pas que vous utilisez la version la plus récente des fichiers d’en-tête du kit de développement logiciel (SDK), vous recevrez le code d’erreur suivant lors de la compilation du code qui utilise les fonctionnalités qui ont été introduites après la publication de Visual C++ : Error C2065 : identificateur non déclaré.

## <a name="macros-for-conditional-declarations"></a>Macros pour les déclarations conditionnelles

certaines fonctions qui dépendent d’une version particulière de Windows sont déclarées à l’aide de code conditionnel. Cela vous permet d’utiliser le compilateur pour détecter si votre application utilise des fonctions qui ne sont pas prises en charge sur sa ou ses versions cibles de Windows. Pour compiler une application qui utilise ces fonctions, vous devez définir les macros appropriées. Dans le cas contraire, vous recevrez le message d’erreur C2065.

les fichiers d’en-tête Windows utilisent des macros pour indiquer quelles versions de Windows prennent en charge de nombreux éléments de programmation. Par conséquent, vous devez définir ces macros pour utiliser les nouvelles fonctionnalités introduites dans chaque version majeure du système d’exploitation. (Les fichiers d’en-tête individuels peuvent utiliser des macros différentes ; par conséquent, si des problèmes de compilation se produisent, recherchez dans le fichier d’en-tête qui contient la définition des définitions conditionnelles.) Pour plus d’informations, consultez SdkDdkVer. h.

le tableau suivant décrit les macros préférées utilisées dans les fichiers d’en-tête Windows. Si vous définissez la \_ version NTDDI, vous devez également définir \_ Win32 \_ winnt.



| Système minimal requis                       | Valeur pour la \_ version de NTDDI            |
|-----------------------------------------------|-------------------------------------|
| Windows 10 1903 « 19H1 »                        | **NTDDI \_ WIN10 \_ 19H1** (0x0A000007) |
| Windows 10 1809 « Redstone 5 »                  | **NTDDI \_ WIN10 \_ RS5** (0x0A000006)  |
| Windows 10 1803 « Redstone 4 »                  | **NTDDI \_ WIN10 \_ RS4** (0x0A000005)  |
| Windows 10 1709 « Redstone 3 »                  | **NTDDI \_ WIN10 \_ RS3** (0x0A000004)  |
| Windows 10 1703 « Redstone 2 »                  | **NTDDI \_ WIN10 \_ RS2** (0x0A000003)  |
| Windows 10 1607 « Redstone 1 »                  | **NTDDI \_ WIN10 \_ RS1** (0x0A000002)  |
| Windows 10 1511 « seuil 2 »                 | **NTDDI \_ WIN10 \_ Th2** (0x0A000001)  |
| Windows 10 1507 « seuil »                   | **NTDDI \_ WIN10** (0x0A000000)       |
| Windows 8.1                                   | **NTDDI \_ WINBLUE** (0x06030000)     |
| Windows 8                                     | **NTDDI \_ WIN8** (0x06020000)        |
| Windows 7                                     | **NTDDI \_ WIN7** (0x06010000)        |
| Windows Server 2008                           | **NTDDI \_ WS08** (0x06000100)        |
| Windows Vista Service Pack 1 (SP1)       | **NTDDI \_ VISTASP1** (0x06000100)    |
| Windows Vista                                 | **NTDDI \_ VISTA** (0x06000000)       |
| Windows Server 2003 avec Service Pack 2 (SP2) | **NTDDI \_ WS03SP2** (0x05020200)     |
| Windows Server 2003 avec Service Pack 1 (SP1) | **NTDDI \_ WS03SP1** (0x05020100)     |
| Windows Server 2003                           | **NTDDI \_ WS03** (0x05020000)        |
| Windows XP avec Service Pack 3 (SP3)          | **NTDDI \_ WINXPSP3** (0x05010300)    |
| Windows XP avec Service Pack 2 (SP2)          | **NTDDI \_ WINXPSP2** (0x05010200)    |
| Windows XP avec Service Pack 1 (SP1)          | **NTDDI \_ WINXPSP1** (0x05010100)    |
| Windows XP                                    | **NTDDI \_ WINXP** (0x05010000)       |



 

les tableaux suivants décrivent les autres macros utilisées dans les fichiers d’en-tête Windows.



| Système minimal requis                           | Valeur minimale pour \_ Win32 \_ winnt et winver |
|---------------------------------------------------|---------------------------------------------|
| Windows 10                                        | **\_ Win32 \_ winnt \_ WIN10** (0x0A00)          |
| Windows 8.1                                       | **\_ Win32 \_ winnt \_ WINBLUE** (0x0603)        |
| Windows 8                                         | **\_ Win32 \_ winnt \_ WIN8** (0x0602)           |
| Windows 7                                         | **\_ Win32 \_ winnt \_ win7** (0x0601)           |
| Windows Server 2008                               | **\_ Win32 \_ winnt \_ WS08** (0x0600)           |
| Windows Vista                                     | **\_ Win32 \_ winnt \_ Vista** (0x0600)          |
| Windows serveur 2003 avec SP1, Windows XP avec SP2 | **\_ Win32 \_ winnt \_ WS03** (0x0502)           |
| Windows serveur 2003, Windows XP                   | **\_ Win32 \_ winnt \_ WinXP** (0x0501)          |



 



| Version minimale nécessaire          | Valeur minimale de \_ Win32 \_ IE      |
|-----------------------------------|-----------------------------------|
| Internet Explorer 11,0            | **\_ Win32 \_ IE \_ IE110** (0x0A00)   |
| Internet Explorer 10.0            | **\_ Win32 \_ IE \_ IE100** (0x0A00)   |
| Internet Explorer 9.0             | **\_ Win32 \_ IE \_ IE90** (0x0900)    |
| Internet Explorer 8.0             | **\_ Win32 \_ IE \_ IE80** (0x0800)    |
| Internet Explorer 7.0             | **\_ Win32 \_ IE \_ IE70** (0x0700)    |
| Internet Explorer 6,0 SP2         | **\_ Win32 \_ IE \_ IE60SP2** (0x0603) |
| Internet Explorer 6,0 SP1         | **\_ Win32 \_ IE \_ IE60SP1** (0x0601) |
| Internet Explorer 6.0             | **\_ Win32 \_ IE \_ IE60** (0x0600)    |
| Internet Explorer 5,5             | **\_ Win32 \_ IE \_ IE55** (0x0550)    |
| Internet Explorer 5,01            | **\_ Win32 \_ IE \_ IE501** (0x0501)   |
| Internet Explorer 5,0, 5.0 a, 5.0 b | **\_ Win32 \_ IE \_ Ie50** (0x0500)    |



 

## <a name="setting-winver-or-_win32_winnt"></a>Définition de WINVER ou de \_ Win32 \_ winnt

Vous pouvez définir ces symboles à l’aide de l' \# instruction define dans chaque fichier source, ou en spécifiant l’option de compilateur/d prise en charge par Visual C++.

Par exemple, pour définir WINVER dans votre fichier source, utilisez l’instruction suivante :

`#define WINVER 0x0502`

Pour définir \_ Win32 \_ winnt dans votre fichier source, utilisez l’instruction suivante :

`#define _WIN32_WINNT 0x0502`

Pour définir \_ Win32 \_ winnt à l’aide de l’option du compilateur/d, utilisez la commande suivante :

**cl-c/d \_ WIN32 \_ winnt = 0x0502** _source_**. cpp**

Pour plus d’informations sur l’utilisation de l’option de compilateur/D, consultez [/d (définitions de préprocesseur)](/cpp/build/reference/d-preprocessor-definitions).

notez que certaines fonctionnalités introduites dans la dernière version de Windows peuvent être ajoutées à une Service Pack pour une version précédente de Windows. Par conséquent, pour cibler un Service Pack, vous devrez peut-être définir \_ Win32 \_ winnt avec la valeur de la prochaine version majeure du système d’exploitation. par exemple, la fonction [**GetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) a été introduite dans Windows Server 2003 et est définie de manière conditionnelle si \_ WIN32 \_ winnt 0x0502 ou une version ultérieure. cette fonction a également été ajoutée à Windows XP avec SP1. par conséquent, si vous deviez définir \_ WIN32 \_ winnt comme 0x0501 pour cibler Windows xp, vous manquez les fonctionnalités définies dans Windows xp avec SP1.

## <a name="controlling-structure-packing"></a>Contrôle de la compression de structure

Les projets doivent être compilés pour utiliser la compression de structure par défaut, qui est actuellement de 8 octets, car le plus grand type intégral est de 8 octets. cela garantit que tous les types de structure dans les fichiers d’en-tête sont compilés dans l’application avec le même alignement que celui attendu par l’API Windows. Elle garantit également que les structures avec des valeurs de 8 octets sont correctement alignées et n’entraînent pas d’erreurs d’alignement sur les processeurs qui appliquent l’alignement des données.

Pour plus d’informations, consultez [/Zp (alignement des membres de la structure)](/cpp/build/reference/zp-struct-member-alignment) ou [Pack](/cpp/preprocessor/pack).

## <a name="faster-builds-with-smaller-header-files"></a>Builds plus rapides avec des fichiers d’en-tête plus petits

vous pouvez réduire la taille des fichiers d’en-tête Windows en excluant certaines des déclarations d’API les moins courantes comme suit :

-   définissez le terme WIN32 \_ \_ et la \_ moyenne pour exclure les api telles que les sockets de chiffrement, DDE, RPC, Shell et Windows.

    `#define WIN32_LEAN_AND_MEAN`

-   Définissez un ou plusieurs symboles d'*API* pour exclure l’API. Par exemple, NOCOMM exclut l’API de communication série. pour obtenir une liste de prise en charge des symboles d'*api* , consultez Windows. h.

    `#define NOCOMM`

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Site de téléchargement du SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 