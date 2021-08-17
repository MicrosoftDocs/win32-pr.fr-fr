---
description: Implémentation du codec.
ms.assetid: 5ec23f95-cc7d-4c16-979a-f1d2cc485bb0
title: Implémentation de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1bb9c51788526d68b370dec782b433e6f8d7114ece2b4f5a735ef7662f869d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974858"
---
# <a name="codec-implementation"></a>Implémentation de codec

les codecs vidéo et Windows Media Audio sont implémentés en tant qu’objets COM. En règle générale, un codec est implémenté en tant que paire d’objets COM : un pour l’encodeur et un pour le décodeur. L’encodeur a un identificateur de classe (CLSID) et le décodeur a un CLSID différent. par exemple, la partie encodeur du codec Windows Media Audio 9 a un clsid représenté par la constante **clsid \_ CWMAEncMediaObject**, et la partie décodeur de ce même codec a un clsid représenté par la constante **clsid \_ CWMADecMediaObject**.

Dans certains cas, plusieurs encodeurs sont inclus dans un seul objet COM. par exemple, l’encodeur Windows Media Video 9 et l’encodeur Windows Media Video 9,1 font tous deux partie du même objet COM. Par conséquent, elles ont toutes les deux le même CLSID, qui est représenté par la constante **CLSID \_ CWMV9EncMediaObject**. De même, certains objets COM incluent plus d’un décodeur.

chaque objet encodeur ou décodeur expose l’interface [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) afin que l’objet puisse être utilisé en tant qu’objet DirectX Media (DMO) et l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).

pour la plupart des encodeurs, que vous utilisiez ou non l’encodeur en tant que DMO ou MFT, vous utilisez le même CLSID pour créer une instance de l’encodeur. par exemple, pour créer une instance de l’encodeur Windows Media Video 9, vous utilisez le **CLSID \_ CWMV9EncMediaObject**, que vous souhaitiez utiliser l’encodeur en tant que DMO ou MFT. de même, pour la plupart des décodeurs, chaque décodeur a un seul CLSID, que vous utilisiez ou non le décodeur en tant que DMO ou MFT.

> [!Note]  
> il existe quelques exceptions à l’instruction précédente sur l’utilisation d’un CLSID unique pour la DMO et la table MFT. par exemple, le décodeur MPEG-4 Part 2 possède un clsid lorsqu’il joue le rôle d’un DMO et d’un clsid différent lorsqu’il agit en tant que MFT.

 

Outre les interfaces de base, chaque objet encodeur ou décodeur implémente deux interfaces similaires pour l’utilisation des propriétés de codec, **IPropertyBag** et **IPropertyStore**. Les versions antérieures des objets encodeur et décodeur utilisaient **IPropertyBag**, qui identifie chaque propriété par une valeur de chaîne contenant un nom de propriété. **IPropertyStore** est une interface plus récente qui identifie les propriétés avec une valeur de clé de propriété unique. La prise en charge de **IPropertyStore** a été ajoutée pour assurer la prise en charge de MFTS. La plupart des chaînes de nom de propriété **IPropertyBag** ont un GUID de clé de propriété **IPropertyStore** correspondant et la plupart des GUID ont une chaîne de nom **IPropertyBag** correspondante, à quelques exceptions près.

Cette documentation répertorie les propriétés par constante de clé de propriété, mais chaque entrée comprend la constante de chaîne de nom de propriété pour une utilisation avec **IPropertyBag** , le cas échéant.

## <a name="related-topics"></a>Rubriques connexes

[Codecs Windows Media](windows-media-codecs.md)
