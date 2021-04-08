---
description: L’activation d’un privilège dans un jeton d’accès permet au processus d’effectuer des actions au niveau du système qu’il ne pouvait pas avoir précédemment.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Activation et désactivation des privilèges en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354f3ac2b27a7c027bd7c48e753263c43b676dd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035011"
---
# <a name="enabling-and-disabling-privileges-in-c"></a><span data-ttu-id="f4b6e-103">Activation et désactivation des privilèges en C++</span><span class="sxs-lookup"><span data-stu-id="f4b6e-103">Enabling and Disabling Privileges in C++</span></span>

<span data-ttu-id="f4b6e-104">L’activation d’un privilège dans un jeton d’accès permet au processus d’effectuer des actions au niveau du système qu’il ne pouvait pas avoir précédemment.</span><span class="sxs-lookup"><span data-stu-id="f4b6e-104">Enabling a privilege in an access token allows the process to perform system-level actions that it could not previously.</span></span> <span data-ttu-id="f4b6e-105">Votre application doit vérifier minutieusement que le privilège est approprié au type de compte, en particulier pour les privilèges puissants suivants.</span><span class="sxs-lookup"><span data-stu-id="f4b6e-105">Your application should thoroughly verify that the privilege is appropriate to the type of account, especially for the following powerful privileges.</span></span>



| <span data-ttu-id="f4b6e-106">Privilège, constante</span><span class="sxs-lookup"><span data-stu-id="f4b6e-106">Privilege constant</span></span>           | <span data-ttu-id="f4b6e-107">Valeur de chaîne</span><span class="sxs-lookup"><span data-stu-id="f4b6e-107">String value</span></span>                  | <span data-ttu-id="f4b6e-108">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="f4b6e-108">Display name</span></span>                        |
|------------------------------|-------------------------------|-------------------------------------|
| <span data-ttu-id="f4b6e-109">nom de la \_ ASSIGNPRIMARYTOKEN se \_</span><span class="sxs-lookup"><span data-stu-id="f4b6e-109">SE\_ASSIGNPRIMARYTOKEN\_NAME</span></span> | <span data-ttu-id="f4b6e-110">SeAssignPrimaryTokenPrivilege</span><span class="sxs-lookup"><span data-stu-id="f4b6e-110">SeAssignPrimaryTokenPrivilege</span></span> | <span data-ttu-id="f4b6e-111">Remplacer un jeton de niveau processus</span><span class="sxs-lookup"><span data-stu-id="f4b6e-111">Replace a process-level token</span></span>       |
| <span data-ttu-id="f4b6e-112">nom de la sauvegarde de SE \_ \_</span><span class="sxs-lookup"><span data-stu-id="f4b6e-112">SE\_BACKUP\_NAME</span></span>             | <span data-ttu-id="f4b6e-113">SeBackupPrivilege</span><span class="sxs-lookup"><span data-stu-id="f4b6e-113">SeBackupPrivilege</span></span>             | <span data-ttu-id="f4b6e-114">Sauvegarder des fichiers et des répertoires</span><span class="sxs-lookup"><span data-stu-id="f4b6e-114">Back up files and directories</span></span>       |
| <span data-ttu-id="f4b6e-115">\_nom de débogage de se \_</span><span class="sxs-lookup"><span data-stu-id="f4b6e-115">SE\_DEBUG\_NAME</span></span>              | <span data-ttu-id="f4b6e-116">SeDebugPrivilege</span><span class="sxs-lookup"><span data-stu-id="f4b6e-116">SeDebugPrivilege</span></span>              | <span data-ttu-id="f4b6e-117">Déboguer les programmes</span><span class="sxs-lookup"><span data-stu-id="f4b6e-117">Debug programs</span></span>                      |
| <span data-ttu-id="f4b6e-118">\_augmenter le \_ nom du quota \_</span><span class="sxs-lookup"><span data-stu-id="f4b6e-118">SE\_INCREASE\_QUOTA\_NAME</span></span>    | <span data-ttu-id="f4b6e-119">SeIncreaseQuotaPrivilege</span><span class="sxs-lookup"><span data-stu-id="f4b6e-119">SeIncreaseQuotaPrivilege</span></span>      | <span data-ttu-id="f4b6e-120">Ajuster les quotas de mémoire pour un processus</span><span class="sxs-lookup"><span data-stu-id="f4b6e-120">Adjust memory quotas for a process</span></span>  |
| <span data-ttu-id="f4b6e-121">\_nom TCB du se \_</span><span class="sxs-lookup"><span data-stu-id="f4b6e-121">SE\_TCB\_NAME</span></span>                | <span data-ttu-id="f4b6e-122">SeTcbPrivilege</span><span class="sxs-lookup"><span data-stu-id="f4b6e-122">SeTcbPrivilege</span></span>                | <span data-ttu-id="f4b6e-123">Agir en tant que partie du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="f4b6e-123">Act as part of the operating system</span></span> |



 

<span data-ttu-id="f4b6e-124">Avant d’activer l’un de ces privilèges potentiellement dangereux, déterminez que les fonctions ou opérations de votre code nécessitent réellement les privilèges.</span><span class="sxs-lookup"><span data-stu-id="f4b6e-124">Before enabling any of these potentially dangerous privileges, determine that functions or operations in your code actually require the privileges.</span></span> <span data-ttu-id="f4b6e-125">Par exemple, très peu de fonctions du système d’exploitation nécessitent en fait le **SeTcbPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="f4b6e-125">For example, very few functions in the operating system actually require the **SeTcbPrivilege**.</span></span> <span data-ttu-id="f4b6e-126">Pour obtenir la liste de tous les privilèges disponibles, consultez [constantes de privilège](authorization-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f4b6e-126">For a list of all the available privileges, see [Privilege Constants](authorization-constants.md).</span></span>

<span data-ttu-id="f4b6e-127">L’exemple suivant montre comment activer ou désactiver un privilège dans un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="f4b6e-127">The following example shows how to enable or disable a privilege in an [*access token*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="f4b6e-128">L’exemple appelle la fonction [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) pour récupérer l' [*identificateur unique local*](/windows/desktop/SecGloss/l-gly) (LUID) que le système local utilise pour identifier le privilège.</span><span class="sxs-lookup"><span data-stu-id="f4b6e-128">The example calls the [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) function to get the [*locally unique identifier*](/windows/desktop/SecGloss/l-gly) (LUID) that the local system uses to identify the privilege.</span></span> <span data-ttu-id="f4b6e-129">L’exemple appelle ensuite la fonction [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , qui active ou désactive le privilège qui dépend de la valeur du paramètre *bEnablePrivilege* .</span><span class="sxs-lookup"><span data-stu-id="f4b6e-129">Then the example calls the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function, which either enables or disables the privilege that depends on the value of the *bEnablePrivilege* parameter.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 

