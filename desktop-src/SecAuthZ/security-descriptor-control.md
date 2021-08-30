---
description: Jeu d’indicateurs binaires qui qualifient la signification d’un descripteur de sécurité ou de ses composants.
ms.assetid: 9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2
title: SECURITY_DESCRIPTOR_CONTROL (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da495f90337cd84b57c991c4c195d4d4ff971b8d15f012f724eeb1662e74a71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907399"
---
# <a name="security_descriptor_control"></a>\_contrôle de descripteur de sécurité \_

Le type de données de **\_ \_ contrôle du descripteur de sécurité** est un ensemble d’indicateurs binaires qui qualifient la signification d’un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) ou de ses composants. Chaque descripteur de sécurité a un membre de **contrôle** qui stocke les bits de **\_ \_ contrôle du descripteur de sécurité** .


```C++
typedef WORD SECURITY_DESCRIPTOR_CONTROL, *PSECURITY_DESCRIPTOR_CONTROL;
```



## <a name="remarks"></a>Remarques

Pour obtenir les bits de contrôle d’un descripteur de sécurité, appelez la fonction [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) . Pour définir les bits de contrôle d’un descripteur de sécurité, utilisez les fonctions pour modifier les descripteurs de sécurité. Pour obtenir la liste de ces fonctions, consultez la section Voir aussi.

Les applications peuvent utiliser la fonction [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) pour définir les bits de contrôle liés à l’héritage automatique des ACE.

La valeur de contrôle récupérée par la fonction [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) peut inclure une combinaison des indicateurs de bits de **\_ \_ contrôle de descripteur de sécurité** suivants.



