---
description: Indique si la chaîne reconnue de ce IContextNode provient du dictionnaire système, du dictionnaire de l’utilisateur ou de la liste de mots.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'IContextNode :: IsStringSupported, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2eef383f059897665c013e3575d452564295ccd9bd014ae8084fd1635892bd99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709109"
---
# <a name="icontextnodeisstringsupported-method"></a>IContextNode :: IsStringSupported, méthode

Indique si la chaîne reconnue de ce [**IContextNode**](icontextnode.md) provient du dictionnaire système, du dictionnaire de l’utilisateur ou de la liste de mots.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pfIsSupported* \[ out, retval\]
</dt> <dd>

**Variante \_ TRUE** si la valeur de chaîne reconnue de ce [**IContextNode**](icontextnode.md) est prise en charge par le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) avec les nœuds indicateurs correspondants appliqués ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="requirements"></a>Configuration requise



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

 

 




