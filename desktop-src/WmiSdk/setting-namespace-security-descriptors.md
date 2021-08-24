---
description: Les applications C++ et les scripts s’exécutant sous un compte d’administrateur complet peuvent modifier un descripteur de sécurité d’espace de noms.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Définition des descripteurs de sécurité des espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc112376a960c3760bc51450cc30b8da3a38c24fa52e985321b2662ae319a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050297"
---
# <a name="setting-namespace-security-descriptors"></a>Définition des descripteurs de sécurité des espaces de noms

Les applications C++ et les scripts s’exécutant sous un compte d’administrateur complet peuvent modifier un descripteur de sécurité d’espace de noms.

## <a name="namespace-security-descriptors"></a>Descripteurs de sécurité des espaces de noms

Chaque espace de noms WMI possède un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)qui permet à chaque espace de noms d’avoir des paramètres de sécurité uniques qui déterminent qui a accès aux données et méthodes de l’espace de noms. Pour plus d’informations sur la sécurité d’accès WMI, consultez [accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md). [Accès aux espaces de noms WMI](access-to-wmi-namespaces.md) décrit les paramètres de sécurité par défaut pour les espaces de noms WMI et l’audit de sécurité dans WMI.

Vous pouvez définir des autorisations de compte pour chaque espace de noms WMI dans le référentiel WMI (CIM) de l’une des manières suivantes :

-   Lorsque l’espace de noms est créé dans le fichier MOF. Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms lors de la création de l’espace de noms](setting-namespace-security-when-the-namespace-is-created.md).
-   Manuellement, à l’aide du contrôle WMI. Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).
-   Par programmation, en appelant les méthodes de la classe [**\_ \_ SystemSecurity**](--systemsecurity.md) .

Les méthodes suivantes de l’objet [**\_ \_ SystemSecurity**](--systemsecurity.md) associé à chaque espace de noms vous permettent de lire ou de modifier la sécurité sur un espace de noms.

<dl> <dt>

<span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)
</dt> <dd>

Définit le paramètre *Rights* en tant que bitmap avec chaque bit correspondant à un droit d’accès.

</dd> <dt>

<span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**Getsd a**](--systemsecurity-getsd.md)
</dt> <dd>

Obtient le descripteur de sécurité pour l’espace de noms auquel l’utilisateur est connecté. Cette méthode retourne un descripteur de sécurité au format de tableau d’octets binaire. Si vous écrivez un script, utilisez la méthode [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .

</dd> <dt>

<span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**Setsd a**](--systemsecurity-setsd.md)
</dt> <dd>

Définit le descripteur de sécurité (SD) pour l’espace de noms auquel un utilisateur est connecté. Cette méthode requiert un descripteur de sécurité au format de tableau d’octets binaire. Si vous écrivez un script, utilisez la méthode [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .

</dd> <dt>

<span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)
</dt> <dd>

Obtient le descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI associé à l’instance de [**\_ \_ SystemSecurity**](--systemsecurity.md). Le descripteur de sécurité est retourné en tant qu’instance de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)
</dt> <dd>

Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante. Le descripteur de sécurité est représenté par une instance de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)
</dt> <dd>

obtient les droits d’accès à distance pour une liste d’utilisateurs individuels sur les ordinateurs qui exécutent des versions obsolètes de Windows, où le contrôle d’accès via Windows descripteurs de sécurité n’est pas disponible.

</dd> <dt>

<span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)
</dt> <dd>

définit les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès via Windows descripteurs de sécurité n’est pas disponible.

</dd> </dl>

Si vous écrivez des scripts, utilisez [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) et [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md). Vous pouvez utiliser les méthodes de la classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) pour modifier les descripteurs de sécurité.

Si vous programmez en C++, vous pouvez manipuler le descripteur de sécurité binaire à l’aide du [langage SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)et des méthodes de conversion [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

n’oubliez pas que, à partir de Windows Vista, le contrôle de compte d’utilisateur (UAC, [User Account control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) ) affecte l’accès aux données wmi et ce qui peut être configuré avec le [*contrôle wmi*](gloss-w.md). Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
