---
description: Spécifie l’heure de début de la présentation.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: Attribut MF_TOPONODE_MEDIASTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7efeed2bd34745ffda4e756c8b43894bd51fc287ded5cba0ecf0ffb323713754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244420"
---
# <a name="mf_toponode_mediastart-attribute"></a>\_ \_ Attribut MEDIASTART TOPONODE MF

Spécifie l’heure de début de la présentation.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>S’applique à

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Notes

Cet attribut spécifie la position dans la source où la lecture commence, en unités de 100 nanosecondes, par rapport au démarrage de la source. Si l’attribut n’est pas défini, la lecture commence à zéro (le début du fichier). Par exemple, pour démarrer la lecture à la marque de 5 secondes, définissez cet attribut sur 50 millions. Définissez l’attribut sur les nœuds sources dans la topologie (nœuds avec le type égal à **\_ nœud de topologie MF \_ \_ SOURCESTREAM**). Définissez l’attribut avant d’appeler [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Si vous insérez manuellement un décodeur dans la topologie, vous devez également définir les attributs [MF \_ TOPONODE \_ Mark \_ ici](mf-toponode-markin-here-attribute.md) et [MF \_ TOPONODE \_ MARKOUT \_ ici](mf-toponode-markout-here-attribute.md) sur le nœud décodeur.

 

Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**. Toutefois, les valeurs négatives ne sont pas significatives.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Durée des présentations de séquence](sequence-presentation-times.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> <dt>

[**\_MEDIASTOP TOPONODE \_ MF**](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




