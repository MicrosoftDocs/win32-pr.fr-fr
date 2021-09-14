---
description: Spécifie si le codec doit utiliser le filtrage médian pendant l’encodage.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: MFPKEY_FORCEMEDIANSETTING, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231749"
---
# <a name="mfpkey_forcemediansetting-property"></a>MFPKEY \_ propriété FORCEMEDIANSETTING

Spécifie si le codec doit utiliser le filtrage médian pendant l’encodage.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCForceMedianSetting g

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

FALSE

## <a name="remarks"></a>Notes

Le filtrage médian indique au codec d’ignorer le bruit et le grain lors du calcul du mouvement entre les frames. Cela peut améliorer la qualité de la vidéo très bruyante, mais peut entraîner des traces de mouvement (également appelées « artefacts de fin ») lorsqu’elle est appliquée à une vidéo source propre.

Par défaut, le codec utilise une logique interne pour déterminer si le filtrage médian doit être utilisé. Si vous définissez cette propriété, cette logique sera remplacée.

> [!Note]  
> Ce filtre n’est pas le même que les filtres de flou médian trouvés dans de nombreuses applications d’édition vidéo et de traitement.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




