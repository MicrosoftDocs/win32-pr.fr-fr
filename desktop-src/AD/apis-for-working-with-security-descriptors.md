---
title: API pour l’utilisation des descripteurs de sécurité
description: API pour l’utilisation des descripteurs de sécurité
ms.assetid: eb5ee183-949c-41f5-9f74-f9c418fdf0a2
ms.tgt_platform: multiple
keywords:
- descripteurs de sécurité Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78988a2c435f397f0030ebaaef4e6d06385e710bc3671995338052c220f852
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024571"
---
# <a name="apis-for-working-with-security-descriptors"></a>API pour l’utilisation des descripteurs de sécurité

Chaque objet de Active Directory Domain Services a un attribut **ntSecurityDescriptor** qui contient le descripteur de sécurité de l’objet. Il existe deux façons principales de lire et manipuler un descripteur de sécurité d’un objet d’annuaire :

-   Utilisez la méthode [**IADs :: obtenir**](/windows/desktop/api/iads/nf-iads-iads-get) pour récupérer le descripteur de sécurité en tant qu’objet com ADSI avec une interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Les interfaces **IADsSecurityDescriptor**, [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)et [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) peuvent être utilisées pour gérer le descripteur de sécurité et ses composants (listes de contrôle d’accès, entrées de contrôle d’accès, etc.). Pour plus d’informations et pour obtenir un exemple de code, consultez [utilisation de IADs pour obtenir un descripteur de sécurité](using-iads-to-get-a-security-descriptor.md).
-   Utilisez la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) pour récupérer un descripteur de sécurité d’objet en tant que pointeur vers une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Utilisez ce pointeur avec une fonction de contrôle d’accès Win32, telle que [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) ou [**BuildSecurityDescriptor**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora). Pour plus d’informations et pour obtenir un exemple de code, consultez [utilisation de IDirectoryObject pour obtenir un descripteur de sécurité](using-idirectoryobject-to-get-a-security-descriptor.md).

La technique recommandée, et celle utilisée par la plupart des exemples de code de ce guide, consiste à utiliser les **\* *interfaces IADs _, car elles simplifient la gestion des descripteurs de sécurité, des listes de contrôle d’accès et des ACE. pour les programmeurs Visual Basic, les* interfaces \* _ IADs** sont le moyen le plus efficace pour gérer les descripteurs de sécurité.

La technique [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) est utile quand une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) est requise. Par exemple, l’exemple de code qui [vérifie un droit d’accès de contrôle dans la liste de contrôle d’accès d’un objet](checking-a-control-access-right-in-an-objectampaposs-acl.md) utilise cette méthode pour récupérer un descripteur de sécurité à passer à la fonction [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .

Pour plus d'informations, consultez les pages suivantes :

-   [Utilisation de IADs pour obtenir un descripteur de sécurité](using-iads-to-get-a-security-descriptor.md)
-   [Utilisation de IDirectoryObject pour obtenir un descripteur de sécurité](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [Composants du descripteur de sécurité](security-descriptor-components.md)
-   [Récupération de la liste DACL d’un objet](retrieving-an-objectampaposs-dacl.md)
-   [Récupération de la liste SACL d’un objet](retrieving-an-objectampaposs-sacl.md)
-   [Lecture du descripteur de sécurité d’un objet](reading-an-objectampaposs-security-descriptor.md)
-   [Exemple de code pour la création d’un descripteur de sécurité](example-code-for-creating-a-security-descriptor.md)
-   [Exemple de code pour l’énumération de la liste de contrôle d’accès d’un objet dans Active Directory Domain Services](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 