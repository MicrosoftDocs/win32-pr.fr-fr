---
description: La propriété PatchFiles retourne un objet StringList qui contient une liste de fichiers qui peuvent être mis à jour par la liste de correctifs fournie.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Installer. PatchFiles, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012116"
---
# <a name="installerpatchfiles-property"></a>Installer. PatchFiles, propriété

La propriété **PatchFiles** retourne un objet [**StringList**](stringlist-object.md) qui contient une liste de fichiers qui peuvent être mis à jour par la liste de correctifs fournie. Cette propriété appelle [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista). Pour plus d’informations sur l’utilisation de la propriété **PatchFiles** [, consultez Liste des fichiers qui peuvent être mis à jour](listing-the-files-that-can-be-updated.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 4,5 sur Windows Server 2003 et Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet installer**](installer-object.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




