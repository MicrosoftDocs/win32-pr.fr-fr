---
description: La propriété SourceListInfo de l’objet Product obtient et définit les propriétés d’informations relatives à la source d’un produit. Cette propriété appelle MsiSourceListGetInfo ou MsiSourceListSetInfo. Il s’agit d’une propriété de lecture ou d’écriture.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Propriété Product. SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009778"
---
# <a name="productsourcelistinfo-property"></a>Propriété Product. SourceListInfo

La propriété **SourceListInfo** de l’objet [**Product**](product-object.md) obtient et définit les propriétés d’informations relatives à la source d’un produit. Cette propriété appelle [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) ou [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa). Il s’agit d’une propriété de lecture ou d’écriture.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a>Valeur de la propriété

Nom des propriétés d’informations sources d’un produit à interroger ou définir. Pour connaître les valeurs possibles, consultez la section Notes de cette rubrique.

## <a name="remarks"></a>Notes

Toutes les propriétés qui peuvent être récupérées ne peuvent pas être définies. Le paramètre *szProperty* peut avoir l’une des valeurs suivantes.



| Propriété         | Pouvez-vous définir ? | Signification                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | O        | Chemin d’accès relatif à la racine du support d’installation.                                                                                                                                                                                                       |
| DiskPrompt       | O        | Modèle d’invite utilisé pour inviter l’utilisateur à fournir un support d’installation.                                                                                                                                                                                       |
| LastUsedSource   | O        | Emplacement source utilisé le plus récemment pour le produit. Lorsque vous définissez cette propriété, faites précéder l’emplacement source de « n ; » pour une source réseau ou « u ; » pour le type d’URL. Par exemple, «n ; \\ \\ Scratch \\ éraflures \\ » et « u ; https://MyServer/MyFolder/MySource ». |
| LastUsedType     | N        | « n » si la dernière source utilisée est un emplacement réseau. « u » si la dernière source utilisée était un emplacement d’URL. « m » si la dernière source utilisée était un média. Chaîne vide ("") s’il n’existe aucune dernière source utilisée.                                                                   |
| PackageName      | O        | nom du package de Windows Installer ou du package correctif sur la source.                                                                                                                                                                                      |



 

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

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




