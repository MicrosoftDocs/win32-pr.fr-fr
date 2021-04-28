---
description: 'Méthode patch. SourceListAddMediaDisk : la méthode SourceListAddMediaDisk ajoute un disque à l’ensemble des disques inscrits. Accepte les VolumeLabel et les DiskPrompt en tant que paramètres. Cette méthode appelle sur MsiSourceListAddMediaDisk.'
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Méthode patch. SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 052831befb95976358b53d989db36d5b2fa43efe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084368"
---
# <a name="patchsourcelistaddmediadisk-method"></a>Méthode patch. SourceListAddMediaDisk

La méthode **SourceListAddMediaDisk** ajoute un disque à l’ensemble des disques inscrits. Accepte *les* *VolumeLabel* et les *DiskPrompt* en tant que paramètres. Cette méthode appelle sur [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

## <a name="syntax"></a>Syntaxe


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DiskId* 
</dt> <dd>

Ce paramètre fournit l’ID du disque en cours d’ajout ou de mise à jour.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Ce paramètre fournit l’étiquette du disque en cours d’ajout ou de mise à jour. Une mise à jour remplace l’étiquette de volume existante dans le registre. Pour modifier l’invite du disque uniquement, récupérez le nom du volume inscrit existant et fournissez-le avec l’invite du nouveau disque. Une chaîne NULL ou vide enregistre une chaîne vide (longueur de 0 octets) comme nom de volume.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Ce paramètre indique l’invite de disque du disque en cours d’ajout ou de mise à jour. Une mise à jour remplace l’invite de disque existante dans le registre. Pour modifier le nom de volume uniquement, récupérez l’invite de disque existante à partir du Registre et fournissez-lui le nouveau nom de volume. Une chaîne NULL ou vide enregistre une chaîne vide (longueur de 0 octets) comme invite de disque.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




