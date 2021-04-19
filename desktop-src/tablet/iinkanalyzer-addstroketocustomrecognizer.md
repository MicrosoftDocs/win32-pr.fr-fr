---
description: Ajoute des données de trait pour un seul trait à un nœud de reconnaissance personnalisé.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516478"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a>IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode

Ajoute des données de trait pour un seul trait à un nœud de reconnaissance personnalisé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulStrokeId* \[ dans\]
</dt> <dd>

Identificateur du trait à ajouter.

</dd> <dt>

*ulStrokePacketDataCount* \[ dans\]
</dt> <dd>

Nombre de paquets dans le trait.

</dd> <dt>

*plStrokePacketData* \[ dans\]
</dt> <dd>

Tableau contenant les données de paquet pour le trait.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ dans\]
</dt> <dd>

Nombre de propriétés de paquet dans chaque paquet.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ dans\]
</dt> <dd>

Tableau contenant les identificateurs de propriété de paquet.

</dd> <dt>

*pCustomRecognizer* \[ dans\]
</dt> <dd>

[**IContextNode**](icontextnode.md) de type **CustomRecognizer** auquel ajouter le trait.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ à\]
</dt> <dd>

[**IContextNode**](icontextnode.md) auquel l’analyseur d’encre a ajouté le trait.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeStrokeAddedTo* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Quand *ppContextNodeStrokeAddedTo* a la valeur **null**, il indique que l’appelant ne s’intéresse pas à la valeur de retour de la méthode.

[**IInkAnalyzer**](iinkanalyzer.md) ajoute le trait à un [**IContextNode**](icontextnode.md) de type **CustomRecognizer** (consultez [types de nœuds de contexte](context-node-types.md)). Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).

[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture du thread d’entrée actif au trait et ajoute le trait au premier nœud **UnclassifiedInk** sous le nœud **CustomRecognizer** . Si aucun nœud **UnclassifiedInk** n’existe, il est créé. Si le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associé au nœud **CustomRecognizer** ne prend pas en charge l’identificateur de culture, le **IInkAnalyzer** continue à analyser et génère un avertissement [**IAnalysisWarning**](ianalysiswarning.md) . Cet avertissement a la valeur [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **AnalysisWarningCode \_ LanguageIdNotRespected**.

*plStrokePacketData* contient des données de paquet pour tous les points du trait. *pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point de chaque trait. Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la région et de la zone englobante du trait ajouté.

[**IInkAnalyzer**](iinkanalyzer.md) retourne un **HRESULT** d' **E \_ INVALIDARG** dans les circonstances suivantes.

-   Le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur que le trait à ajouter.
-   Le paramètre *pCustomRecognizer* contient un nœud de reconnaissance personnalisé associé à un objet [**IInkAnalyzer**](iinkanalyzer.md) différent.
-   Le paramètre *pCustomRecognizer* contient un [**IContextNode**](icontextnode.md) qui n’est pas de type **CustomRecognizer**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Types de nœuds de contexte](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer :: CreateCustomRecognizer, méthode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

