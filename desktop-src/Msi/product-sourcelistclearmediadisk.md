---
description: La méthode SourceListClearMediaDisk de l’objet Product supprime un disque spécifié de l’ensemble des disques inscrits pour un produit. Accepte le dédérapageur en tant que paramètre. Cette méthode appelle MsiSourceListClearMediaDisk.
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: Méthode Product. SourceListClearMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6e1115c8c2c02078dc9de08d3e0f64b08272dadc7309af5c7a3bbcf4134ee152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074719"
---
# <a name="productsourcelistclearmediadisk-method"></a>Méthode Product. SourceListClearMediaDisk

La méthode **SourceListClearMediaDisk** de l’objet [**Product**](product-object.md) supprime un disque spécifié de l’ensemble des disques inscrits pour un produit. Accepte le *dédérapageur* en tant que paramètre. Cette méthode appelle [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).

## <a name="syntax"></a>Syntaxe


```JScript
Product.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DiskId* 
</dt> <dd>

Ce paramètre fournit l’ID du disque à supprimer.

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

[**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




