---
description: La méthode Close de l’objet View met fin à l’exécution de la requête et libère les ressources de la base de données.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532885"
---
# <a name="viewclose-method"></a>View. Close, méthode

La méthode **Close** de l’objet [**View**](view-object.md) met fin à l’exécution de la requête et libère les ressources de la base de données.

## <a name="syntax"></a>Syntaxe


```JScript
View.Close()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode doit être appelée avant que la méthode [**Execute**](view-execute.md) soit appelée à nouveau sur l’objet [**View**](view-object.md) , à moins que toutes les lignes du jeu de résultats aient été obtenues avec la méthode [**Fetch**](view-fetch.md) . Elle est appelée en interne lorsque la vue est détruite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




