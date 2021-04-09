---
description: Renomme un nom de compte d’utilisateur.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Renommer la méthode de la classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111247"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a>Renommer la méthode de la \_ classe UserAccount Win32

La méthode de la classe **Renommer** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomme le nom d’un compte d’utilisateur.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Nouveau nom du compte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Réussite.

</dd> <dt>

**Instance introuvable**
</dt> <dd>

1

Instance introuvable.

</dd> <dt>

**Instance obligatoire**
</dt> <dd>

2

Instance obligatoire.

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

3

Paramètre non valide.

</dd> <dt>

**Utilisateur non trouvé.**
</dt> <dd>

4

Utilisateur introuvable.

</dd> <dt>

**Domaine introuvable**
</dt> <dd>

5

Domaine introuvable.

</dd> <dt>

**L’opération est autorisée uniquement sur le contrôleur de domaine principal du domaine**
</dt> <dd>

6

L’opération est autorisée uniquement sur le contrôleur de domaine principal du domaine.

</dd> <dt>

**L’opération n’est pas autorisée sur le dernier compte d’administration.**
</dt> <dd>

7

</dd> <dt>

**L’opération n’est pas autorisée sur les groupes spéciaux spécifiés ; utilisateur, administrateur, local ou invité.**
</dt> <dd>

8

L’opération n’est pas autorisée sur les groupes spéciaux spécifiés : utilisateur, administrateur, local ou invité.

</dd> <dt>

**Autre erreur d’API**
</dt> <dd>

9

Autre erreur d’API.

</dd> <dt>

**Erreur interne**
</dt> <dd>

10

Erreur interne.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette fonctionnalité est implémentée en tant que méthode pour fournir un contexte distinct pour le nouveau nom qui peut être distingué de la valeur de propriété de clé pour le nom associé à l’instance à modifier.

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

[**\_UserAccount Win32**](win32-useraccount.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

