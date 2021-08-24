---
description: Modifie la valeur qui indique si ce IContextNode est partiellement ou entièrement rempli.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'IContextNode :: SetPartiallyPopulated, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df87085a82117a694b48d08c3e6e1f8500c8959060052f553a53f1a285d9707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713462"
---
# <a name="icontextnodesetpartiallypopulated-method"></a>IContextNode :: SetPartiallyPopulated, méthode

Modifie la valeur qui indique si ce [**IContextNode**](icontextnode.md) est partiellement ou entièrement rempli.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fPartiallyPopulated* \[ dans\]
</dt> <dd>

**Variante \_ TRUE** si ce [**IContextNode**](icontextnode.md) est partiellement rempli ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Utilisez cette méthode lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Pour plus d’informations, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

Lors de la virtualisation de votre arborescence de documents, veillez à définir la valeur PropertyGuidsForContextNodes. RotatedBoundingBox (à l’aide de ContextNode. AddPropertyValue) sur tous les objets ContextNode. La propriété RotatedBoundingBox est calculée par le InkAnalyzer et doit être définie par défaut sur tous les ContextNodes d’écriture. Toutefois, si votre application virtualise les résultats de l’analyse en définissant la propriété PartiallyPopulated, lors de la gestion de l’événement PopulateContextNode, veillez à remplir la propriété RotatedBoundingBox. Si vous ne définissez pas la propriété RotatedBoundingBox, vous risquez d’utiliser des données de document potentiellement plus utilisées dans l’opération d’analyse en cours

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

[**\_IAnalysisProxyEvents ::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




