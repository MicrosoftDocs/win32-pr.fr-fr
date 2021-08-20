---
description: Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode ChangeSecurityPermissions).
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissionsEx de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b550ca2c3297d4f2185918036bc283138e619dda2e1facff696ec8fe868e07b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081023"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a>Méthode ChangeSecurityPermissionsEx de la \_ classe CIM LogicalFile

La méthode **ChangeSecurityPermissionsEX** modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) ). Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Spécifie les informations de sécurité.

</dd> <dt>

*Option* \[ dans\]
</dt> <dd>

Privilège de sécurité à modifier. Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez

`Option = 1 + 4`

ou

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)


</dt> <dd>

Modifiez le propriétaire du fichier logique.

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)


</dt> <dd>

Modifiez le groupe du fichier logique.

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)


</dt> <dd>

Modifiez la liste de contrôle d’accès du fichier logique.

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)


</dt> <dd>

Modifiez la liste de contrôle d’accès système du fichier logique.

</dd> </dl> </dd> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué. Ce paramètre a une valeur **null** si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode. En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent. Si la valeur du paramètre est **null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Récursif* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, les autorisations de sécurité sont appliquées de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) . Pour les instances de fichier, ce paramètre est ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.

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

Le système de fichiers n’est pas NTFS.

</dd> <dt>

**plateforme non NT/Windows 2000**
</dt> <dd>

12

Plateforme non Windows.

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

## <a name="remarks"></a>Remarques

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

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

[**\_LOGICALFILE CIM**](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

