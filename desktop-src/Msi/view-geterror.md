---
description: La méthode GetError de l’objet View retourne l’erreur de validation et le nom de la colonne pour laquelle l’erreur s’est produite.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: Vue. GetError, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ddbed26565598ad58b3605b7c70a9a5bbede3e5282ff4a7fa011df5c56bd8b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038799"
---
# <a name="viewgeterror-method"></a>Vue. GetError, méthode

La méthode **GetError** de l’objet [**View**](view-object.md) retourne l’erreur de validation et le nom de la colonne pour laquelle l’erreur s’est produite. Dans Automation, la valeur retournée est une chaîne au format \# \# ColumnName, où \# \# représente un code d’erreur à deux chiffres. Elle retourne la première erreur dans le tableau d’erreurs de la vue ; les appels suivants retournent la valeur suivante dans le tableau d’erreurs. Une fois qu’une valeur de « 00 » est retournée, il n’y a plus d’erreurs, et les appels suivants font simplement une nouvelle boucle sur le tableau.

## <a name="syntax"></a>Syntaxe


```JScript
View.GetError()
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
| IID<br/>     | L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




