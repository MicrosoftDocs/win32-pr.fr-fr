---
title: Modification des éléments des informations utilisateur
description: Les fonctions de gestion de réseau fournissent divers niveaux d’informations pour vous aider à modifier les informations utilisateur.
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1aa6ec8d7fed30d38d25adc67974d8bad8ab1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119314"
---
# <a name="changing-elements-of-user-information"></a>Modification des éléments des informations utilisateur

Les fonctions de gestion de réseau fournissent divers niveaux d’informations pour vous aider à modifier les informations utilisateur. Certains niveaux requièrent des privilèges d’administrateur pour s’exécuter correctement. Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).

L’exemple de code de cette rubrique montre comment modifier plusieurs éléments d’informations utilisateur en appelant la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . Le code utilise différentes structures d’informations de gestion de réseau.

Lors de la modification des informations utilisateur, il est préférable d’utiliser le niveau spécifique pour ce renseignement. Cela empêche la réinitialisation accidentelle d’informations non liées lors de l’utilisation des valeurs de niveau inférieur.

La définition de certains des niveaux les plus couramment utilisés est illustrée dans les exemples de code suivants :

-   [Définition du mot de passe utilisateur, niveau 1003](#setting-the-user-password-level-1003)
-   [Définition du privilège de l’utilisateur, niveau 1005](#setting-the-user-privilege-level-1005)
-   [Définition du répertoire de démarrage de l’utilisateur, niveau 1006](#setting-the-user-home-directory-level-1006)
-   [Définition du champ de commentaire de l’utilisateur, niveau 1007](#setting-the-user-comment-field-level-1007)
-   [Définition des indicateurs utilisateur, niveau 1008](#setting-the-user-flags-level-1008)
-   [Définition du chemin d’accès au script utilisateur, niveau 1009](#setting-the-user-script-path-level-1009)
-   [Définition des indicateurs de l’autorité de l’utilisateur, niveau 1010](#setting-the-user-authority-flags-level-1010)
-   [Définition du nom complet de l’utilisateur, niveau 1011](#setting-the-user-full-name-level-1011)

Tous les fragments de code supposent que l’utilisateur a défini la directive de compilation UNICODE et a inclus les fichiers d’en-tête du kit de développement logiciel (SDK) appropriés, comme suit :


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

#define SERVER L"test_server_name"
#define USERNAME L"test_user_name"

DWORD netRet = 0;
```



## <a name="setting-the-user-password-level-1003"></a>Définition du mot de passe utilisateur, niveau 1003

Le fragment de code suivant montre comment définir le mot de passe d’un utilisateur sur une valeur connue à l’aide d’un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . La [**rubrique \_ informations utilisateur \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) contient des informations supplémentaires.


```C++
#define PASSWORD L"new_password"

USER_INFO_1003 usriSetPassword;
//
// Set the usri1003_password member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriSetPassword.usri1003_password = PASSWORD;
    
netRet = NetUserSetInfo( SERVER, USERNAME, 1003, (LPBYTE)&usriSetPassword, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1003!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1003\n", netRet);
```



## <a name="setting-the-user-privilege-level-1005"></a>Définition du privilège de l’utilisateur, niveau 1005

Le fragment de code suivant montre comment spécifier le niveau de privilège affecté à un utilisateur avec un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . La [**rubrique \_ informations utilisateur \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) contient des informations supplémentaires. Pour plus d’informations sur les privilèges de compte, consultez [privilèges](/windows/desktop/SecAuthZ/privileges) et [constantes d’autorisation](/windows/desktop/SecAuthZ/authorization-constants).


```C++
USER_INFO_1005 usriPriv;
//
// Set the usri1005_priv member to the appropriate value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriPriv.usri1005_priv = USER_PRIV_USER;

netRet = NetUserSetInfo( SERVER, USERNAME, 1005, (LPBYTE)&usriPriv, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1005!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1005\n", netRet);
```



## <a name="setting-the-user-home-directory-level-1006"></a>Définition du répertoire de démarrage de l’utilisateur, niveau 1006

Le fragment de code suivant montre comment spécifier le chemin d’accès du répertoire de départ d’un utilisateur à l’aide d’un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . Le répertoire peut être un chemin d’accès codé en dur ou un chemin d’accès Unicode valide. La [**rubrique \_ informations utilisateur \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) contient des informations supplémentaires.


```C++
#define HOMEDIR L"C:\\USER\USER_PATH"
USER_INFO_1006 usriHomeDir;
//
// Set the usri1006_home_dir member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriHomeDir.usri1006_home_dir = HOMEDIR;

netRet = NetUserSetInfo( SERVER, USERNAME, 1006, (LPBYTE)&usriHomeDir, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1006!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1006\n", netRet);
```



## <a name="setting-the-user-comment-field-level-1007"></a>Définition du champ de commentaire de l’utilisateur, niveau 1007

Le fragment de code suivant illustre comment associer un commentaire à un utilisateur en appelant la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . La [**rubrique \_ informations utilisateur \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) contient des informations supplémentaires.


```C++
#define COMMENT L"This is my Comment Text for the user"
USER_INFO_1007 usriComment;
//
// Set the usri1007_comment member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriComment.usri1007_comment = COMMENT;

netRet = NetUserSetInfo( SERVER, USERNAME, 1007, (LPBYTE)&usriComment, NULL );

if( netRet == NERR_Success )
    printf("Success with level 1007!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1007\n", netRet);
```



## <a name="setting-the-user-flags-level-1008"></a>Définition des indicateurs utilisateur, niveau 1008

Le fragment de code suivant montre comment définir des indicateurs utilisateur avec un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . La [**rubrique \_ informations utilisateur \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) contient une liste de valeurs valides pour les indicateurs et une description de chaque indicateur.

notez que l' \_ indicateur de SCRIPT UF doit être défini pour les réseaux Windows NT, Windows 2000, Windows XP et LAN Manager. Si vous tentez de définir d’autres indicateurs sans définir \_ le script UF sur ces réseaux, la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) échouera.


```C++
#define USR_FLAGS UF_SCRIPT | UF_NORMAL_ACCOUNT
USER_INFO_1008 usriFlags;
//
// Set the usri1008_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFlags.usri1008_flags = USR_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1008, (LPBYTE)&usriFlags, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1008!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1008\n", netRet);
```



## <a name="setting-the-user-script-path-level-1009"></a>Définition du chemin d’accès au script utilisateur, niveau 1009

Le fragment de code suivant montre comment définir le chemin d’accès pour le fichier de script d’ouverture de session d’un utilisateur particulier à l’aide d’un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . Le fichier de script peut être. Fichier CMD, fichier .EXE ou .BAT. La chaîne peut également avoir la valeur null. La [**rubrique \_ informations utilisateur \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) contient des informations supplémentaires.


```C++
#define SCRIPT_PATH L"C:\\BIN\\MYSCRIPT.BAT"
USER_INFO_1009 usriScrPath;
//
// Set the usri1009_script_path member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriScrPath.usri1009_script_path = SCRIPT_PATH;
netRet = NetUserSetInfo( SERVER, USERNAME, 1009, (LPBYTE)&usriScrPath, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1009!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1009\n", netRet);
```



## <a name="setting-the-user-authority-flags-level-1010"></a>Définition des indicateurs de l’autorité de l’utilisateur, niveau 1010

Le fragment de code suivant montre comment définir les indicateurs de privilège d’opérateur pour un utilisateur avec un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . La [**rubrique \_ informations utilisateur \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) contient une liste de valeurs valides pour les indicateurs et une description de chaque indicateur.


```C++
#define AUTHORITY_FLAGS AF_OP_ACCOUNTS
USER_INFO_1010 usriAuthFlags;
//
// Set the usri1010_auth_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriAuthFlags.usri1010_auth_flags = AUTHORITY_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1010, (LPBYTE)&usriAuthFlags, NULL);
if( netRet == NERR_Success )
    printf("Success with level 1010!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1010\n", netRet);
```



## <a name="setting-the-user-full-name-level-1011"></a>Définition du nom complet de l’utilisateur, niveau 1011

Le fragment de code suivant montre comment définir le nom complet d’un utilisateur à l’aide d’un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . La [**rubrique \_ informations utilisateur \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) contient des informations supplémentaires.


```C++
#define USER_FULL_NAME L"Joe B. User"
USER_INFO_1011 usriFullName;
//
// Set the usri1011_full_name member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFullName.usri1011_full_name = USER_FULL_NAME;
netRet = NetUserSetInfo( SERVER, USERNAME, 1011, (LPBYTE)&usriFullName, NULL);
if( netRet == NERR_Success ) 
    printf("Success with level 1011!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo\n", netRet);
```



 

 