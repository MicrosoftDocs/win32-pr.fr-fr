---
description: La propriété features est une propriété en lecture seule qui retourne un objet StringList énumérant l’ensemble des fonctionnalités publiées pour le produit spécifié.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Installer. Features, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121610"
---
# <a name="installerfeatures-property"></a>Installer. Features, propriété

La propriété **features** est une propriété en lecture seule qui retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des fonctionnalités publiées pour le produit spécifié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie le code de produit du produit.

## <a name="remarks"></a>Notes

Pour énumérer les fonctionnalités, une application itère au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each. Étant donné que les fonctionnalités ne sont pas ordonnées, toutes les nouvelles fonctionnalités ont un index arbitraire, ce qui signifie que la fonction peut retourner des fonctionnalités dans n’importe quel ordre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[Fonctions d’État du système](installer-function-reference.md)
</dt> </dl>

 

 




