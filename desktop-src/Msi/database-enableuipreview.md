---
description: La méthode EnableUIPreview de l’objet de base de données facilite la création de boîtes de dialogue et de panneaux en fournissant la prise en charge nécessaire pour afficher les boîtes de dialogue de l’interface utilisateur stockées dans la base de données du programme d’installation.
ms.assetid: c4687de7-8ab4-4377-ac5c-1fed7c915519
title: Database. EnableUIPreview, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.EnableUIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7631b1d2d6becffcfcec7078c58dbe9469827beefea07b80dbb04a1295119fe6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745719"
---
# <a name="databaseenableuipreview-method"></a>Database. EnableUIPreview, méthode

La méthode **EnableUIPreview** de l’objet [**de base de données**](database-object.md) facilite la création de boîtes de dialogue et de panneaux en fournissant la prise en charge nécessaire pour afficher les boîtes de dialogue de l’interface utilisateur stockées dans la base de données du programme d’installation. La méthode démarre le mode aperçu en retournant un objet **de base de données** en aperçu. Le mode aperçu se termine lorsque l’objet Preview est relâché.

## <a name="syntax"></a>Syntaxe


```JScript
Database.EnableUIPreview()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




