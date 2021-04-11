---
description: Modifie les autorisations de sécurité pour le fichier de données logiques spécifié dans le chemin d’accès de l’objet.
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111006"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a>Méthode ChangeSecurityPermissions de la \_ classe de fichier de fichier CIM

La méthode **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier de données logiques spécifié dans le chemin d’accès de l’objet. Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire. Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Spécifie les informations de sécurité.

> [!Note]  
> Une liste de contrôle d’accès (ACL) **null** dans la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité. Pour plus d’informations sur les implications d’un accès illimité, consultez [création d’un descripteur de sécurité pour un nouvel objet](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

*Option* \[ dans\]
</dt> <dd>

Privilège de sécurité à modifier. Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez :

`Option = 1 + 4`

ou

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

Modifiez la liste de contrôle d’accès du fichier logique.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)


</dt> <dd>

Modifiez la liste de contrôle d’accès système du fichier logique.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Réussite.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

Accès refusé.

</dd> <dt>

**Échec non spécifié**
</dt> <dd>

8

Échec non spécifié.

</dd> <dt>

**Objet non valide**
</dt> <dd>

9

Objet non valide.

</dd> <dt>

**L’objet existe déjà**
</dt> <dd>

10

L’objet existe déjà.

</dd> <dt>

**Système de fichiers non NTFS**
</dt> <dd>

11

</dd> <dt>

**Plateforme non NT/Windows 2000**
</dt> <dd>

12

Plateforme non basée sur Windows NT.

</dd> <dt>

**Le lecteur n’est pas le même**
</dt> <dd>

13

Le lecteur n’est pas le même.

</dd> <dt>

**Répertoire non vide**
</dt> <dd>

14

le répertoire n'est pas vide.

</dd> <dt>

**Violation de partage**
</dt> <dd>

15

Violation de partage.

</dd> <dt>

**Fichier de démarrage non valide**
</dt> <dd>

16

Fichier de démarrage non valide.

</dd> <dt>

**Privilège non détenu**
</dt> <dd>

17

Privilège non détenu.

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

21

Paramètre non valide.

</dd> </dl>

## <a name="remarks"></a>Notes

La méthode **ChangeSecurityPermissions** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

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

[**\_Fichier de fichier CIM**](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[**\_Fichier de fichier CIM**](cim-datafile.md)
</dt> <dt>

[Tâches WMI : fichiers et dossiers](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

