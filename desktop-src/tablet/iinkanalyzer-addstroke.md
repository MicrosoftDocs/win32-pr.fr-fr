---
description: Ajoute des données de trait pour un seul trait à IInkAnalyzer et assigne l’identificateur de culture du thread d’entrée actif au trait.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'IInkAnalyzer :: AddStroke, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f7ba08e779e115c243918d94e5b41e8a7d77f54fab92b045274135ead2ae0264
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590589"
---
# <a name="iinkanalyzeraddstroke-method"></a>IInkAnalyzer :: AddStroke, méthode

Ajoute des données de trait pour un seul trait à [**IInkAnalyzer**](iinkanalyzer.md) et assigne l’identificateur de culture du thread d’entrée actif au trait.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lStrokeId* \[ dans\]
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

*ppContextNodeStrokeAddedTo* \[ à\]
</dt> <dd>

Pointeur vers le [**IContextNode**](icontextnode.md) auquel le [**IInkAnalyzer**](iinkanalyzer.md) a ajouté le trait.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeStrokeAddedTo* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Quand *ppContextNodeStrokeAddedTo* a la valeur **null**, il indique que l’appelant ne s’intéresse pas à la valeur de retour de la méthode.

[**IInkAnalyzer**](iinkanalyzer.md) ajoute le trait à un [**IContextNode**](icontextnode.md) de type UnclassifiedInk (consultez [types de nœuds de contexte](context-node-types.md)). Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).

[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture du thread d’entrée actif au trait et ajoute le trait au premier nœud de contexte UnclassifiedInk sous le nœud racine de l’analyseur d’encre qui contient des traits avec le même identificateur de culture. Si l’analyseur d’encre n’a pas de nœud avec le même identificateur de culture, il crée un nœud de contexte UnclassifiedInk sous son nœud racine et ajoute le trait au nouveau nœud de contexte UnclassifiedInk.

*plStrokePacketData* contient des données de paquet pour tous les points du trait. *pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point du trait. Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la région et de la zone englobante du trait ajouté.

Si le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur de trait, le **IInkAnalyzer** retourne un **HRESULT** d' **E \_ INVALIDARG**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeForLanguage, méthode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokes, méthode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesForLanguage, méthode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: RemoveStroke, méthode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer :: RemoveStrokes, méthode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

