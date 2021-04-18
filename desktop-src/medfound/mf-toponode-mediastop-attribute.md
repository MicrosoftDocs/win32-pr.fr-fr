---
description: Spécifie l’heure d’arrêt de la présentation.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: Attribut MF_TOPONODE_MEDIASTOP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5b763d1d5adabc520900dde6839d1599ddcb3d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106543007"
---
# <a name="mf_toponode_mediastop-attribute"></a>\_ \_ Attribut MEDIASTOP TOPONODE MF

Spécifie l’heure d’arrêt de la présentation.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>S’applique à

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Notes

Cet attribut spécifie la position dans la source où la lecture s’arrête, en unités de 100 nanosecondes, par rapport au démarrage de la source. Si l’attribut n’est pas défini, la lecture s’arrête à la fin de la source. Par exemple, pour arrêter la lecture à la marque de 5 secondes, définissez cet attribut sur 50 millions. Définissez l’attribut sur les nœuds sources dans la topologie (nœuds avec le type égal à **\_ nœud de topologie MF \_ \_ SOURCESTREAM**). Définissez l’attribut avant d’appeler [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Si vous insérez manuellement un décodeur dans la topologie, vous devez également définir les attributs [MF \_ TOPONODE \_ Mark \_ ici](mf-toponode-markin-here-attribute.md) et [MF \_ TOPONODE \_ MARKOUT \_ ici](mf-toponode-markout-here-attribute.md) sur le nœud décodeur.

 

Une fois la topologie définie, la définition de cet attribut n’a aucun effet.

Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**. Toutefois, les valeurs négatives ne sont pas significatives.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Durée des présentations de séquence](sequence-presentation-times.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> <dt>

[**\_MEDIASTART TOPONODE \_ MF**](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




