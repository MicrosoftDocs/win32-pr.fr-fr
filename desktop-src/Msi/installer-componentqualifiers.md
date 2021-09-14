---
description: La propriété ComponentQualifiers est une propriété en lecture seule qui retourne un objet StringList énumérant l’ensemble des qualificateurs inscrits pour le composant spécifié.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Installer. ComponentQualifiers, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121662"
---
# <a name="installercomponentqualifiers-property"></a>Installer. ComponentQualifiers, propriété

La propriété **ComponentQualifiers** est une propriété en lecture seule qui retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des qualificateurs inscrits pour le composant spécifié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a>Valeur de la propriété

GUID de chaîne qui représente la catégorie du [composant](publishcomponent-table.md).

## <a name="remarks"></a>Notes

Pour énumérer les qualificateurs, l’application itère au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each. Étant donné que les qualificateurs ne sont pas triés, tout nouveau qualificateur a un index arbitraire, ce qui signifie que la fonction peut retourner des qualificateurs dans n’importe quel ordre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




