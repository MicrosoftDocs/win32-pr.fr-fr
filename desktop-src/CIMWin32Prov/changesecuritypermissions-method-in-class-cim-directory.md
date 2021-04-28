---
description: 'Méthode ChangeSecurityPermissions de la classe CIM_Directory : modifie les autorisations de sécurité pour le fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet.'
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 389ed5b7b0a43981c5eeb3d66a73bd19cbd99d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091067"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a>Méthode ChangeSecurityPermissions de la \_ classe de répertoire CIM

La méthode **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet. Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire. Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

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

Spécifie des informations de sécurité.

> [!Note]  
> Une liste de contrôle d’accès (ACL) **null** dans la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité.

 

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

## <a name="return-value"></a>Valeur renvoyée

Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.

<dl> <dt>


</dt> <dd>

0

Réussite.

</dd> <dt>


</dt> <dd>

2

Accès refusé.

</dd> <dt>


</dt> <dd>

8

Échec non spécifié.

</dd> <dt>


</dt> <dd>

9

Objet non valide.

</dd> <dt>


</dt> <dd>

10

L’objet existe déjà.

</dd> <dt>


</dt> <dd>

11

Le système de fichiers n’est pas NTFS.

</dd> <dt>


</dt> <dd>

12

Plateforme non Windows.

</dd> <dt>


</dt> <dd>

13

Le lecteur n’est pas le même.

</dd> <dt>


</dt> <dd>

14

le répertoire n'est pas vide.

</dd> <dt>


</dt> <dd>

15

Violation de partage.

</dd> <dt>


</dt> <dd>

16

Fichier de démarrage non valide.

</dd> <dt>


</dt> <dd>

17

Privilège non détenu.

</dd> <dt>


</dt> <dd>

21

Paramètre non valide.

</dd> </dl>

## <a name="remarks"></a>Notes 

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

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

[\_Répertoire CIM](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[**\_Répertoire CIM**](cim-directory.md)
</dt> </dl>

 

