---
description: Ajoute des données de trait pour plusieurs traits à un nœud de reconnaissance personnalisé.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9c50bcd1faa9df94847e3100309fc8598511dd760fa5efd6ccdf84812020fd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719218"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a>IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode

Ajoute des données de trait pour plusieurs traits à un nœud de reconnaissance personnalisé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulStrokeIdsCount* \[ dans\]
</dt> <dd>

Nombre de traits à ajouter.

</dd> <dt>

*plStrokeIds* \[ dans\]
</dt> <dd>

Tableau contenant les identificateurs de trait.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ dans\]
</dt> <dd>

Nombre de propriétés dans chaque paquet.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ dans\]
</dt> <dd>

Tableau contenant les identificateurs de propriété de paquet.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ dans\]
</dt> <dd>

Tableau contenant le nombre de paquets dans chaque trait.

</dd> <dt>

*plStrokePacketData* \[ dans\]
</dt> <dd>

Tableau contenant les données du paquet pour les traits.

</dd> <dt>

*pCustomRecognizer* \[ dans\]
</dt> <dd>

[**IContextNode**](icontextnode.md) de type **CustomRecognizer** auquel ajouter les traits.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ à\]
</dt> <dd>

[**IContextNode**](icontextnode.md) auquel l’analyseur d’encre a ajouté les traits.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeStrokeAddedTo* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Quand *ppContextNodeStrokeAddedTo* a la valeur **null**, il indique que l’appelant ne s’intéresse pas à la valeur de retour de la méthode.

[**IInkAnalyzer**](iinkanalyzer.md) ajoute les traits à un [**IContextNode**](icontextnode.md) de type **CustomRecognizer** (consultez types de [nœuds de contexte](context-node-types.md)). Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).

[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture du thread d’entrée actif aux traits et ajoute les traits au premier nœud **UnclassifiedInk** sous le nœud **CustomRecognizer** . Si aucun nœud **UnclassifiedInk** n’existe, il est créé. Si le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associé au nœud **CustomRecognizer** ne prend pas en charge l’identificateur de culture, le **IInkAnalyzer** continue à analyser et génère un avertissement [**IAnalysisWarning**](ianalysiswarning.md) . Cet avertissement a la valeur [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **AnalysisWarningCode \_ LanguageIdNotRespected**.

*plStrokePacketData* contient des données de paquet pour tous les traits. *pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point de chaque trait. Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

> [!Note]  
> Seuls les traits avec les mêmes descriptions de paquets peuvent être ajoutés dans un seul appel à la **méthode IInkAnalyzer :: AddStrokesToCustomRecognizer**.

 

Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la zone et du cadre englobant des traits ajoutés.

[**IInkAnalyzer**](iinkanalyzer.md) retourne un **HRESULT** d' **E \_ INVALIDARG** dans les circonstances suivantes.

-   Le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur que l’un des traits à ajouter.
-   Le paramètre *pCustomRecognizer* contient un nœud de reconnaissance personnalisé associé à un objet [**IInkAnalyzer**](iinkanalyzer.md) différent.
-   Le paramètre *pCustomRecognizer* contient un [**IContextNode**](icontextnode.md) qui n’est pas de type **CustomRecognizer**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Types de nœuds de contexte](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer :: CreateCustomRecognizer, méthode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

