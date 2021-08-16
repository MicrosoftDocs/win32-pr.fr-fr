---
title: BufferAverage
description: L’attribut BufferAverage contient la taille moyenne de la mémoire tampon nécessaire pour un flux de vitesse de transmission variable (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- Format Windows Media BufferAverage
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd839bff96f5ba327e585f8608bd4612fc047d354c24fee972e507ea5ca681f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656119"
---
# <a name="bufferaverage"></a>BufferAverage

L’attribut **BufferAverage** contient la taille moyenne de la mémoire tampon nécessaire pour un flux de vitesse de transmission variable (VBR).

## <a name="global-constant"></a>Constante globale

\_wszBufferAverage g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Remarques

Lors de l’accès à l’interface **IWMHeaderInfo3** de l’objet Writer, vous pouvez ajouter ou modifier cette valeur. Dans d’autres objets (éditeur de métadonnées, lecteur et lecteur synchrone), cette valeur est en lecture seule.

Le writer écrit automatiquement une valeur **BufferAverage** pour chaque flux VBR.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




