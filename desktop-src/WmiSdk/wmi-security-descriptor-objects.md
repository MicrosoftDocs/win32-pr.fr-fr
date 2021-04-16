---
description: WMI a des objets et des méthodes qui vous permettent de lire et manipuler les descripteurs de sécurité pour déterminer qui a accès aux objets sécurisables.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Objets descripteurs de sécurité WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550399"
---
# <a name="wmi-security-descriptor-objects"></a>Objets descripteurs de sécurité WMI

WMI a des objets et des méthodes qui vous permettent de lire et manipuler les descripteurs de sécurité pour déterminer qui a accès aux objets sécurisables.

-   [Rôle des descripteurs de sécurité](#the-role-of-security-descriptors)
-   [Objets de sécurité Access Control et WMI](#access-control-and-wmi-security-objects)
-   [\_Objet Win32 SecurityDescriptor](/windows)
-   [DACL et SACL](#dacl-and-sacl)
-   [\_ACE Win32, \_ approuvé Win32, \_ sid Win32](/windows)
-   [Exemple : vérification de l’accès aux imprimantes](#example-checking-who-has-access-to-printers)
-   [Rubriques connexes](#related-topics)

## <a name="the-role-of-security-descriptors"></a>Rôle des descripteurs de sécurité

Les descripteurs de sécurité définissent les attributs de sécurité des objets sécurisables tels que les fichiers, les clés de Registre, les espaces de noms WMI, les imprimantes, les services ou les partages. Un descripteur de sécurité contient des informations sur le propriétaire et le groupe principal d’un objet. Un fournisseur peut comparer le descripteur de sécurité des ressources à l’identité d’un utilisateur demandeur et déterminer si l’utilisateur a le droit d’accéder à la ressource demandée par un utilisateur. Pour plus d’informations, consultez [accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md).

Certaines méthodes WMI, telles que [**est**](--systemsecurity-getsd.md), retournent un descripteur de sécurité dans le format de tableau d’octets binaire. À compter de Windows Vista, utilisez les méthodes de la classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) pour convertir un descripteur de sécurité binaire en une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), qui peut être manipulée plus facilement. Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).

## <a name="access-control-and-wmi-security-objects"></a>Objets de sécurité Access Control et WMI

La liste suivante répertorie les objets de sécurité WMI :

-   [**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [**\_Confiance Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [**\_Sid Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

Le diagramme suivant montre les relations entre les objets de sécurité WMI.

![relations entre les objets de sécurité WMI](images/security-descriptor.png)

Pour plus d’informations sur le rôle de sécurité d’accès, consultez [meilleures pratiques de sécurité](/windows/desktop/SecBP/best-practices-for-the-security-apis), [maintenance de la sécurité WMI](maintaining-wmi-security.md)et [Access Control](/windows/desktop/SecAuthZ/access-control).

## <a name="win32_securitydescriptor-object"></a>\_Objet Win32 SecurityDescriptor

Le tableau suivant répertorie les propriétés de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .



| Propriété         | Description                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ControlFlags** | Ensemble de bits de contrôle qui qualifient la signification d’un SD ou de ses membres individuels. Pour plus d’informations sur la définition des valeurs de bit **ControlFlags** , consultez [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).<br/>                                                                                                                                                                      |
| **DACL**         | [Liste de Access Control discrétionnaire (ACL)](/windows/desktop/SecAuthZ/access-control-lists) d’utilisateurs et de groupes et leurs droits d’accès à un objet sécurisé. Cette propriété contient un tableau d’instances de l' [**\_ entrée**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) de contrôle d’accès Win32 qui représentent les [entrées Access Control](/windows/desktop/SecAuthZ/access-control-entries). Pour plus d’informations, consultez [création d’une liste DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).<br/> |
| **Groupe**        | Groupe auquel appartient cet objet sécurisé. Cette propriété contient une instance de [**l' \_ approbation Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) qui contient le nom, le domaine et l’identificateur de sécurité (SID) du groupe auquel appartient le propriétaire.<br/>                                                                                                                                                             |
| **Propriétaire**        | Propriétaire de cet objet sécurisé. Cette propriété contient une instance de [l' \_ approbation Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) qui contient le nom, le domaine et l’identificateur de sécurité (SID) du propriétaire.<br/>                                                                                                                                                                                                          |
| **SACL**         | La [liste de Access Control système (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contient un tableau d’instances de [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) qui représentent le type de tentatives d’accès qui génèrent des enregistrements d’audit pour les utilisateurs ou les groupes. Pour plus d’informations, consultez [SACL pour un nouvel objet](/windows/desktop/SecAuthZ/sacl-for-a-new-object).<br/>                                                                        |



 

## <a name="dacl-and-sacl"></a>DACL et SACL

Les tableaux d’objets [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) de la liste de contrôle d’accès discrétionnaire (DACL) et de la liste de contrôle d’accès système {SACL) créent un lien entre un utilisateur ou un groupe et leurs droits d’accès.

Lorsqu’une propriété DACL ne contient pas d’entrée de contrôle d’accès (ACE), les droits d’accès ne sont pas accordés et l’accès à l’objet est refusé.

> [!Note]  
> Une liste DACL **null** accorde un accès complet à tout le monde, ce qui constitue un risque sérieux pour la sécurité. Pour plus d’informations, consultez [création d’une liste DACL](/windows/desktop/SecBP/creating-a-dacl).

 

## <a name="win32_ace-win32_trustee-win32_sid"></a>\_ACE Win32, \_ approuvé Win32, \_ sid Win32

Un [**objet \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) contient une instance de la classe [**Win32 \_ Trusted**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) qui identifie un utilisateur ou un groupe, et une propriété **AccessMask** qui est un masque de masque, qui spécifie les actions qu’un utilisateur ou un groupe peut effectuer. Par exemple, un utilisateur ou un groupe peut se voir accorder le droit de lire un fichier, mais pas d’écrire dans le fichier. Un **objet \_ ACE Win32** contient également un ACE qui indique s’il s’agit d’un accès Allow ou Deny.

> [!Note]  
> L’ordre des entrées de contrôle d’accès [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) dans une liste DACL est important, car l’entrée de contrôle d’accès Allow et Deny est autorisée dans une liste DACL. Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

Chaque compte d’utilisateur ou groupe représenté par [**un \_ tiers de confiance Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) possède un identificateur de sécurité (SID) qui identifie de manière unique un compte, et spécifie les privilèges d’accès du compte. La façon dont vous spécifiez les données SID dépend du système d’exploitation. Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).

Le diagramme suivant montre le contenu d’une instance de l' [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

![contenu d’une \- instance ACE Win32](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a>Exemple : vérification de l’accès aux imprimantes

L’exemple de code VBScript suivant montre comment utiliser le descripteur de sécurité de l’imprimante. Le script appelle la méthode [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) dans la classe [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) pour obtenir le descripteur, puis détermine s’il existe une liste de Access Control discrétionnaire (DACL) présente dans le descripteur de sécurité. S’il existe une liste de contrôle d’accès discrétionnaire, le script obtient la liste des entrées de Access Control (ACE) à partir de la liste DACL. Chaque ACE est représenté par une instance de [**l' \_ entrée**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)du contrôle d’accès Win32. Le script vérifie chaque ACE pour obtenir le nom de l’utilisateur et détermine si l’utilisateur a accès à l’imprimante. L’utilisateur est représenté par une instance de [**\_ confiance Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) incorporée dans l' **instance \_ ACE Win32** .


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md)
</dt> <dt>

[Classe d’assistance du descripteur de sécurité](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Meilleures pratiques de sécurité](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> <dt>

[Contrôle d’accès](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

