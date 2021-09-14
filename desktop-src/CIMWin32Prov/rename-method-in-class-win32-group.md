---
description: Autorise la modification du nom du groupe.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Renommer la méthode de la classe Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006945"
---
# <a name="rename-method-of-the-win32_group-class"></a>Renommer la méthode de la \_ classe de groupe Win32

La méthode de la classe **Renommer** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) permet de modifier le nom du groupe.

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

nom du compte d’utilisateur Windows sur le domaine spécifié par la propriété de **domaine** de cette classe.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode **Rename** peut retourner les codes d’erreur répertoriés dans la liste suivante. Pour les valeurs entières autres que celles listées, reportez-vous à [ \_ codes de retour WMI](/windows/desktop/WmiSdk/wmi-return-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Réussite.

</dd> <dt>

**Instance introuvable**
</dt> <dd>

1

</dd> <dt>

**Instance obligatoire**
</dt> <dd>

2

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

3

</dd> <dt>

**Groupe introuvable**
</dt> <dd>

4

</dd> <dt>

**Domaine introuvable**
</dt> <dd>

5

</dd> <dt>

**L’opération est autorisée uniquement sur le contrôleur de domaine principal du domaine**
</dt> <dd>

6

</dd> <dt>

**L’opération n’est pas autorisée sur les groupes spéciaux spécifiés ; utilisateur, administrateur, local ou invité.**
</dt> <dd>

7

</dd> <dt>

**Autre erreur d’API**
</dt> <dd>

8

</dd> <dt>

**Erreur interne**
</dt> <dd>

9

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Groupe Win32**](win32-group.md)
</dt> <dt>

[**\_LogicalFileSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

