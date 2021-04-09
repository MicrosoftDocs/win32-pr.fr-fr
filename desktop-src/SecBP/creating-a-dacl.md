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
# <a name="creating-a-dacl"></a>Création d’une liste DACL

La création d’une [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) appropriée est une partie importante et essentielle du développement d’applications. Étant donné qu’une liste DACL **null** autorise tous les types d’accès à tous les utilisateurs, n’utilisez pas de DACL **null** .

L’exemple suivant montre comment créer correctement une liste DACL. L’exemple contient une fonction, CreateMyDACL, qui utilise le [langage SDDL (Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ) pour définir le contrôle d’accès accordé et refusé dans une liste DACL. Pour fournir un accès différent pour les objets de votre application, modifiez la fonction CreateMyDACL si nécessaire.

Dans l’exemple :

1.  La fonction main passe une adresse d’une structure d' [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) à la fonction CreateMyDACL.
2.  La fonction CreateMyDACL utilise des chaînes SDDL pour :
    -   Refuser l’accès aux utilisateurs invités et anonymes.
    -   Autorise l’accès en lecture/écriture/exécution aux utilisateurs authentifiés.
    -   Autorisez le contrôle total pour les administrateurs.

    Pour plus d’informations sur les formats de chaîne SDDL, consultez [format de chaîne de descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-string-format).
3.  La fonction CreateMyDACL appelle la fonction [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) pour convertir les chaînes SDDL en [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly). Le descripteur de sécurité est désigné par le membre **lpSecurityDescriptor** de la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . CreateMyDACL envoie la valeur de retour de **convertstringsecuritydescriptortosecuritydescriptor a** à la fonction main.
4.  La fonction main utilise la structure [**d' \_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) mise à jour pour spécifier la liste DACL d’un nouveau dossier créé par la fonction [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) .
5.  Lorsque la fonction main est terminée à l’aide de la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , la fonction main libère la mémoire allouée pour le membre **lpSecurityDescriptor** en appelant la fonction [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .

> [!Note]  
> Pour compiler correctement des fonctions SDDL comme [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), vous devez définir la \_ \_ constante Win32 Winnt sur 0x0500 ou une version ultérieure.

 


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



 

 
