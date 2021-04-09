---
description: Montre comment créer correctement une liste DACL.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Création d’une liste DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf8213f6fbb4e2a885655b47437ec464337ea13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868218"
---
# <a name="creating-a-dacl"></a><span data-ttu-id="8d4a1-103">Création d’une liste DACL</span><span class="sxs-lookup"><span data-stu-id="8d4a1-103">Creating a DACL</span></span>

<span data-ttu-id="8d4a1-104">La création d’une [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) appropriée est une partie importante et essentielle du développement d’applications.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-104">Creating a proper [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) is a necessary and important part of application development.</span></span> <span data-ttu-id="8d4a1-105">Étant donné qu’une liste DACL **null** autorise tous les types d’accès à tous les utilisateurs, n’utilisez pas de DACL **null** .</span><span class="sxs-lookup"><span data-stu-id="8d4a1-105">Because a **NULL** DACL permits all types of access to all users, do not use **NULL** DACLs.</span></span>

<span data-ttu-id="8d4a1-106">L’exemple suivant montre comment créer correctement une liste DACL.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-106">The following example shows how to properly create a DACL.</span></span> <span data-ttu-id="8d4a1-107">L’exemple contient une fonction, CreateMyDACL, qui utilise le [langage SDDL (Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ) pour définir le contrôle d’accès accordé et refusé dans une liste DACL.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-107">The example contains a function, CreateMyDACL, that uses the [security descriptor definition language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) to define the granted and denied access control in a DACL.</span></span> <span data-ttu-id="8d4a1-108">Pour fournir un accès différent pour les objets de votre application, modifiez la fonction CreateMyDACL si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-108">To provide different access for your application's objects, modify the CreateMyDACL function as needed.</span></span>

<span data-ttu-id="8d4a1-109">Dans l’exemple :</span><span class="sxs-lookup"><span data-stu-id="8d4a1-109">In the example:</span></span>

