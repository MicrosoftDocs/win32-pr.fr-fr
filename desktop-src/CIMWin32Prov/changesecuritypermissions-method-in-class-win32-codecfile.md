---
description: Modifie les autorisations de sécurité pour le fichier de codec logique spécifié dans le chemin d’accès de l’objet.
ms.assetid: d7945666-e514-4bfc-81bc-8e98aa90bcf0
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b0789164b2bb28b5c3c84e907cf7ae2acb96e01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517390"
---
# <a name="changesecuritypermissions-method-of-the-win32_codecfile-class"></a>Méthode ChangeSecurityPermissions de la \_ classe Win32 CodecFile

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier de codec logique spécifié dans le chemin d’accès de l’objet. Si le fichier logique est un répertoire, **ChangeSecurityPermissions** est récursif et modifie les autorisations de sécurité de tous les fichiers et sous-répertoires contenus dans le répertoire. **ChangeSecurityPermissions** retourne une valeur entière égale à 0 (zéro) si les autorisations sont modifiées, et un autre nombre pour indiquer une erreur.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SecurityDescriptor* \[ dans\]
</dt> <dd>

Expression qui correspond à une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Ce descripteur contient de nouvelles autorisations de sécurité pour l’instance de [**Win32 \_ CodecFile**](win32-codecfile.md).

</dd> <dt>

*Option* \[ dans\]
</dt> <dd>

Privilège de sécurité à modifier. Par exemple, pour modifier la sécurité du propriétaire et de la liste de contrôle d’accès discrétionnaire (DACL), utilisez :

`Option = 1 + 4`

-ou-

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1 (0x1))


</dt> <dd>

Modifiez le propriétaire du fichier logique.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ GROUPEr les \_ \_ informations de sécurité** (2 (0X2))


</dt> <dd>

Modifiez le groupe du fichier logique.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4 (0x4))


</dt> <dd>

Modifiez la liste de contrôle d’accès discrétionnaire (DACL) du fichier logique.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8 (0x8))


</dt> <dd>

Modifiez la liste de contrôle d’accès système (SACL) du fichier logique.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur 0 (zéro) si les autorisations sont modifiées et un nombre différent pour indiquer une erreur.

<dl> <dt>

**Success**
</dt> <dd>

0

La demande a réussi.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’accès est refusé.

</dd> <dt>

**Échec non spécifié**
</dt> <dd>

8

Une erreur non spécifiée s’est produite.

</dd> <dt>

**Objet non valide**
</dt> <dd>

9

Le nom spécifié n’est pas valide.

</dd> <dt>

**L’objet existe déjà**
</dt> <dd>

10

L'objet spécifié existe déjà.

</dd> <dt>

**Système de fichiers non NTFS**
</dt> <dd>

11

Le système de fichiers n’est pas un système de fichiers NTFS.

</dd> <dt>

**Plateforme non NT/Windows 2000**
</dt> <dd>

12

La plateforme n’est pas Windows.

</dd> <dt>

**Le lecteur n’est pas le même**
</dt> <dd>

13

Le lecteur n’est pas le même.

</dd> <dt>

**Répertoire non vide**
</dt> <dd>

14

Le répertoire n'est pas vide.

</dd> <dt>

**Violation de partage**
</dt> <dd>

15

Violation de partage.

</dd> <dt>

**Fichier de démarrage non valide**
</dt> <dd>

16

Le fichier de démarrage spécifié n’est pas valide.

</dd> <dt>

**Privilège non détenu**
</dt> <dd>

17

Un privilège requis pour l’opération n’est pas conservé.

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

21

Un paramètre spécifié n’est pas valide.

</dd> </dl>

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

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_CodecFile Win32**](win32-codecfile.md)
</dt> </dl>

 

