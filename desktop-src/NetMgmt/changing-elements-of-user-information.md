---
title: Modification des éléments des informations utilisateur
description: Les fonctions de gestion de réseau fournissent divers niveaux d’informations pour vous aider à modifier les informations utilisateur.
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1aa6ec8d7fed30d38d25adc67974d8bad8ab1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509260"
---
# <a name="changing-elements-of-user-information"></a><span data-ttu-id="898d1-103">Modification des éléments des informations utilisateur</span><span class="sxs-lookup"><span data-stu-id="898d1-103">Changing Elements of User Information</span></span>

<span data-ttu-id="898d1-104">Les fonctions de gestion de réseau fournissent divers niveaux d’informations pour vous aider à modifier les informations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="898d1-104">The network management functions provide a variety of information levels to assist in changing user information.</span></span> <span data-ttu-id="898d1-105">Certains niveaux requièrent des privilèges d’administrateur pour s’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="898d1-105">Some levels require administrative privileges to execute successfully.</span></span> <span data-ttu-id="898d1-106">Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="898d1-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="898d1-107">L’exemple de code de cette rubrique montre comment modifier plusieurs éléments d’informations utilisateur en appelant la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="898d1-107">The sample code in this topic demonstrates how to change several elements of user information by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="898d1-108">Le code utilise différentes structures d’informations de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="898d1-108">The code uses various network management information structures.</span></span>

<span data-ttu-id="898d1-109">Lors de la modification des informations utilisateur, il est préférable d’utiliser le niveau spécifique pour ce renseignement.</span><span class="sxs-lookup"><span data-stu-id="898d1-109">When changing user information, it is best to use the specific level for that piece of information.</span></span> <span data-ttu-id="898d1-110">Cela empêche la réinitialisation accidentelle d’informations non liées lors de l’utilisation des valeurs de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="898d1-110">This prevents the accidental resetting of unrelated information when using the lower level values.</span></span>

<span data-ttu-id="898d1-111">La définition de certains des niveaux les plus couramment utilisés est illustrée dans les exemples de code suivants :</span><span class="sxs-lookup"><span data-stu-id="898d1-111">Setting some of the more commonly used levels is illustrated in the following code samples:</span></span>

