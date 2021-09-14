---
description: La méthode TakeOwnerShip obtient la propriété du fichier logique qui est spécifié dans le chemin d’accès de l’objet.
ms.assetid: 0835c335-0ada-44c1-9e71-44ba2041d8e2
ms.tgt_platform: multiple
title: Méthode TakeOwnerShip de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ade501db9b6af21b3761b70f638faa20d699401
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006858"
---
# <a name="takeownership-method-of-the-cim_datafile-class"></a>Méthode TakeOwnerShip de la \_ classe de fichier de fichier CIM

La méthode **TakeOwnership** obtient la propriété du fichier logique qui est spécifié dans le chemin d’accès de l’objet. Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire. Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Réussite.

</dd> <dt>

**2**
</dt> <dd>

Accès refusé.

</dd> <dt>

**8**
</dt> <dd>

Échec non spécifié.

</dd> <dt>

**9**
</dt> <dd>

Objet non valide.

</dd> <dt>

**10**
</dt> <dd>

L’objet existe déjà.

</dd> <dt>

**11**
</dt> <dd>

Le système de fichiers n’est pas NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plateforme non Windows.

</dd> <dt>

**13**
</dt> <dd>

Le lecteur n’est pas le même.

</dd> <dt>

**14**
</dt> <dd>

le répertoire n'est pas vide.

</dd> <dt>

**15**
</dt> <dd>

Violation de partage.

</dd> <dt>

**16**
</dt> <dd>

Fichier de démarrage non valide.

</dd> <dt>

**17**
</dt> <dd>

Privilège non détenu.

</dd> <dt>

**21**
</dt> <dd>

Paramètre non valide.

</dd> </dl>

## <a name="remarks"></a>Notes

La méthode **TakeOwnership** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

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

[\_Fichier de fichier CIM](takeownership-method-in-class-cim-datafile.md)
</dt> <dt>

[**\_Fichier de fichier CIM**](cim-datafile.md)
</dt> <dt>

[Tâches WMI : fichiers et dossiers](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

