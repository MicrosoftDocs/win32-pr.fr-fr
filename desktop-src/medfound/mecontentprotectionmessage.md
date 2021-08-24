---
description: Déclenché par un composant de pipeline lorsque la configuration change pour l’un des schémas de protection de sortie. Cet événement s’applique uniquement au contenu protégé.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Événement MEContentProtectionMessage (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0316767025fe4446909146b92cfcea8abcc3e0511990c19485a50c94dbc3fa59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013829"
---
# <a name="mecontentprotectionmessage-event"></a>Événement MEContentProtectionMessage

Déclenché par un composant de pipeline lorsque la configuration change pour l’un des schémas de protection de sortie. Cet événement s’applique uniquement au contenu protégé.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

Toutes les sorties approuvées doivent gérer cet événement. Les transformations de Media Foundation (MFTs) reçoivent cet événement via la méthode [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) . Les récepteurs multimédias reçoivent cet événement par le biais de la méthode [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .

La sortie approuvée doit appliquer les modifications de stratégie ou retourner le code d’erreur MF \_ E \_ stratégie \_ non prise en charge.

Les données d’événement et les attributs dépendent du système de protection du contenu en cours d’utilisation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




