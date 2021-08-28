---
description: Ajoute des données de trait pour plusieurs traits à IInkAnalyzer et assigne l’identificateur de culture du thread d’entrée actif aux traits.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: 'IInkAnalyzer :: AddStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed8d58100c2d05b2d87af30cab6d4823df645b53ecb62a5e54a7318ba07743a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939989"
---
# <a name="iinkanalyzeraddstrokes-method"></a>IInkAnalyzer :: AddStrokes, méthode

Ajoute des données de trait pour plusieurs traits à [**IInkAnalyzer**](iinkanalyzer.md) et assigne l’identificateur de culture du thread d’entrée actif aux traits.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
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

[**IInkAnalyzer**](iinkanalyzer.md) ajoute les traits à un [**IContextNode**](icontextnode.md) de type UnclassifiedInk (consultez types de [nœuds de contexte](context-node-types.md)). Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).

[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture du thread d’entrée actif aux traits et ajoute les traits au premier nœud de contexte UnclassifiedInk sous le nœud racine de l’analyseur d’encre qui contient des traits avec le même identificateur de culture. Si l’analyseur d’encre n’a pas de nœud avec le même identificateur de culture, il crée un nœud de contexte UnclassifiedInk sous son nœud racine et ajoute les traits au nouveau nœud de contexte UnclassifiedInk.

*plStrokePacketData* contient des données de paquet pour tous les traits. *pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point de chaque trait. Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

> [!Note]  
> Seuls les traits avec les mêmes descriptions de paquets peuvent être ajoutés dans un seul appel à la **méthode IInkAnalyzer :: AddStrokes**.

 

Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la zone et du cadre englobant des traits ajoutés.

Si le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur que l’un des traits à ajouter, le **IInkAnalyzer** retourne un **HRESULT** d' **E \_ INVALIDARG**.

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

[**IInkAnalyzer :: AddStroke, méthode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeForLanguage, méthode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesForLanguage, méthode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: RemoveStroke, méthode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer :: RemoveStrokes, méthode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

