---
description: La méthode FileHash de l’objet installer prend le chemin d’accès à un fichier et retourne un hachage 128 bits de ce fichier. Les informations de hachage de fichier sont retournées en tant qu’objet enregistrement. L’intégralité du hachage de fichier 128 bits est retournée en tant que champs de propriété IntegerData 4 32 bits.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Installer. FileHash, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a2da76ef3f0606002e26e8c320f83ca45e46bbbeb573d509c235c9fca8932247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630790"
---
# <a name="installerfilehash-method"></a>Installer. FileHash, méthode

La méthode **FileHash** de l' [**objet installer**](installer-object.md) prend le chemin d’accès à un fichier et retourne un hachage 128 bits de ce fichier. Les informations de hachage de fichier sont retournées en tant qu' [**objet enregistrement**](record-object.md). L’intégralité du hachage de fichier 128 bits est retournée en tant que champs de propriété [**IntegerData**](record-integerdata.md) 4 32 bits.

Les valeurs retournées dans l' [**objet record**](record-object.md) correspondent aux quatre champs de la structure [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) retournée par [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). La numérotation de quatre champs est basée sur 1 dans la [table MsiFileHash](msifilehash-table.md).

-   Le champ 1 correspond à la colonne HashPart1.
-   Le champ 2 correspond à la colonne HashPart2.
-   Le champ 3 correspond à la colonne HashPart3.
-   Le champ 4 correspond à la colonne HashPart4.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FilePath* 
</dt> <dd>

Chemin d’accès au fichier à hacher.

</dd> <dt>

*Options* 
</dt> <dd>

Réservé pour un usage futur.

La valeur de ce paramètre doit être 0 (zéro).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette méthode retourne un [**objet enregistrement**](record-object.md) qui contient le hachage du fichier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de version de fichier par défaut](default-file-versioning.md)
</dt> <dt>

[Gérer les tailles et les versions des fichiers](manage-file-sizes-and-versions.md)
</dt> <dt>

[Table MsiFileHash](msifilehash-table.md)
</dt> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




