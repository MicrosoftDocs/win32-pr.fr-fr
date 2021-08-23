---
description: La méthode d’exportation de l’objet de base de données copie la structure et les données d’une table spécifiée dans un fichier d’archive de texte.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Database. Export, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: faa5e2459eb0fe4ba04fd548bc478c9a0e2c85267e1df8e3d318f4a3f6a082ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745609"
---
# <a name="databaseexport-method"></a>Database. Export, méthode

La méthode d' **exportation** de l’objet [**de base de données**](database-object.md) copie la structure et les données d’une table spécifiée dans un [fichier d’archive de texte](text-archive-files.md).

## <a name="syntax"></a>Syntaxe


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*table* 
</dt> <dd>

Nom requis de la table de base de données. Respecte la casse si vous utilisez la base de données du programme d’installation.

</dd> <dt>

*path* 
</dt> <dd>

Chaîne obligatoire qui correspond au chemin d’accès au dossier dans lequel le fichier texte est placé.

</dd> <dt>

*file* 
</dt> <dd>

Nom requis du fichier à créer. Cela n’inclut pas le dossier, car il doit être défini dans l’objet Path.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




