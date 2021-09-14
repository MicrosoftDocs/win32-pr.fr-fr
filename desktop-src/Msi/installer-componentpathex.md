---
description: Retourne un objet RecordList qui donne le chemin d’accès complet d’un composant installé spécifié.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Installer. ComponentPathEx, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121665"
---
# <a name="installercomponentpathex-property"></a>Installer. ComponentPathEx, propriété

Cette propriété retourne un objet [**RecordList**](recordlist-object.md) qui donne le chemin d’accès complet d’un composant installé spécifié. Cette propriété appelle [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cette propriété est disponible à partir de Windows Installer 5,0.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows programme d’installation 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




