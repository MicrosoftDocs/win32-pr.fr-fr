---
description: La méthode Rename renomme le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet.
ms.assetid: 3eaf9f4f-270e-41d0-86ae-c5edb1850ef5
ms.tgt_platform: multiple
title: Renommer la méthode de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aea061990a6d3bd52a98dc9101102059767ecf9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111259"
---
# <a name="rename-method-of-the-cim_datafile-class"></a>Renommer la méthode de la \_ classe de fichier de fichier CIM

La méthode **Rename** renomme le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet. Un changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire. Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du fichier* \[ dans\]
</dt> <dd>

Nouveau nom complet du fichier (ou répertoire).

Exemple : « c : \\ temp \\newfile.txt »

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Opération réussie.

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

La méthode **Rename** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.

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

[\_Fichier de fichier CIM](rename-method-in-class-cim-datafile.md)
</dt> <dt>

[**\_Fichier de fichier CIM**](cim-datafile.md)
</dt> <dt>

[Tâches WMI : fichiers et dossiers](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