| Valeur                                                     | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SE \_ \_demande d' \_ héritage \_ automatique de DACL<br/> 0x0100<br/> | Indique un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) requis dans lequel la liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) est configurée pour prendre en charge la propagation automatique des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) héritées aux objets enfants existants.<br/> Pour les [*listes de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) qui prennent en charge l’héritage automatique, ce bit est toujours défini. Les serveurs protégés peuvent appeler la fonction [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) pour convertir un descripteur de sécurité et définir cet indicateur. <br/> |
| SE \_ DACL \_ auto \_ hérité<br/> 0x0400<br/>    | Indique un descripteur de sécurité dans lequel la liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) est configurée pour prendre en charge la propagation automatique des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) pouvant être héritées aux objets enfants existants.<br/> Pour les [*listes de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) qui prennent en charge l’héritage automatique, ce bit est toujours défini. Les serveurs protégés peuvent appeler la fonction [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) pour convertir un descripteur de sécurité et définir cet indicateur. <br/>                                                                                                  |
| SE \_ DACL \_ par défaut<br/> 0x0008<br/>          | Indique un descripteur de sécurité avec une liste DACL par défaut. Par exemple, si le créateur d’un objet ne spécifie pas de liste DACL, l’objet reçoit la DACL par défaut à partir du [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) du créateur. Cet indicateur peut affecter la façon dont le système traite la liste DACL en ce qui concerne l’héritage de l’entrée du contrôle d’accès. le système ignore cet indicateur si l’indicateur de SE \_ DACL \_ présent n’est pas défini.<br/> Cet indicateur est utilisé pour déterminer comment la liste DACL finale sur l’objet doit être calculée et qu’elle n’est pas stockée physiquement dans le contrôle de descripteur de sécurité de l’objet sécurisable.<br/> Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                      |
| SE \_ liste DACL \_ présente<br/> 0x0004<br/>            | Indique un descripteur de sécurité qui a une liste DACL. Si cet indicateur n’est pas défini, ou si cet indicateur est défini et que la liste DACL est **null**, le descripteur de sécurité autorise un accès complet à tout le monde.<br/> Cet indicateur est utilisé pour stocker les informations de sécurité spécifiées par un appelant jusqu’à ce que le descripteur de sécurité soit associé à un objet sécurisable. une fois le descripteur de sécurité associé à un objet sécurisable, l' \_ indicateur SE DACL \_ présent est toujours défini dans le contrôle descripteur de sécurité.<br/> Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                                                                                                                                                   |
| SE \_ DACL \_ protégé<br/> 0x1000<br/>          | Empêche la modification de la liste DACL du descripteur de sécurité par les ACE pouvant être héritées. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SE \_ GROUPE \_ par défaut<br/> 0x0002<br/>         | Indique que l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du groupe de descripteurs de sécurité a été fourni par un mécanisme par défaut. Cet indicateur peut être utilisé par un gestionnaire de ressources pour identifier les objets dont le groupe de descripteurs de sécurité a été défini par un mécanisme par défaut. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SE \_ PROPRIÉTAIRE \_ par défaut<br/> 0x0001<br/>         | Indique que le SID du propriétaire du descripteur de sécurité a été fourni par un mécanisme par défaut. Cet indicateur peut être utilisé par un gestionnaire de ressources pour identifier les objets dont le propriétaire a été défini par un mécanisme par défaut. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SE \_ \_contrôle RM \_ valide<br/> 0x4000<br/>       | Indique que le contrôle Resource Manager est valide.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| SE \_ \_demande d' \_ héritage \_ automatique SACL<br/> 0x0200<br/> | Indique un descripteur de sécurité requis dans lequel la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) est configurée pour prendre en charge la propagation automatique des ACE pouvant être héritées aux objets enfants existants.<br/> Le système définit ce bit lorsqu’il exécute l’algorithme d’héritage automatique pour l’objet et ses objets enfants existants. Pour convertir un descripteur de sécurité et définir cet indicateur, les serveurs protégés peuvent appeler la fonction [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) .<br/>                                                                                                                                                                                                                                                                                   |
| SE \_ \_ACL automatiquement \_ hérité<br/> 0x0800<br/>    | Indique un descripteur de sécurité dans lequel la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) est configurée pour prendre en charge la propagation automatique des ACE pouvant être héritées aux objets enfants existants.<br/> Le système définit ce bit lorsqu’il exécute l’algorithme d’héritage automatique pour l’objet et ses objets enfants existants. Pour convertir un descripteur de sécurité et définir cet indicateur, les serveurs protégés peuvent appeler la fonction [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) . <br/>                                                                                                                                                                                                                                                                                           |
| SE \_ SACL \_ par défaut<br/> 0x0008<br/>          | Un mécanisme par défaut, plutôt que le [*fournisseur*](/windows/desktop/SecGloss/p-gly) d’origine du descripteur de sécurité, fournissait la liste SACL. Cet indicateur peut affecter la façon dont le système traite la liste SACL, en ce qui concerne l’héritage de l’entrée du contrôle d’accès. le système ignore cet indicateur si le SE \_ \_ indicateur de présence SACL n’est pas défini. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SE \_ liste SACL \_ présente<br/> 0x0010<br/>            | Indique un descripteur de sécurité qui a une liste SACL. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SE \_ liste SACL \_ protégée<br/> 0x2000<br/>          | Empêche la modification de la liste SACL du descripteur de sécurité par les ACE pouvant être héritées. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SE \_ Auto \_ relatif<br/> 0x8000<br/>           | Indique un [*descripteur de sécurité auto-relatif*](/windows/desktop/SecGloss/s-gly). Si cet indicateur n’est pas défini, le descripteur de sécurité est au format absolu. Pour plus d’informations, consultez [descripteurs de sécurité absolus et Self-Relative](absolute-and-self-relative-security-descriptors.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>winnt. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Access Control de bas niveau](low-level-access-control.md)
</dt> <dt>

[Structures de Access Control de base](authorization-structures.md)
</dt> <dt>

[**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity)
</dt> <dt>

[**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol)
</dt> <dt>

[**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)
</dt> <dt>

[**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)
</dt> <dt>

[**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)
</dt> <dt>

[**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)
</dt> <dt>

[**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)
</dt> <dt>

[**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)
</dt> <dt>

[**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)
</dt> <dt>

[**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)
</dt> <dt>

[**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)
</dt> </dl>

 

