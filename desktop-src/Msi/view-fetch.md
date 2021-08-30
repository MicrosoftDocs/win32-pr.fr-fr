---
description: La méthode fetch de l’objet View récupère la ligne suivante de données de colonne si davantage de lignes sont disponibles dans le jeu de résultats, sinon elle a la valeur null. Appelez la méthode Execute avant la méthode fetch.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. Fetch, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b05144b542fd1daa1fc59e12d8ab9ec7031c4a3a5eb6506e9d1316a29b4424ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039489"
---
# <a name="viewfetch-method"></a>View. Fetch, méthode

La méthode **Fetch** de l’objet [**View**](view-object.md) récupère la ligne suivante de données de colonne si davantage de lignes sont disponibles dans le jeu de résultats, sinon elle a la valeur null. Appelez la méthode [**Execute**](view-execute.md) avant la méthode **Fetch** .

## <a name="syntax"></a>Syntaxe


```JScript
View.Fetch()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le même objet d' [**enregistrement**](record-object.md) doit être utilisé pour récupérer les données dans plusieurs lignes, sinon l’objet doit être libéré en étant hors de portée. L’enregistrement peut être testé pour la fin du jeu de résultats à l’aide de la syntaxe « if FetchRecord Is Nothing ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




