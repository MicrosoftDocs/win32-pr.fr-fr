---
description: La méthode SourceListAddSource ajoute un réseau ou une source d’URL. Accepte SourcePath, le type et l’index en tant que paramètres. Cette méthode appelle MsiSourceListAddSourceEx.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Méthode patch. SourceListAddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc0a3bc0d966ec6836d1523745b296350562aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543170"
---
# <a name="patchsourcelistaddsource-method"></a>Méthode patch. SourceListAddSource

La méthode **SourceListAddSource** ajoute un réseau ou une source d’URL. Accepte *SourcePath*, le *type* et l' *index* en tant que paramètres. Cette méthode appelle [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).

## <a name="syntax"></a>Syntaxe


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Type* 
</dt> <dd>

Type de source à ajouter : MSISOURCETYPE \_ réseau ou URL MSISOURCETYPE \_ .

</dd> <dt>

*SourcePath* 
</dt> <dd>

Chemin d’accès à la source à ajouter.

</dd> <dt>

*Index* 
</dt> <dd>

Si **SourceListAddSource** est appelé avec une nouvelle source et un nouvel *index* défini sur 0, le programme d’installation ajoute la source à la fin de la liste source.

Si cette fonction est appelée avec une source déjà existante dans la liste source et l' *index* a la valeur 0, le programme d’installation conserve l’index existant de la source.

Si la fonction est appelée avec une source existante dans la liste source et que l' *index* a une valeur différente de zéro, la source est supprimée de son emplacement actuel dans la liste et insérée à la position spécifiée par l' *index*, avant toute source qui existe déjà à cette position.

Si la fonction est appelée avec une nouvelle source et que l' *index* est défini sur une valeur différente de zéro, la source est insérée à la position spécifiée par l' *index*, avant toute source qui existe déjà à cette position. La valeur d’index pour toutes les sources de la liste après l’index spécifié par l' *index* est mise à jour pour garantir que les valeurs d’index uniques et la commande préexistante restent inchangées.

Si l' *index* est supérieur au nombre de sources dans la liste, la source est placée à la fin de la liste avec une valeur d’index supérieure à une source existante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Correctif**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




