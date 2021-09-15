---
description: Spécifie la fréquence d’actualisation du moniteur.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: Attribut MF_TOPOLOGY_PLAYBACK_FRAMERATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296307"
---
# <a name="mf_topology_playback_framerate-attribute"></a>\_ \_ Attribut de fréquence de lecture de la topologie MF \_

Spécifie la fréquence d’actualisation du moniteur.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Pour définir cet attribut, appelez [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="applies-to"></a>S’applique à

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Notes

Le chargeur de topologie utilise cet attribut pour optimiser le pipeline avant le démarrage de la lecture. Si vous définissez cet attribut, affectez également à l’attribut [ \_ \_ \_ \_ optimisations de la lecture statique de la topologie MF](mf-topology-static-playback-optimizations.md) la **valeur true**.

La fréquence d’images est exprimée sous la forme d’un rapport. Les 32 bits supérieurs de la valeur d’attribut contiennent le numérateur, et les 32 de bits inférieurs contiennent le dénominateur.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> <dt>

[Gestion de la qualité vidéo](video-quality-management.md)
</dt> </dl>

 

 




