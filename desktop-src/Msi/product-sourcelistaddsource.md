---
description: La méthode SourceListAddSource ajoute un réseau ou une source d’URL. Accepte SourcePath, type et index comme paramètres. Cette méthode appelle MsiSourceListAddSourceEx.
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: Méthode Product. SourceListAddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b95185cbd25354314eace5da7704da51dbbefe024ba8597c0eed41a688984117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925869"
---
# <a name="productsourcelistaddsource-method"></a>Méthode Product. SourceListAddSource

La méthode **SourceListAddSource** ajoute un réseau ou une source d’URL. Accepte *SourcePath*,*type* et *index* comme paramètres. Cette méthode appelle [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).

## <a name="syntax"></a>Syntaxe


```JScript
Product.SourceListAddSource(
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

Si **SourceListAddSource** est appelé avec une nouvelle source et que l' *index* a la valeur 0, le programme d’installation ajoute la source à la fin de la liste source.

Si cette fonction est appelée avec une source déjà existante dans la liste source et l' *index* a la valeur 0, le programme d’installation conserve l’index existant de la source.

Si la fonction est appelée avec une source existante dans la liste source et que l' *index* a une valeur différente de zéro, la source est supprimée de son emplacement actuel dans la liste et insérée à la position spécifiée par l' *index*, avant toute source qui existe déjà à cette position.

Si la fonction est appelée avec une nouvelle source et que l' *index* est défini sur une valeur différente de zéro, la source est insérée à la position spécifiée par l' *index*, avant toute source qui existe déjà à cette position. La valeur d’index pour toutes les sources de la liste après l’index spécifié par l' *index* est mise à jour pour s’assurer que les valeurs d’index uniques et que la commande préexistante reste inchangée.

Si l' *index* est supérieur au nombre de sources dans la liste, la source est placée à la fin de la liste avec une valeur d’index supérieure à une source existante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Production**](product-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




