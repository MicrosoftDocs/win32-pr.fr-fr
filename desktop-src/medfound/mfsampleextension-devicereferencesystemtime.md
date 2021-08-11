---
description: Spécifie l’horodateur de l’appareil d’origine sur l’exemple.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: Attribut MFSampleExtension_DeviceReferenceSystemTime (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0458c1a2b0f5b204483cba0e6f571a2a5ace34b7b39463cc20ded664eecaaa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241134"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>\_Attribut MFSampleExtension DeviceReferenceSystemTime

Spécifie l’horodateur de l’appareil d’origine sur l’exemple.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Notes

Il s’agit de l’horodatage de référence d’appareil des échantillons de média dans la résolution de 100 ns. Cet horodatage peut ou non contenir la valeur réelle du compteur de performance des requêtes (QPC), en fonction de la source qui produit les exemples. Cette valeur peut être modifiée par d’autres composants dans le pipeline de média. Cette valeur n’est pas disponible pour les MFTs insérés dans le pipeline de capture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




