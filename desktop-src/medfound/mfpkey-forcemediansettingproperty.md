---
description: Spécifie si le codec doit utiliser le filtrage médian pendant l’encodage.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: MFPKEY_FORCEMEDIANSETTING, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722fca2f73f2114cf17664f228e00a12f46e5a399f54b8dc6990940f5c18d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953949"
---
# <a name="mfpkey_forcemediansetting-property"></a>MFPKEY \_ propriété FORCEMEDIANSETTING

Spécifie si le codec doit utiliser le filtrage médian pendant l’encodage.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCForceMedianSetting g

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

FALSE

## <a name="remarks"></a>Remarques

Le filtrage médian indique au codec d’ignorer le bruit et le grain lors du calcul du mouvement entre les frames. Cela peut améliorer la qualité de la vidéo très bruyante, mais peut entraîner des traces de mouvement (également appelées « artefacts de fin ») lorsqu’elle est appliquée à une vidéo source propre.

Par défaut, le codec utilise une logique interne pour déterminer si le filtrage médian doit être utilisé. Si vous définissez cette propriété, cette logique sera remplacée.

> [!Note]  
> Ce filtre n’est pas le même que les filtres de flou médian trouvés dans de nombreuses applications d’édition vidéo et de traitement.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




