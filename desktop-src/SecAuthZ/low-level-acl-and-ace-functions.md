---
description: Créez une liste de contrôle d’accès (ACL) à l’aide des fonctions de bas niveau, allouez une mémoire tampon pour la liste de contrôle d’accès, puis initialisez-la en appelant la fonction InitializeAcl.
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: Fonctions ACL et ACE de bas niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac63c17d84996afe9bdc43d0ccdd021db69ab488
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009105"
---
# <a name="low-level-acl-and-ace-functions"></a>Fonctions ACL et ACE de bas niveau

Pour créer une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) à l’aide des fonctions de bas niveau, allouez une mémoire tampon pour la liste de contrôle d’accès, puis initialisez-la en appelant la fonction [**InitializeAcl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) . Pour ajouter des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) à la fin d’une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL), utilisez les fonctions [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) et [**AddAccessDeniedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) . La fonction [**AddAuditAccessAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace) ajoute un ACE à la fin d’une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). Vous pouvez utiliser la fonction [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) pour ajouter une ou plusieurs entrées de contrôle d’accès à une position spécifiée dans une liste de contrôle d’accès. La fonction **AddAce** vous permet également d’ajouter une ACE héritable à une liste de contrôle d’accès. La fonction [**DeleteAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace) supprime une entrée du contrôle d’accès à partir d’une position spécifiée dans une liste de contrôle d’accès. La fonction [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) récupère une entrée du contrôle d’accès à partir d’une position spécifiée dans une liste de contrôle d’accès. La fonction [**FindFirstFreeAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace) récupère un pointeur vers le premier octet libre dans une liste de contrôle d’accès.

Pour modifier une liste de contrôle d’accès existante dans le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet, utilisez la fonction [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) ou [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) pour récupérer la liste de contrôle d’accès existante. Vous pouvez utiliser la fonction [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) pour copier des entrées de contrôle d’accès de l’ACL existante. Après avoir alloué et initialisé une nouvelle liste de contrôle d’accès, utilisez des fonctions telles que [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) et [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) pour y ajouter des ACE. Lorsque vous avez terminé la création de la nouvelle liste de contrôle d’accès, utilisez la fonction [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) ou [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) pour ajouter la nouvelle liste de contrôle d’accès au descripteur de sécurité de l’objet.

Vous pouvez utiliser les fonctions [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace), [**AddAccessDeniedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)ou [**AddAuditAccessObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) pour ajouter des [ACE spécifiques](object-specific-aces.md) à l’objet à la fin d’une liste de contrôle d’accès.

 

 
