---
description: La propriété ModuleKeys en lecture seule de l’objet Error retourne un pointeur vers une collection de chaînes contenant les clés primaires de la ligne dans le module à l’origine de l’erreur, une clé par entrée dans la collection.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Erreur. ModuleKeys, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d33b546bea909700cc1a737043947d980006764daa86771820740570adf7f80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044599"
---
# <a name="errormodulekeys-property"></a>Error. ModuleKeys, propriété

La propriété **ModuleKeys** en lecture seule de l’objet [**Error**](error-object.md) retourne un pointeur vers une collection de chaînes contenant les clés primaires de la ligne dans le module à l’origine de l’erreur, une clé par entrée dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Le client est responsable de la libération de la collection de chaînes lorsqu’il n’est plus nécessaire.

La collection est vide si les valeurs ne s’appliquent pas au type de l’erreur. Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .

### <a name="c"></a>C++

Consultez la fonction [**obtenir \_ ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

