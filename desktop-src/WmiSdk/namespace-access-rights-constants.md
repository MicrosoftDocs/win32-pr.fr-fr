---
description: 'WMI a des constantes de sécurité utilisées pour la vérification de l’accès aux espaces de noms par \_ \_ SystemSecurity :: GetCallerAccessRights.'
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Constantes de droits d’accès à l’espace de noms (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033838"
---
# <a name="namespace-access-rights-constants"></a>Constantes de droits d’accès à l’espace de noms

WMI a des constantes de sécurité utilisées pour la vérification de l’accès aux espaces de noms par [**\_ \_ SystemSecurity :: GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md). Pour obtenir des informations de sécurité sur les listes de contrôle d’accès (ACL, DACL ou SACL), consultez [listes de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [**droits d’accès standard**](/windows/desktop/SecAuthZ/standard-access-rights). Ces constantes sont définies dans l’énumération des **\_ \_ indicateurs de sécurité WBEM** .

<dl> <dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**\_activation WBEM**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Active le compte et accorde des autorisations de lecture à l’utilisateur. Il s’agit d’un droit d’accès par défaut pour tous les utilisateurs et correspond à l’autorisation activer le compte sous l’onglet sécurité du [*contrôle WMI*](gloss-w.md). Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**exécution de la \_ méthode WBEM \_**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Autorise l’exécution des méthodes. Les fournisseurs peuvent effectuer des vérifications d’accès supplémentaires. Il s’agit d’un droit d’accès par défaut pour tous les utilisateurs et correspond à l’autorisation exécuter les méthodes sur l’onglet sécurité du contrôle WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**\_REP en \_ écriture \_ complète WBEM**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Permet à un compte d’utilisateur d’écrire dans des classes du référentiel WMI, ainsi que des instances. Un utilisateur ne peut pas écrire dans les classes système. Seuls les membres du groupe administrateurs ont cette autorisation. **WBEM \_ Le \_ \_ REP en écriture complète** correspond à l’autorisation en écriture complète sur l’onglet sécurité du contrôle WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_REP- \_ écriture \_ partielle WBEM**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Vous permet d’écrire des données uniquement dans des instances, et non dans des classes. Un utilisateur ne peut pas écrire des classes dans l' [*espace de stockage WMI*](gloss-w.md). Seuls les membres du groupe administrateurs disposent de ce droit. **WBEM \_ Le \_ \_ REP en écriture partielle** correspond à l’autorisation écriture partielle sur l’onglet sécurité du contrôle WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_fournisseur d’écriture WBEM \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Permet d’écrire des classes et des instances pour les fournisseurs. Notez que les fournisseurs peuvent effectuer des vérifications d’accès supplémentaires lorsqu’ils empruntent l’identité d’un utilisateur. Il s’agit d’un droit d’accès par défaut pour tous les utilisateurs et correspond à l’autorisation d’écriture du fournisseur sur l’onglet sécurité du contrôle WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_accès à distance WBEM \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Permet à un compte d’utilisateur d’effectuer à distance les opérations autorisées par les autorisations décrites ci-dessus. Seuls les membres du groupe administrateurs disposent de ce droit. **WBEM \_ L' \_ accès à distance** correspond à l’autorisation activation à distance sur l’onglet sécurité du contrôle WMI.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[Sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

