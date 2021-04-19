---
description: Jeu d’indicateurs binaires qui qualifient la signification d’un descripteur de sécurité ou de ses composants.
ms.assetid: 9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2
title: SECURITY_DESCRIPTOR_CONTROL (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3def788407093d0a487640d1ad0e445b61fe20e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514223"
---
# <a name="security_descriptor_control"></a>\_contrôle de descripteur de sécurité \_

Le type de données de **\_ \_ contrôle du descripteur de sécurité** est un ensemble d’indicateurs binaires qui qualifient la signification d’un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) ou de ses composants. Chaque descripteur de sécurité a un membre de **contrôle** qui stocke les bits de **\_ \_ contrôle du descripteur de sécurité** .


```C++
typedef WORD SECURITY_DESCRIPTOR_CONTROL, *PSECURITY_DESCRIPTOR_CONTROL;
```



## <a name="remarks"></a>Notes

Pour obtenir les bits de contrôle d’un descripteur de sécurité, appelez la fonction [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) . Pour définir les bits de contrôle d’un descripteur de sécurité, utilisez les fonctions pour modifier les descripteurs de sécurité. Pour obtenir la liste de ces fonctions, consultez la section Voir aussi.

Les applications peuvent utiliser la fonction [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) pour définir les bits de contrôle liés à l’héritage automatique des ACE.

La valeur de contrôle récupérée par la fonction [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) peut inclure une combinaison des indicateurs de bits de **\_ \_ contrôle de descripteur de sécurité** suivants.



| Valeur                                                     | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_demande d' \_ \_ héritage automatique \_ de la DACL se<br/> 0x0100<br/> | Indique un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) requis dans lequel la liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) est configurée pour prendre en charge la propagation automatique des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) héritées aux objets enfants existants.<br/> Pour les [*listes de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) qui prennent en charge l’héritage automatique, ce bit est toujours défini. Les serveurs protégés peuvent appeler la fonction [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) pour convertir un descripteur de sécurité et définir cet indicateur. <br/> |
| SE \_ DACL \_ auto \_ hérité<br/> 0x0400<br/>    | Indique un descripteur de sécurité dans lequel la liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) est configurée pour prendre en charge la propagation automatique des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) pouvant être héritées aux objets enfants existants.<br/> Pour les [*listes de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) qui prennent en charge l’héritage automatique, ce bit est toujours défini. Les serveurs protégés peuvent appeler la fonction [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) pour convertir un descripteur de sécurité et définir cet indicateur. <br/>                                                                                                  |
| \_liste DACL de se \_ par défaut<br/> 0x0008<br/>          | Indique un descripteur de sécurité avec une liste DACL par défaut. Par exemple, si le créateur d’un objet ne spécifie pas de liste DACL, l’objet reçoit la DACL par défaut à partir du [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) du créateur. Cet indicateur peut affecter la façon dont le système traite la liste DACL en ce qui concerne l’héritage de l’entrée du contrôle d’accès. Le système ignore cet indicateur si l' \_ indicateur de \_ présence DACL se présente n’est pas défini.<br/> Cet indicateur est utilisé pour déterminer comment la liste DACL finale sur l’objet doit être calculée et qu’elle n’est pas stockée physiquement dans le contrôle de descripteur de sécurité de l’objet sécurisable.<br/> Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                      |
| SE \_ DACL en \_ présence<br/> 0x0004<br/>            | Indique un descripteur de sécurité qui a une liste DACL. Si cet indicateur n’est pas défini, ou si cet indicateur est défini et que la liste DACL est **null**, le descripteur de sécurité autorise un accès complet à tout le monde.<br/> Cet indicateur est utilisé pour stocker les informations de sécurité spécifiées par un appelant jusqu’à ce que le descripteur de sécurité soit associé à un objet sécurisable. Une fois le descripteur de sécurité associé à un objet sécurisable, l' \_ \_ indicateur de présence DACL se est toujours défini dans le contrôle de descripteur de sécurité.<br/> Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                                                                                                                                                   |
| \_liste DACL de se \_ protégée<br/> 0x1000<br/>          | Empêche la modification de la liste DACL du descripteur de sécurité par les ACE pouvant être héritées. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Groupe de SE \_ \_ par défaut<br/> 0x0002<br/>         | Indique que l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du groupe de descripteurs de sécurité a été fourni par un mécanisme par défaut. Cet indicateur peut être utilisé par un gestionnaire de ressources pour identifier les objets dont le groupe de descripteurs de sécurité a été défini par un mécanisme par défaut. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| propriétaire de SE \_ \_ par défaut<br/> 0x0001<br/>         | Indique que le SID du propriétaire du descripteur de sécurité a été fourni par un mécanisme par défaut. Cet indicateur peut être utilisé par un gestionnaire de ressources pour identifier les objets dont le propriétaire a été défini par un mécanisme par défaut. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| \_contrôle RM de se \_ \_ valide<br/> 0x4000<br/>       | Indique que le contrôle Resource Manager est valide.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_demande d' \_ \_ héritage automatique SACL se \_<br/> 0x0200<br/> | Indique un descripteur de sécurité requis dans lequel la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) est configurée pour prendre en charge la propagation automatique des ACE pouvant être héritées aux objets enfants existants.<br/> Le système définit ce bit lorsqu’il exécute l’algorithme d’héritage automatique pour l’objet et ses objets enfants existants. Pour convertir un descripteur de sécurité et définir cet indicateur, les serveurs protégés peuvent appeler la fonction [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) .<br/>                                                                                                                                                                                                                                                                                   |
| \_SACL \_ auto \_ hérité<br/> 0x0800<br/>    | Indique un descripteur de sécurité dans lequel la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) est configurée pour prendre en charge la propagation automatique des ACE pouvant être héritées aux objets enfants existants.<br/> Le système définit ce bit lorsqu’il exécute l’algorithme d’héritage automatique pour l’objet et ses objets enfants existants. Pour convertir un descripteur de sécurité et définir cet indicateur, les serveurs protégés peuvent appeler la fonction [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) . <br/>                                                                                                                                                                                                                                                                                           |
| SACL de SE \_ \_ par défaut<br/> 0x0008<br/>          | Un mécanisme par défaut, plutôt que le [*fournisseur*](/windows/desktop/SecGloss/p-gly) d’origine du descripteur de sécurité, fournissait la liste SACL. Cet indicateur peut affecter la façon dont le système traite la liste SACL, en ce qui concerne l’héritage de l’entrée du contrôle d’accès. Le système ignore cet indicateur si l' \_ indicateur de \_ présence SACL se présente n’est pas défini. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_liste SACL se \_ présente<br/> 0x0010<br/>            | Indique un descripteur de sécurité qui a une liste SACL. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_protection SACL de se \_<br/> 0x2000<br/>          | Empêche la modification de la liste SACL du descripteur de sécurité par les ACE pouvant être héritées. Pour définir cet indicateur, utilisez la fonction [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| soi- \_ même \_ relatif<br/> 0x8000<br/>           | Indique un [*descripteur de sécurité auto-relatif*](/windows/desktop/SecGloss/s-gly). Si cet indicateur n’est pas défini, le descripteur de sécurité est au format absolu. Pour plus d’informations, consultez [descripteurs de sécurité absolus et Self-Relative](absolute-and-self-relative-security-descriptors.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Winnt. h (inclure Windows. h)</dt> </dl> |



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

 

