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
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100988"
---
# <a name="bufferaverage"></a>BufferAverage

L’attribut **BufferAverage** contient la taille moyenne de la mémoire tampon nécessaire pour un flux de vitesse de transmission variable (VBR).

## <a name="global-constant"></a>Constante globale

\_wszBufferAverage g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Lors de l’accès à l’interface **IWMHeaderInfo3** de l’objet Writer, vous pouvez ajouter ou modifier cette valeur. Dans d’autres objets (éditeur de métadonnées, lecteur et lecteur synchrone), cette valeur est en lecture seule.

Le writer écrit automatiquement une valeur **BufferAverage** pour chaque flux VBR.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




