---
description: La propriété MediaDisks énumère tous les disques multimédias pour cette instance de produit. Cette propriété appelle MsiSourceListEnumMediaDisks. Retourne les informations de disque sous la forme d’un tableau d’objets d’enregistrement.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Patch. MediaDisks, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218745"
---
# <a name="patchmediadisks-property"></a>Patch. MediaDisks, propriété

La propriété **MediaDisks** énumère tous les disques multimédias pour cette instance de produit. Cette propriété appelle [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa). Retourne les informations de disque sous la forme d’un tableau d’objets d' [**enregistrement**](record-object.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Dans chaque enregistrement, le premier champ contient l’ID de disque, le deuxième le nom de volume et le troisième l’invite de disque inscrite pour le disque.

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

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[**Enregistrement**](record-object.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