-   [<span data-ttu-id="898d1-112">Définition du mot de passe utilisateur, niveau 1003</span><span class="sxs-lookup"><span data-stu-id="898d1-112">Setting the User Password, Level 1003</span></span>](#setting-the-user-password-level-1003)
-   [<span data-ttu-id="898d1-113">Définition du privilège de l’utilisateur, niveau 1005</span><span class="sxs-lookup"><span data-stu-id="898d1-113">Setting the User Privilege, Level 1005</span></span>](#setting-the-user-privilege-level-1005)
-   [<span data-ttu-id="898d1-114">Définition du répertoire de démarrage de l’utilisateur, niveau 1006</span><span class="sxs-lookup"><span data-stu-id="898d1-114">Setting the User Home Directory, Level 1006</span></span>](#setting-the-user-home-directory-level-1006)
-   [<span data-ttu-id="898d1-115">Définition du champ de commentaire de l’utilisateur, niveau 1007</span><span class="sxs-lookup"><span data-stu-id="898d1-115">Setting the User Comment Field, Level 1007</span></span>](#setting-the-user-comment-field-level-1007)
-   [<span data-ttu-id="898d1-116">Définition des indicateurs utilisateur, niveau 1008</span><span class="sxs-lookup"><span data-stu-id="898d1-116">Setting the User Flags, Level 1008</span></span>](#setting-the-user-flags-level-1008)
-   [<span data-ttu-id="898d1-117">Définition du chemin d’accès au script utilisateur, niveau 1009</span><span class="sxs-lookup"><span data-stu-id="898d1-117">Setting the User Script Path, Level 1009</span></span>](#setting-the-user-script-path-level-1009)
-   [<span data-ttu-id="898d1-118">Définition des indicateurs de l’autorité de l’utilisateur, niveau 1010</span><span class="sxs-lookup"><span data-stu-id="898d1-118">Setting The User Authority Flags, Level 1010</span></span>](#setting-the-user-authority-flags-level-1010)
-   [<span data-ttu-id="898d1-119">Définition du nom complet de l’utilisateur, niveau 1011</span><span class="sxs-lookup"><span data-stu-id="898d1-119">Setting The User Full Name, Level 1011</span></span>](#setting-the-user-full-name-level-1011)

<span data-ttu-id="898d1-120">Tous les fragments de code supposent que l’utilisateur a défini la directive de compilation UNICODE et a inclus les fichiers d’en-tête du kit de développement logiciel (SDK) appropriés, comme suit :</span><span class="sxs-lookup"><span data-stu-id="898d1-120">All code fragments assume that the user has defined the UNICODE compile directive and included the appropriate SDK header files, as follows:</span></span>


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



## <a name="setting-the-user-password-level-1003"></a><span data-ttu-id="898d1-121">Définition du mot de passe utilisateur, niveau 1003</span><span class="sxs-lookup"><span data-stu-id="898d1-121">Setting the User Password, Level 1003</span></span>

<span data-ttu-id="898d1-122">Le fragment de code suivant montre comment définir le mot de passe d’un utilisateur sur une valeur connue à l’aide d’un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="898d1-122">The following code fragment illustrates how to set a user's password to a known value with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="898d1-123">La [**rubrique \_ informations utilisateur \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) contient des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="898d1-123">The [**USER\_INFO\_1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) topic contains additional information.</span></span>


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



## <a name="setting-the-user-privilege-level-1005"></a><span data-ttu-id="898d1-124">Définition du privilège de l’utilisateur, niveau 1005</span><span class="sxs-lookup"><span data-stu-id="898d1-124">Setting the User Privilege, Level 1005</span></span>

<span data-ttu-id="898d1-125">Le fragment de code suivant montre comment spécifier le niveau de privilège affecté à un utilisateur avec un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="898d1-125">The following code fragment illustrates how to specify the level of privilege assigned to a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="898d1-126">La [**rubrique \_ informations utilisateur \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) contient des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="898d1-126">The [**USER\_INFO\_1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) topic contains additional information.</span></span> <span data-ttu-id="898d1-127">Pour plus d’informations sur les privilèges de compte, consultez [privilèges](/windows/desktop/SecAuthZ/privileges) et [constantes d’autorisation](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="898d1-127">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>


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



## <a name="setting-the-user-home-directory-level-1006"></a><span data-ttu-id="898d1-128">Définition du répertoire de démarrage de l’utilisateur, niveau 1006</span><span class="sxs-lookup"><span data-stu-id="898d1-128">Setting the User Home Directory, Level 1006</span></span>

<span data-ttu-id="898d1-129">Le fragment de code suivant montre comment spécifier le chemin d’accès du répertoire de départ d’un utilisateur à l’aide d’un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="898d1-129">The following code fragment illustrates how to specify the path of a user's home directory with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="898d1-130">Le répertoire peut être un chemin d’accès codé en dur ou un chemin d’accès Unicode valide.</span><span class="sxs-lookup"><span data-stu-id="898d1-130">The directory can be a hard-coded path or a valid Unicode path.</span></span> <span data-ttu-id="898d1-131">La [**rubrique \_ informations utilisateur \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) contient des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="898d1-131">The [**USER\_INFO\_1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) topic contains additional information.</span></span>


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



## <a name="setting-the-user-comment-field-level-1007"></a><span data-ttu-id="898d1-132">Définition du champ de commentaire de l’utilisateur, niveau 1007</span><span class="sxs-lookup"><span data-stu-id="898d1-132">Setting the User Comment Field, Level 1007</span></span>

<span data-ttu-id="898d1-133">Le fragment de code suivant illustre comment associer un commentaire à un utilisateur en appelant la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="898d1-133">The following code fragment illustrates how to associate a comment with a user by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="898d1-134">La [**rubrique \_ informations utilisateur \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) contient des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="898d1-134">The [**USER\_INFO\_1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) topic contains additional information.</span></span>


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



## <a name="setting-the-user-flags-level-1008"></a><span data-ttu-id="898d1-135">Définition des indicateurs utilisateur, niveau 1008</span><span class="sxs-lookup"><span data-stu-id="898d1-135">Setting the User Flags, Level 1008</span></span>

<span data-ttu-id="898d1-136">Le fragment de code suivant montre comment définir des indicateurs utilisateur avec un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="898d1-136">The following code fragment illustrates how to set user flags with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="898d1-137">La [**rubrique \_ informations utilisateur \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) contient une liste de valeurs valides pour les indicateurs et une description de chaque indicateur.</span><span class="sxs-lookup"><span data-stu-id="898d1-137">The [**USER\_INFO\_1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) topic contains a list of valid values for the flags and a description of each flag.</span></span>

<span data-ttu-id="898d1-138">Notez que l' \_ indicateur de script UF doit être défini pour les réseaux Windows NT, windows 2000, Windows XP et LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="898d1-138">Note that the UF\_SCRIPT flag must be set for Windows NT, Windows 2000, Windows XP, and LAN Manager networks.</span></span> <span data-ttu-id="898d1-139">Si vous tentez de définir d’autres indicateurs sans définir \_ le script UF sur ces réseaux, la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) échouera.</span><span class="sxs-lookup"><span data-stu-id="898d1-139">Trying to set other flags without setting UF\_SCRIPT on these networks will cause the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function to fail.</span></span>


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



## <a name="setting-the-user-script-path-level-1009"></a><span data-ttu-id="898d1-140">Définition du chemin d’accès au script utilisateur, niveau 1009</span><span class="sxs-lookup"><span data-stu-id="898d1-140">Setting the User Script Path, Level 1009</span></span>

<span data-ttu-id="898d1-141">Le fragment de code suivant montre comment définir le chemin d’accès pour le fichier de script d’ouverture de session d’un utilisateur particulier à l’aide d’un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="898d1-141">The following code fragment illustrates how to set the path for the logon script file of a particular user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="898d1-142">Le fichier de script peut être. Fichier CMD,. Fichier EXE ou. Fichier BAT.</span><span class="sxs-lookup"><span data-stu-id="898d1-142">The script file can be a .CMD file, an .EXE file, or a .BAT file.</span></span> <span data-ttu-id="898d1-143">La chaîne peut également avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="898d1-143">The string can also be null.</span></span> <span data-ttu-id="898d1-144">La [**rubrique \_ informations utilisateur \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) contient des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="898d1-144">The [**USER\_INFO\_1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) topic contains additional information.</span></span>


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



## <a name="setting-the-user-authority-flags-level-1010"></a><span data-ttu-id="898d1-145">Définition des indicateurs de l’autorité de l’utilisateur, niveau 1010</span><span class="sxs-lookup"><span data-stu-id="898d1-145">Setting The User Authority Flags, Level 1010</span></span>

<span data-ttu-id="898d1-146">Le fragment de code suivant montre comment définir les indicateurs de privilège d’opérateur pour un utilisateur avec un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="898d1-146">The following code fragment illustrates how to set the operator privilege flags for a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="898d1-147">La [**rubrique \_ informations utilisateur \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) contient une liste de valeurs valides pour les indicateurs et une description de chaque indicateur.</span><span class="sxs-lookup"><span data-stu-id="898d1-147">The [**USER\_INFO\_1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) topic contains a list of valid values for the flags and a description of each flag.</span></span>


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



## <a name="setting-the-user-full-name-level-1011"></a><span data-ttu-id="898d1-148">Définition du nom complet de l’utilisateur, niveau 1011</span><span class="sxs-lookup"><span data-stu-id="898d1-148">Setting The User Full Name, Level 1011</span></span>

<span data-ttu-id="898d1-149">Le fragment de code suivant montre comment définir le nom complet d’un utilisateur à l’aide d’un appel à la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="898d1-149">The following code fragment illustrates how to set a user's full name with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="898d1-150">La [**rubrique \_ informations utilisateur \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) contient des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="898d1-150">The [**USER\_INFO\_1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) topic contains additional information.</span></span>


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



 

 