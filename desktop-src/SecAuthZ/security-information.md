---
description: Identifie les informations de sécurité relatives aux objets qui sont définies ou interrogées.
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: SECURITY_INFORMATION (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaad4b9f61a20b26397081433b88782dcbc33f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201658"
---
# <a name="security_information"></a>informations de sécurité \_

Le type de données **\_ informations de sécurité** identifie les informations de sécurité relatives aux objets qui sont définies ou interrogées. Ces informations de sécurité incluent :

-   Propriétaire d’un objet
-   Groupe principal d’un objet
-   [*Liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) d’un objet
-   [*Liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) d’un objet


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>Notes

Certains membres d' **\_ informations de sécurité** ne fonctionnent qu’avec la fonction [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) . Ces membres ne sont pas retournés dans la structure retournée par d’autres fonctions de sécurité telles que [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Chaque élément d’informations de sécurité est désigné par un indicateur de bit. Chaque indicateur de bit peut être l’une des valeurs suivantes. Pour plus d’informations, consultez les fonctions [**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) et [**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask) .



| Valeur/droits requis pour interroger/définir                                                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_informations sur la sécurité des attributs \_<br/> Droit requis pour la requête : **lire \_ le contrôle**<br/> Droit requis pour définir : **écriture \_ DAC**<br/>                                                                                     | Propriétés de ressource de l’objet référencé. Les propriétés de ressource sont stockées dans les types d’entrées du contrôle d’accès de \_ ressource système \_ \_ dans la liste SACL du descripteur de sécurité.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Cet indicateur de bit n’est pas disponible.<br/> <br/>                 |
| SAUVEGARDER \_ les \_ informations de sécurité<br/> Droit requis pour la requête : **lire \_ le contrôle** et accéder à la **\_ \_ sécurité du système**<br/> Il est nécessaire de définir : **écrire \_ DAC** et **écrire le \_ propriétaire** et la **\_ \_ sécurité du système d’accès**<br/> | Toutes les parties du descripteur de sécurité. Cela est utile pour les logiciels de sauvegarde et de restauration qui doivent conserver l’ensemble du descripteur de sécurité.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Cet indicateur de bit n’est pas disponible.<br/> <br/>                                                  |
| \_informations de sécurité DACL \_<br/> Droit requis pour la requête : **lire \_ le contrôle**<br/> Droit requis pour définir : **écriture \_ DAC**<br/>                                                                                          | La liste DACL de l’objet est référencée.<br/>                                                                                                                                                                                                                                                                                                                        |
| GROUPEr les \_ informations de sécurité \_<br/> Droit requis pour la requête : **lire \_ le contrôle**<br/> Droit requis pour définir : **écrire le \_ propriétaire** <br/>                                                                                      | L’identificateur de groupe principal de l’objet est référencé.<br/>                                                                                                                                                                                                                                                                                                    |
| ÉTIQUETer les \_ informations de sécurité \_<br/> Droit requis pour la requête : **lire \_ le contrôle**<br/> Droit requis pour définir : **écrire le \_ propriétaire** <br/>                                                                                      | L’étiquette d’intégrité obligatoire est référencée.<br/> L’étiquette d’intégrité obligatoire est une entrée du contrôle d’accès dans la liste SACL de l’objet.<br/> **Windows Server 2003 et Windows XP :** Cet indicateur de bit n’est pas disponible.<br/> <br/>                                                                                                                                    |
| \_informations de sécurité du propriétaire \_<br/> Droit requis pour la requête : **lire \_ le contrôle**<br/> Droit requis pour définir : **écrire le \_ propriétaire** <br/>                                                                                      | L’identificateur de propriétaire de l’objet est référencé.<br/>                                                                                                                                                                                                                                                                                                            |
| \_informations de \_ sécurité \_ DACL protégées<br/> Droit requis pour la requête : non disponible<br/> Droit requis pour définir : **écriture \_ DAC**<br/>                                                                                   | La liste DACL ne peut pas hériter d' [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE).<br/>                                                                                                                                                                                                                   |
| \_informations de \_ sécurité \_ SACL protégées<br/> Droit requis pour la requête : non disponible<br/> Droit requis pour définir : **accéder à la \_ \_ sécurité du système**<br/>                                                                     | La liste SACL ne peut pas hériter des ACE.<br/>                                                                                                                                                                                                                                                                                                                                      |
| \_informations de sécurité SACL \_<br/> Droit requis pour interroger : accéder à la **\_ \_ sécurité du système**<br/> Droit requis pour définir : **accéder à la \_ \_ sécurité du système**<br/>                                                                 | La liste SACL de l’objet est référencée.<br/>                                                                                                                                                                                                                                                                                                                        |
| \_informations sur la sécurité de l’étendue \_<br/> Droit requis pour la requête : **lire \_ le contrôle**<br/> Droit requis pour définir : **accéder à la \_ \_ sécurité du système**<br/>                                                                           | Identificateur de la stratégie d’accès centralisée (CAP) applicable à l’objet référencé. Chaque identificateur de CAP est stocké dans un \_ type d' \_ \_ ACE d’ID de stratégie système \_ dans la liste SACL du SD.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Cet indicateur de bit n’est pas disponible.<br/> <br/> |
| \_informations de sécurité DACL \_ non \_ protégées<br/> Droit requis pour la requête : non disponible<br/> Droit requis pour définir : **écriture \_ DAC**<br/>                                                                                 | La liste DACL hérite des ACE de l’objet parent.<br/>                                                                                                                                                                                                                                                                                                                     |
| \_informations de sécurité SACL \_ non \_ protégées<br/> Droit requis pour la requête : non disponible<br/> Droit requis pour définir : **accéder à la \_ \_ sécurité du système**<br/>                                                                   | La liste SACL hérite des ACE de l’objet parent.<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Winnt. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle d’accès](access-control.md)
</dt> <dt>

[Structures de Access Control de base](authorization-structures.md)
</dt> <dt>

[**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
</dt> <dt>

[**Convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)
</dt> <dt>

[**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)
</dt> <dt>

[**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)
</dt> <dt>

[**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)
</dt> <dt>

[**GetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity)
</dt> <dt>

[**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya)
</dt> <dt>

[**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)
</dt> <dt>

[**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)
</dt> <dt>

[**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)
</dt> <dt>

[**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[**SetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity)
</dt> <dt>

[**TreeResetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treeresetnamedsecurityinfoa)
</dt> <dt>

[**TreeSetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treesetnamedsecurityinfoa)
</dt> </dl>

 

