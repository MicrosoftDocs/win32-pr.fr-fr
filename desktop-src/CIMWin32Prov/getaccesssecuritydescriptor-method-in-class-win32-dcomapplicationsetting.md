---
description: Obtient le descripteur de sécurité qui contrôle qui peut accéder à une application DCOM.
ms.assetid: 5ddd563b-f731-47ac-8a13-20940adfa86d
ms.tgt_platform: multiple
title: Méthode GetAccessSecurityDescriptor de la classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 326b68eebfdf5ffe785d0d94849c46d03fd3e40e3713e8ab0469d663d26b55da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077629"
---
# <a name="getaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Méthode GetAccessSecurityDescriptor de la \_ classe Win32 DCOMApplicationSetting

La méthode WMI **GetAccessSecurityDescriptor** obtient le descripteur de sécurité qui contrôle les utilisateurs autorisés à accéder à une application DCOM. Le descripteur de sécurité est une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Le compte qui exécute le script ou l’application qui appelle cette méthode doit avoir le privilège **SeSecurityPrivilege** et **SeRestorePrivilege** . Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetAccessSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Descripteur* \[ à\]
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

 

