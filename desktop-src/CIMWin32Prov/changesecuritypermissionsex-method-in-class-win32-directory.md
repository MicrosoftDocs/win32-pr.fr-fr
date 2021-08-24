---
description: Modifie les autorisations de sécurité pour le fichier d’entrée de répertoire spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode ChangeSecurityPermissions).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissionsEx de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d90a6a76067421c3b23c0ec5124fa5da85e029e81d0307a2b4b66d01231fe56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323029"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a>Méthode ChangeSecurityPermissionsEx de la \_ classe Directory Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEX** modifie les autorisations de sécurité pour le fichier d’entrée de répertoire spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ). Si le fichier logique est un répertoire, cette méthode est récursive et modifie les autorisations de sécurité de tous les fichiers et sous-répertoires contenus dans le répertoire.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SecurityDescriptor* \[ dans\]
</dt> <dd>

Expression qui correspond à une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Ce paramètre contient de nouvelles autorisations de sécurité pour l’instance du [**\_ fichier d’échange Win32**](win32-pagefile.md).

</dd> <dt>

*Option* \[ dans\]
</dt> <dd>

Privilège de sécurité à modifier. Par exemple, pour modifier la sécurité du propriétaire et de la liste de contrôle d’accès discrétionnaire (DACL), utilisez la commande suivante :

`Option = 1 + 4`

-ou-

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)


</dt> <dd>

Modifiez le propriétaire du fichier logique.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)


</dt> <dd>

Modifiez le groupe du fichier logique.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)


</dt> <dd>

Modifiez la liste DACL du fichier logique.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)


</dt> <dd>

Modifiez la liste de contrôle d’accès système (SACL) du fichier logique.

</dd> </dl> </dd> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Nom du fichier ou du répertoire dans lequel la méthode **ChangeSecurityPermissionsEX** a échoué. Ce paramètre a la valeur null si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans, facultatif\]
</dt> <dd>

Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **ChangeSecurityPermissionsEX**. En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent. Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** . Ce paramètre est facultatif.

Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.

</dd> <dt>

*Récursif* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, la modification de la propriété est appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) . Pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré. Ce paramètre est facultatif.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la valeur 0 (zéro) si les autorisations sont modifiées et un autre nombre pour indiquer une erreur.

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

**plateforme non NT/Windows 2000**
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

[**\_Répertoire Win32**](win32-directory.md)
</dt> </dl>

 

