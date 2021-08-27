---
description: à partir de Windows Vista, de nombreux objets sécurisables possèdent des méthodes pour obtenir ou définir le descripteur de sécurité. Avec les autorisations appropriées, vous pouvez lire ou modifier les descripteurs de sécurité des objets sécurisables.
ms.assetid: da660e7e-f32d-4b7d-b979-f7b482a73fa2
ms.tgt_platform: multiple
title: Modification de la sécurité d’accès sur les objets sécurisables
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4cdaa948e6f0e695b3e77576b0a0726f0b38f3b649f005b42aa8e205c894db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050987"
---
# <a name="changing-access-security-on-securable-objects"></a>Modification de la sécurité d’accès sur les objets sécurisables

Les imprimantes, les services, les clés de Registre, les applications DCOM et les espaces de noms WMI sont des objets sécurisables. L’accès aux objets sécurisables est protégé par les [*descripteurs de sécurité*](/windows/desktop/SecGloss/s-gly), qui spécifient les utilisateurs qui ont accès. à partir de Windows Vista, de nombreux objets sécurisables possèdent des méthodes pour obtenir ou définir le descripteur de sécurité. Avec les autorisations appropriées, vous pouvez lire ou modifier les descripteurs de sécurité des objets sécurisables. À l’aide de ces méthodes, vous pouvez contrôler les comptes d’utilisateur ou les groupes qui ont accès à une imprimante, un service, un espace de noms WMI ou un autre objet. Pour plus d’informations sur les descripteurs de sécurité et leur utilisation dans WMI, consultez [accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md).

Les sections suivantes sont présentées dans cette rubrique :

-   [Objets et méthodes de descripteur de sécurité](#objects-and-security-descriptor-methods)
-   [Conversion entre des formats de descripteurs de sécurité](#converting-between-security-descriptor-formats)
-   [Problèmes de sécurité](#security-issues)
-   [Rubriques connexes](#related-topics)

## <a name="objects-and-security-descriptor-methods"></a>Objets et méthodes de descripteur de sécurité

La liste suivante contient les méthodes dont les objets sécurisables ont besoin pour vous permettre de lire ou de modifier le descripteur de sécurité :

-   Espaces de noms WMI

    Un fournisseur peut établir une sécurité qui permet uniquement à certains groupes d’avoir accès aux données d’un espace de noms WMI. La sécurité de l’espace de noms est contrôlée par des méthodes sur la classe [**\_ \_ SystemSecurity**](--systemsecurity.md) . à partir de Windows Vista, les méthodes [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) et [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) retournent et écrivent des objets [**\_ \_ SecurityDescriptor**](--securitydescriptor.md) . Pour plus d’informations, consultez [définition des descripteurs de sécurité des espaces de noms](setting-namespace-security-descriptors.md).

-   les clés de Registre

    à partir de Windows Vista, vous pouvez sécuriser les clés de registre afin qu’elles ne puissent pas être modifiées par des utilisateurs non autorisés. La classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) a les méthodes [**GetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/getsecuritydescriptor-method-in-class-stdregprov) et [**SetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/setsecuritydescriptor-method-in-class-stdregprov) . Ces méthodes retournent et écrivent des objets [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Imprimantes

    à partir de Windows Vista, vous pouvez sécuriser l’accès aux instances de la classe [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) à l’aide des méthodes [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) et [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) . Ces méthodes retournent et écrivent des objets [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Services

    à partir de Windows Vista, vous pouvez sécuriser l’accès aux instances de la classe de [**\_ Service Win32**](/windows/desktop/CIMWin32Prov/win32-service) à l’aide des méthodes [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) et [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) . Ces méthodes retournent et écrivent des objets [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Applications DCOM

    Les instances d’application DCOM comportent plusieurs descripteurs de sécurité. à partir de Windows Vista, utilisez les méthodes de la classe [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting) pour récupérer ou modifier les différents descripteurs de sécurité. Les descripteurs de sécurité sont retournés en tant qu’instances de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

    Pour récupérer ou modifier les autorisations de configuration, appelez les méthodes [**GetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) ou [**SetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) .

    Pour récupérer ou modifier les autorisations d’accès, appelez les méthodes [**GetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) ou [**SetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) .

    Pour récupérer ou modifier les autorisations de démarrage et d’activation, appelez les méthodes [**GetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting) ou [**SetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) ,

-   Fichiers

    Les méthodes [**GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) et [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) se trouvent dans la classe [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) , plutôt que dans la classe de [**fichier de \_ fichier CIM**](/windows/desktop/CIMWin32Prov/cim-datafile) .

-   Partages

    Les méthodes [**GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) et [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) se trouvent dans la classe [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) , plutôt que dans la classe de [**\_ partage Win32**](/windows/desktop/CIMWin32Prov/win32-share) .

> [!Note]  
> Lorsqu’une nouvelle [*liste de Access Control de sécurité (SACL)*](/windows/desktop/SecGloss/s-gly) n’est pas spécifiée dans un appel à une méthode **SetSecurityDescriptor** , alors le descripteur de sécurité SACL de l’objet sécurisable cible a la valeur **null** afin que le paramètre SACL précédent ne soit pas conservé.

 

## <a name="converting-between-security-descriptor-formats"></a>Conversion entre des formats de descripteurs de sécurité

Les descripteurs de sécurité sont des tableaux d’octets binaires complexes qui doivent normalement être créés et modifiés en C++. Une fois que vous avez utilisé l’une des méthodes d’obtention pour obtenir le descripteur de sécurité, la classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) fournit des méthodes qui convertissent les descripteurs de sécurité en [langage SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ou en instances de [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

Vous pouvez manipuler les listes de Access Control (ACL) plus facilement dans des instances [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ou dans des langages SDDL. Pour plus d’informations sur la structure et l’utilisation des descripteurs de sécurité dans WMI, consultez objets descripteurs de [sécurité WMI](wmi-security-descriptor-objects.md).

En C++ ou C#, utilisez les fonctions de conversion pour convertir les descripteurs de sécurité binaires en [langage SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Pour modifier les valeurs du descripteur de sécurité dans les applications C++, utilisez [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="security-issues"></a>Problèmes de sécurité

Il est recommandé que les modifications apportées aux descripteurs de sécurité soient effectuées avec une grande prudence afin que la sécurité de l’objet ne soit pas compromise. Sachez que l’ordre des entrées de contrôle d’accès (ACE) dans une liste de contrôle d’accès discrétionnaire (DACL) peut affecter la sécurité d’accès. Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Classe d’assistance du descripteur de sécurité](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Meilleures pratiques de sécurité](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> <dt>

[Access Control](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
