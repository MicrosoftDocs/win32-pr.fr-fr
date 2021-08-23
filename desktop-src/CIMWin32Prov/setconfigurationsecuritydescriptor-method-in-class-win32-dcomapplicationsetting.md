---
description: Met à jour le descripteur de sécurité de configuration de l’application DCOM avec un nouveau descripteur de sécurité défini par une instance d’une \_ classe Win32 SecurityDescriptor.
ms.assetid: e0fe3d2f-7641-4cae-972d-888e800548de
ms.tgt_platform: multiple
title: Méthode SetConfigurationSecurityDescriptor de la classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aef263d3d0dc1f16c908d3f586b78d7ca4cfb0679a86fba2c9896404d81b03cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760159"
---
# <a name="setconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Méthode SetConfigurationSecurityDescriptor de la \_ classe Win32 DCOMApplicationSetting

La méthode **SetConfigurationSecurityDescriptor** met à jour le descripteur de sécurité de configuration de l’application DCOM avec un nouveau descripteur de sécurité qui est défini par une instance d’une classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Ce descripteur de sécurité détermine qui est autorisé à configurer l’application. Le compte qui exécute le script ou l’application qui appelle cette méthode doit avoir les privilèges **SeSecurityPrivilege** et **SeRestorePrivilege** . Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetConfigurationSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Descripteur* \[ dans\]
</dt> <dd>

Descripteur de sécurité à définir pour l’application DCOM.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur. Pour plus d’informations, consultez [codes de retour WMI](/windows/desktop/WmiSdk/wmi-return-codes) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Success**
</dt> <dd>

0

Opération réussie

</dd> <dt>

**2**
</dt> <dd>

L’utilisateur n’a pas accès aux informations demandées

</dd> <dt>

**8**
</dt> <dd>

Échec inconnu

</dd> <dt>

**9**
</dt> <dd>

L’utilisateur ne dispose pas des privilèges suffisants pour exécuter la méthode

</dd> <dt>

**21**
</dt> <dd>

Un paramètre spécifié dans l’appel de méthode n’est pas valide

</dd> <dt>

**Autres**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Remarques

L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).

Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné. Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).

Vous pouvez mettre à jour la liste DACL et la liste SACL dans l’instance [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) lors de l’appel de cette méthode, mais vous pouvez également mettre à jour uniquement la liste DACL ou uniquement la liste SACL.

Les valeurs suivantes dans le [**\_ \_ contrôle descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) déterminent si la liste DACL, la liste SACL ou les deux sont mises à jour.

-   **SE \_ liste DACL \_ présente**

    Indique que la liste DACL doit être mise à jour. Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste DACL.

-   **SE \_ liste SACL \_ présente**

    Indique que la liste SACL doit être mise à jour. Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste SACL. Pour mettre à jour la liste SACL, le privilège **SeSecurityPrivilege** doit être activé sur le compte. Pour les scripts, le nom du privilège est **SeSecurityPrivilege**. Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants).

Si les propriétés tiers de confiance du groupe et tiers de confiance du propriétaire ne sont pas **null**, elles sont mises à jour. Dans le cas contraire, WMI conserve les valeurs d’origine. Pour plus d’informations, consultez [objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).

Quand une nouvelle SACL est **null** dans un appel à cette méthode, alors le descripteur de sécurité SACL de l’objet sécurisable cible reste inchangé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**Constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modification de la sécurité d’accès sur les objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