1.  <span data-ttu-id="8d4a1-110">La fonction main passe une adresse d’une structure d' [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) à la fonction CreateMyDACL.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-110">The main function passes an address of a [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to the CreateMyDACL function.</span></span>
2.  <span data-ttu-id="8d4a1-111">La fonction CreateMyDACL utilise des chaînes SDDL pour :</span><span class="sxs-lookup"><span data-stu-id="8d4a1-111">The CreateMyDACL function uses SDDL strings to:</span></span>
    -   <span data-ttu-id="8d4a1-112">Refuser l’accès aux utilisateurs invités et anonymes.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-112">Deny access to guest and anonymous logon users.</span></span>
    -   <span data-ttu-id="8d4a1-113">Autorise l’accès en lecture/écriture/exécution aux utilisateurs authentifiés.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-113">Allow read/write/execute access to authenticated users.</span></span>
    -   <span data-ttu-id="8d4a1-114">Autorisez le contrôle total pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-114">Allow full control to administrators.</span></span>

    <span data-ttu-id="8d4a1-115">Pour plus d’informations sur les formats de chaîne SDDL, consultez [format de chaîne de descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="8d4a1-115">For more information about the SDDL string formats, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>
3.  <span data-ttu-id="8d4a1-116">La fonction CreateMyDACL appelle la fonction [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) pour convertir les chaînes SDDL en [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="8d4a1-116">The CreateMyDACL function calls the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL strings to a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="8d4a1-117">Le descripteur de sécurité est désigné par le membre **lpSecurityDescriptor** de la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8d4a1-117">The security descriptor is pointed to by the **lpSecurityDescriptor** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="8d4a1-118">CreateMyDACL envoie la valeur de retour de **convertstringsecuritydescriptortosecuritydescriptor a** à la fonction main.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-118">CreateMyDACL sends the return value from **ConvertStringSecurityDescriptorToSecurityDescriptor** to the main function.</span></span>
4.  <span data-ttu-id="8d4a1-119">La fonction main utilise la structure [**d' \_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) mise à jour pour spécifier la liste DACL d’un nouveau dossier créé par la fonction [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="8d4a1-119">The main function uses the updated [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to specify the DACL for a new folder that is created by the [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) function.</span></span>
5.  <span data-ttu-id="8d4a1-120">Lorsque la fonction main est terminée à l’aide de la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , la fonction main libère la mémoire allouée pour le membre **lpSecurityDescriptor** en appelant la fonction [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .</span><span class="sxs-lookup"><span data-stu-id="8d4a1-120">When the main function is finished using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure, the main function frees the memory allocated for the **lpSecurityDescriptor** member by calling the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="8d4a1-121">Pour compiler correctement des fonctions SDDL comme [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), vous devez définir la \_ \_ constante Win32 Winnt sur 0x0500 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8d4a1-121">To successfully compile SDDL functions such as [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), you must define the \_WIN32\_WINNT constant as 0x0500 or greater.</span></span>

 


```C++
#define _WIN32_WINNT 0x0500

#include <windows.h>
#include <sddl.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

BOOL CreateMyDACL(SECURITY_ATTRIBUTES *);

void main()
{
     SECURITY_ATTRIBUTES  sa;
      
     sa.nLength = sizeof(SECURITY_ATTRIBUTES);
     sa.bInheritHandle = FALSE;  

     // Call function to set the DACL. The DACL
     // is set in the SECURITY_ATTRIBUTES 
     // lpSecurityDescriptor member.
     if (!CreateMyDACL(&sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateMyDACL\n");
         exit(1);
     }

     // Use the updated SECURITY_ATTRIBUTES to specify
     // security attributes for securable objects.
     // This example uses security attributes during
     // creation of a new directory.
     if (0 == CreateDirectory(TEXT("C:\\MyFolder"), &sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateDirectory\n");
         exit(1);
     }

     // Free the memory allocated for the SECURITY_DESCRIPTOR.
     if (NULL != LocalFree(sa.lpSecurityDescriptor))
     {
         // Error encountered; generate message and exit.
         printf("Failed LocalFree\n");
         exit(1);
     }
}


// CreateMyDACL.
//    Create a security descriptor that contains the DACL 
//    you want.
//    This function uses SDDL to make Deny and Allow ACEs.
//
// Parameter:
//    SECURITY_ATTRIBUTES * pSA
//    Pointer to a SECURITY_ATTRIBUTES structure. It is your
//    responsibility to properly initialize the 
//    structure and to free the structure's 
//    lpSecurityDescriptor member when you have
//    finished using it. To free the structure's 
//    lpSecurityDescriptor member, call the 
//    LocalFree function.
// 
// Return value:
//    FALSE if the address to the structure is NULL. 
//    Otherwise, this function returns the value from the
//    ConvertStringSecurityDescriptorToSecurityDescriptor 
//    function.
BOOL CreateMyDACL(SECURITY_ATTRIBUTES * pSA)
{
     // Define the SDDL for the DACL. This example sets 
     // the following access:
     //     Built-in guests are denied all access.
     //     Anonymous logon is denied all access.
     //     Authenticated users are allowed 
     //     read/write/execute access.
     //     Administrators are allowed full control.
     // Modify these values as needed to generate the proper
     // DACL for your application. 
     TCHAR * szSD = TEXT("D:")       // Discretionary ACL
        TEXT("(D;OICI;GA;;;BG)")     // Deny access to 
                                     // built-in guests
        TEXT("(D;OICI;GA;;;AN)")     // Deny access to 
                                     // anonymous logon
        TEXT("(A;OICI;GRGWGX;;;AU)") // Allow 
                                     // read/write/execute 
                                     // to authenticated 
                                     // users
        TEXT("(A;OICI;GA;;;BA)");    // Allow full control 
                                     // to administrators

    if (NULL == pSA)
        return FALSE;

     return ConvertStringSecurityDescriptorToSecurityDescriptor(
                szSD,
                SDDL_REVISION_1,
                &(pSA->lpSecurityDescriptor),
                NULL);
}
```



 

 
