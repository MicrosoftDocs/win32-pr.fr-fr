---
description: Le filtre de convertisseur null est un convertisseur qui ignore chaque échantillon qu’il reçoit, sans afficher ou restituer les exemples de données.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtre de convertisseur null (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312386"
---
# <a name="null-renderer-filter"></a>Filtre de convertisseur null

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

Le filtre de convertisseur null est un convertisseur qui ignore chaque échantillon qu’il reçoit, sans afficher ou restituer les exemples de données.



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| Types de média de broche d’entrée                    | Tout type de média                                                                                                       |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| Types de média de broche de sortie                   | Non applicable.                                                                                                      |
| Interfaces de broche de sortie                    | Non applicable.                                                                                                      |
| CLSID du filtre                             | CLSID \_ NullRenderer                                                                                                  |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                                    |
| Exécutable                               | Qedit.dll                                                                                                            |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                  |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                        |



 

## <a name="remarks"></a>Remarques

Utilisez ce filtre quand une broche de sortie dans le graphique nécessite une connexion en aval, mais que vous ne souhaitez pas afficher les données à partir de ce code confidentiel. En connectant la broche de sortie au convertisseur null, vous terminez la connexion sans restituer les données.

Même si ce filtre n’affiche aucun échantillon, il attend la durée de présentation de chaque exemple avant d’ignorer l’exemple. Par conséquent, le graphique s’exécutera au taux normal. Si vous souhaitez que le graphique s’exécute aussi rapidement que possible, affectez la **valeur null** à l’horloge de référence. pour plus d’informations, consultez [définition de l’horloge de Graph](setting-the-graph-clock.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Modification des objets de services](directshow-editing-services-objects.md)
</dt> </dl>

 

 




