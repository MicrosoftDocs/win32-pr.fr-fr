---
description: En savoir plus sur l’interface IAMFilterData, qui convertit les informations de filtre en données binaires compressées. Cette interface a été déconseillée.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interface IAMFilterData (fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1e43e0f16ddfdee596f0dc6bd736ed86fc6fa37d
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989434"
---
# <a name="iamfilterdata-interface"></a>Interface IAMFilterData

> [!Note]  
> Cette interface a été déconseillée. Les nouvelles applications doivent utiliser l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) à la place.

 

L' `IAMFilterData` interface convertit les informations de filtre en données binaires compressées, qui peuvent être stockées dans le registre. L’objet mappeur de filtre expose cette interface.

## <a name="members"></a>Membres

L’interface **IAMFilterData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMFilterData** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMFilterData** possède ces méthodes.



| Méthode                                                     | Description                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**CreateFilterData**](iamfilterdata-createfilterdata.md) | Crée des données de Registre binaires pour un filtre.<br/>     |
| [**ParseFilterData**](iamfilterdata-parsefilterdata.md)   | Décompresse les données de Registre binaires pour un filtre.<br/> |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> L’en-tête de \_ données. h se trouve dans le répertoire de l' [exemple du mappeur](mapper-sample.md) dans le SDK Windows.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Données de fil \_ . h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces déconseillées](deprecated-interfaces.md)
</dt> </dl>

 

 
