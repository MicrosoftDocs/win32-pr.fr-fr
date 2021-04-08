---
description: Configure la source de média ASF pour utiliser la recherche itérative si le fichier source n’a pas d’index.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761449"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex, propriété

Configure la source de média ASF pour utiliser la recherche itérative si le fichier source n’a pas d’index.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**VARIANT \_ booléen**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Notes

Utilisez cette propriété pour configurer la source de média ASF. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de *résolution source*. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

La *recherche itérative* est un algorithme permettant de trouver une position dans un fichier ASF sans index. Elle utilise une série de approximations, en fonction de la vitesse de transmission moyenne, pour se rapprocher progressivement du temps de recherche cible. (L’algorithme est similaire à une recherche binaire.) La recherche itérative peut prendre plus de temps que la recherche par index. elle est donc désactivée par défaut.

Si vous définissez cette propriété, utilisez les propriétés suivantes pour définir les paramètres de recherche :

-   [Nombre maximal de MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [MFPKEY \_ ASFMediaSource \_ IterativeSeek la \_ tolérance \_ en \_ millisecondes](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

Ces propriétés définissent respectivement le nombre maximal d’itérations et la tolérance. L’algorithme s’arrête lorsqu’il atteint le nombre maximal d’itérations, ou lorsqu’il trouve un paquet dont la distance par rapport à l’heure de recherche est comprise dans la tolérance spécifiée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




