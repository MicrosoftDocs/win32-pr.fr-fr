---
description: La propriété SourceListInfo de l’objet patch obtient et définit les propriétés d’informations relatives à la source d’un correctif. Cette propriété appelle MsiSourceListGetInfo ou MsiSourceListSetInfo. Il s’agit d’une propriété de lecture ou d’écriture.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Patch. SourceListInfo, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123638"
---
# <a name="patchsourcelistinfo-property"></a>Patch. SourceListInfo, propriété

La propriété **SourceListInfo** de l’objet [**patch**](patch-object.md) obtient et définit les propriétés d’informations relatives à la source d’un correctif. Cette propriété appelle [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) ou [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa). Il s’agit d’une propriété de lecture ou d’écriture.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a>Valeur de la propriété

Nom des propriétés d’informations sources d’un correctif à interroger ou définir. Pour connaître les valeurs possibles, consultez la section Notes de cette rubrique.

## <a name="remarks"></a>Notes

Toutes les propriétés qui peuvent être récupérées ne peuvent pas être définies. Le paramètre *szProperty* peut avoir l’une des valeurs suivantes.



| Propriété         | Pouvez-vous définir ? | Signification                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | O        | Chemin d’accès relatif à la racine du support d’installation.                                                                                                                                                                                                          |
| DiskPrompt       | O        | Modèle d’invite utilisé pour inviter l’utilisateur à fournir un support d’installation.                                                                                                                                                                                          |
| LastUsedSource   | O        | Emplacement source utilisé le plus récemment pour le correctif. Lorsque vous définissez cette propriété, faites précéder l’emplacement source de « n ; » pour une source réseau ou « u ; » pour le type d’URL. Par exemple, utilisez «n ; \\ \\ éraflure \\ Scratch \\ test» ou « u ; https://microsoft.com/Patches/Office/SP1 ». |
| LastUsedType     | N        | « n » si la dernière source utilisée est un emplacement réseau. « u » si la dernière source utilisée était un emplacement d’URL. « m » si la dernière source utilisée était un média. Chaîne vide ("") s’il n’existe aucune dernière source utilisée.                                                                      |
| PackageName      | O        | nom du package de Windows Installer ou du package correctif sur la source.                                                                                                                                                                                         |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Correctif**](patch-object.md)
</dt> <dt>

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




