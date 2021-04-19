---
description: La \_ \_ structure Stride transport MPEG2 décrit le format des paquets de flux de transport MPEG-2 (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: Structure MPEG2_TRANSPORT_STRIDE (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537379"
---
# <a name="mpeg2_transport_stride-structure"></a>\_Structure Stride de transport MPEG2 \_

La `MPEG2_TRANSPORT_STRIDE` structure décrit le format des paquets de flux de transport MPEG-2 (TS). Cette structure autorise les flux de transport dans lesquels les paquets de transport de 188 octets ne sont pas contigus. Dans le cadre de cette documentation, ces paquets sont appelés *paquets Stride*.

Les paquets Stride sont identifiés par le type de média suivant :



|             |                                        |
|-------------|----------------------------------------|
| Type principal  | Flux de MEDIATYPE \_                      |
| Subtype     | \_Stride de \_ transport MEDIASUBTYPE MPEG2 \_ |
| Type de format | FORMAT \_ aucun                           |



 

Le bloc de format (**pbFormat**) est facultatif. Si le bloc de format est inclus, il doit commencer par une structure **\_ \_ Stride de transport MPEG2** . Cette structure définit la disposition du paquet de transport dans le paquet Stride. Si le bloc de format est **null**, les paquets sont supposés utiliser un ensemble de valeurs par défaut ; Pour plus d’informations, consultez la section Notes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwOffset**
</dt> <dd>

Spécifie l’offset, en octets, entre le début du paquet et le premier octet du paquet de transport incorporé. La valeur doit être comprise entre zéro et `(dwStride - dwPacketLength)` , inclus.

</dd> <dt>

**dwPacketLength**
</dt> <dd>

Spécifie la longueur, en octets, du paquet de transport incorporé. Pour les paquets de transport MPEG-2 standard, la valeur doit être de 188 octets.

</dd> <dt>

**dwStride**
</dt> <dd>

Spécifie la longueur de l’ensemble du paquet Stride, en octets. La valeur doit être au moins égale à `(dwOffset + dwPacketLength)` .

</dd> </dl>

## <a name="remarks"></a>Notes

Le diagramme suivant illustre les relations entre les membres de structure.

![paquet Stride MPEG-2](images/mpeg2-stride-packet.png)

Les mémoires tampons d’entrée qui contiennent des paquets Stride multiplexés présentent des restrictions :

-   Les paquets Stride doivent être empaquetés de façon contiguë dans la mémoire tampon.
-   Aucun octet ne peut précéder le premier paquet Stride ou suivre le dernier paquet Stride.
-   Un nombre entier de paquets Stride doit tenir dans la mémoire tampon ; autrement dit, la longueur de la mémoire tampon% dwStride est égale à zéro.

Il n’existe aucune restriction sur le nombre de paquets Stride par mémoire tampon.

Si le type de média ne contient pas de bloc de format (**pbFormat** a la **valeur null**), les valeurs par défaut suivantes sont utilisées :

-   **dwOffset**: 0
-   **dwPacketLength**: 188
-   **dwStride**: 188

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Bdatypes. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures DirectShow](directshow-structures.md)
</dt> <dt>

[Types de média MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




