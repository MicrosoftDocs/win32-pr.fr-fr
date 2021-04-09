---
description: Utilisez les fonctions GetSecurityInfo et GetNamedSecurityInfo pour récupérer un pointeur vers un descripteur de sécurité d’objets.
ms.assetid: 834f1b58-d403-4899-865e-5721a37587e9
title: Opérations de descripteur de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5574a504468a4f4bb7dc14effe1f4717d695846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113790"
---
# <a name="security-descriptor-operations"></a>Opérations de descripteur de sécurité

L’API Windows fournit des fonctions permettant d’obtenir et de définir les composants du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) associé à un objet sécurisable. Utilisez les fonctions [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) et [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) pour récupérer un pointeur vers le descripteur de sécurité d’un objet. Ces fonctions peuvent également récupérer des pointeurs vers les composants individuels du descripteur de sécurité : DACL, SACL, SID propriétaire et SID de groupe principal. Utilisez les fonctions [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) et [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) pour définir les composants du descripteur de sécurité d’un objet.

En général, vous devez utiliser [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) et [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) avec des objets identifiés par un handle, et [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) et [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) avec des objets identifiés par un nom. Pour plus d’informations sur les fonctions spécifiques à utiliser lors de l’utilisation des différents types d’objets, consultez [objets sécurisables](securable-objects.md).

L’API Windows fournit des fonctions supplémentaires pour manipuler les composants d’un descripteur de sécurité. Pour plus d’informations sur l’utilisation des listes de contrôle d’accès (DACL ou SACL), consultez [obtention d’informations à partir d’une liste ACL](getting-information-from-an-acl.md) et [création ou modification d’une liste](creating-or-modifying-an-acl.md)de contrôle d’accès. Pour plus d’informations sur les SID, consultez [identificateurs de sécurité](security-identifiers.md) (SID).

Pour obtenir les informations de contrôle dans un descripteur de sécurité, appelez la fonction [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) . Pour définir les bits de contrôle liés à l’héritage automatique des entrées du contrôle d’accès, appelez la fonction [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) . Les autres bits de contrôle sont définis par les différentes fonctions qui définissent un composant descripteur de sécurité. Par exemple, si vous utilisez [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) pour modifier la liste DACL d’un objet, la fonction définit ou efface les bits comme il convient pour indiquer si le descripteur de sécurité a une liste DACL, s’il s’agit d’une DACL par défaut, et ainsi de suite. Un autre exemple concerne les bits de contrôle du [*Gestionnaire de ressources*](/windows/desktop/SecGloss/r-gly) (RM) contenus dans le descripteur de sécurité. Ces bits sont utilisés en fonction de l’implémentation du gestionnaire de ressources et sont accessibles via les fonctions [**GetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol) et [**SetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol) .

 

 
