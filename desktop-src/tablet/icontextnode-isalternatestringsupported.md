---
description: Indique si la chaîne reconnue spécifiée provient du dictionnaire système, du dictionnaire de l’utilisateur ou de la liste de mots.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'IContextNode :: IsAlternateStringSupported, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cbf18c63ce81a439092ba3bdabfae38c5f52882ec5364ef5c8fbd67cab5d81a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266299"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>IContextNode :: IsAlternateStringSupported, méthode

Indique si la chaîne reconnue spécifiée provient du dictionnaire système, du dictionnaire de l’utilisateur ou de la liste de mots. Toutes les données qui restreignent, telles que les listes de mots, les repères ou les Factoids, dans n’importe quel nœud d’indication correspondant seront utilisées pour déterminer si la chaîne est prise en charge.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAlternateString* \[ dans\]
</dt> <dd>

Chaîne reconnue à vérifier.

</dd> <dt>

*pfIsSupported* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si la chaîne spécifiée est prise en charge par le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) avec les nœuds indicateurs correspondants appliqués ; **Variante \_ FALSe** s’il n’est pas pris en charge.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 




