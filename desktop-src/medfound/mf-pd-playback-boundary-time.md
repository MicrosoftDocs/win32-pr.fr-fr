---
description: Stocke l’heure (en unités de 100 nanosecondes) à laquelle la présentation doit commencer, par rapport au début de la source du média.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: Attribut MF_PD_PLAYBACK_BOUNDARY_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042748"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a>\_ \_ \_ Attribut heure limite de lecture MF PD \_

Stocke l’heure (en unités de 100 nanosecondes) à laquelle la présentation doit commencer, par rapport au début de la source du média.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>S’applique à

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Notes

L' \_ \_ attribut heure limite de lecture MF PD \_ \_ est facultatif pour les sources multimédias dans une sélection. Cette valeur indique l’heure de début réelle de la présentation. Prenons l’exemple d’une sélection qui comprend les sources multimédias *element1*, *élément2* et *Element3* dans une séquence. 15 secondes après le début de la diffusion de *element1* , une modification dynamique du flux se produit. Le nouveau flux doit commencer à lire 15 secondes dans la présentation. Toutefois, l’image clé la plus proche de l’heure de présentation de 15 secondes est de 12 secondes pour le nouveau flux. Pour démarrer la nouvelle présentation à 15 secondes, une marque est nécessaire pour que les échantillons décodés soient déposés de 12 secondes à 15 secondes.

Avant la transition, l’événement [MENewPresentation](menewpresentation.md) est déclenché par la source du média. Cela retourne le descripteur de présentation qui contient l’attribut d' [ID d’élément de \_ \_ lecture \_ \_ MF PD](mf-pd-playback-element-id.md) pour *element1*. En outre, il contient l' \_ attribut de \_ temps limite de lecture MF PD \_ \_ défini à 15 secondes pour indiquer l’heure à laquelle la transition s’est produite. La source du média effectue la marque à 15 secondes après le décodage, ce qui empêche l’affichage des images de 12 secondes à 15 secondes.

Cette valeur affecte uniquement l’heure de la marque et n’affecte pas la manière dont la session multimédia ajuste les horodatages. Cet attribut est ignoré, sauf si la source du média indique par le biais de l’attribut d' [ \_ ID d’élément de \_ lecture \_ \_ MF PD](mf-pd-playback-element-id.md) que cette présentation est le même élément de lecture que le précédent.

L' \_ attribut de \_ durée limite de lecture MF PD \_ \_ est semblable à l’attribut [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) défini sur le nœud de topologie. Pour les applications qui s’exécutent sur Windows Vista, les sources multimédias qui implémentent [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) doivent utiliser **MF \_ TOPONODE \_ MEDIASTART** au lieu du \_ \_ temps limite de lecture MF PD \_ \_ .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




