---
description: Récupère la valeur qui indique si un objet IContextNode est partiellement rempli ou entièrement rempli.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'IContextNode :: GetPartiallyPopulated, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2fab5b5fce4d87c32fb3435fdad2cfc6b126069b40c7e5c7c2fb302ee468e480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773799"
---
# <a name="icontextnodegetpartiallypopulated-method"></a>IContextNode :: GetPartiallyPopulated, méthode

Récupère la valeur qui indique si un objet [**IContextNode**](icontextnode.md) est partiellement rempli ou entièrement rempli.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pfPartiallyPopulated* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si cet objet [**IContextNode**](icontextnode.md) ne contient pas de données complètes ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Utilisez cette méthode lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Pour plus d’informations, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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
</dt> <dt>

[**IContextNode::SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**\_IAnalysisProxyEvents ::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




