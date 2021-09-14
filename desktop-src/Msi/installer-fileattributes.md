---
description: La propriété FileAttributes de l’objet installer retourne un nombre qui représente les attributs de fichier combinés pour le chemin d’accès désigné à un fichier ou un dossier.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Installer. FileAttributes, propriété (Windows. storage. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121602"
---
# <a name="installerfileattributes-property"></a>Installer. FileAttributes, propriété

La propriété **FileAttributes** de l’objet [**installer**](installer-object.md) retourne un nombre qui représente les attributs de fichier combinés pour le chemin d’accès désigné à un fichier ou un dossier.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Valeur de la propriété

Chemin d’accès au fichier ou dossier requis. Un chemin d’accès partiel suppose le répertoire actif.

## <a name="remarks"></a>Notes

La propriété **FileAttributes** retourne les valeurs suivantes.



| Attribut de fichier              | Valeur      | Valeur |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| attribut de fichier \_ \_ temporaire  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2 048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Retourne – 1 si le fichier ou le dossier n’existe pas ou n’est pas accessible.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| En-tête<br/>  | <dl> <dt>Windows. storage. h</dt> </dl>                                                                                                                                                            |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




