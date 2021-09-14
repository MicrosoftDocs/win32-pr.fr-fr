---
description: La méthode SourceListClearMediaDisk de l’objet patch supprime un disque spécifié de l’ensemble des disques inscrits pour un correctif. Accepte le dédérapageur en tant que paramètre. Cette méthode appelle MsiSourceListClearMediaDisk.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Méthode patch. SourceListClearMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 722b4573d89214312e77e4fde78e1905aefa885f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123649"
---
# <a name="patchsourcelistclearmediadisk-method"></a>Méthode patch. SourceListClearMediaDisk

La méthode **SourceListClearMediaDisk** de l’objet [**patch**](patch-object.md) supprime un disque spécifié de l’ensemble des disques inscrits pour un correctif. Accepte le *dédérapageur* en tant que paramètre. Cette méthode appelle [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).

## <a name="syntax"></a>Syntaxe


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DiskId* 
</dt> <dd>

Ce paramètre fournit l’ID du disque à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

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

[**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




