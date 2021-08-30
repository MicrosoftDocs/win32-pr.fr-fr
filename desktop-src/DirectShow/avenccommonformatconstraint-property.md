---
description: Spécifie le format cible pour un encodeur.
ms.assetid: 3d316561-352f-44f9-9978-01301a68e7b6
title: Propriété AVEncCommonFormatConstraint (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2108255ca6f42596fe707c66b02e0e4dd38baa5b0f788073adff8cdb4677dd16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108680"
---
# <a name="avenccommonformatconstraint-property"></a>Propriété AVEncCommonFormatConstraint

Spécifie le format cible pour un encodeur.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonFormatConstraint**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un **BSTR** qui contient la représentation sous forme de chaîne d’un GUID. Les GUID suivants sont définis.



| GUID                                         | Description                     |
|----------------------------------------------|---------------------------------|
| \_GUID CODECAPI \_ AVEncCommonFormatATSC        | Télévision par câble ATSC.          |
| \_GUID CODECAPI \_ AVEncCommonFormatDVB         | Télévision par câble DVB.           |
| \_GUID CODECAPI \_ AVEncCommonFormatDVD \_ DashVR | DVD-VR                          |
| \_GUID CODECAPI \_ AVEncCommonFormatDVD \_ PlusVR | DVD + VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V      | DVD-Video                       |
| \_GUID CODECAPI \_ AVEncCommonFormatHighMAT     | HighMAT                         |
| \_GUID CODECAPI \_ AVEncCommonFormatHighMPV     | Non documenté dans cette version. |
| \_GUID CODECAPI \_ AVEncCommonFormatMP3         | MPEG Audio Layer-3 (MP3)        |
| \_GUID CODECAPI \_ AVEncCommonFormatSVCD        | CD Super Video (SVCD)           |
| \_GUID CODECAPI \_ AVEncCommonFormatUnSpecified | Format non spécifié.             |
| \_GUID CODECAPI \_ AVEncCommonFormatVCD         | CD vidéo (VCD)                  |



 

## <a name="remarks"></a>Remarques

Les applications peuvent définir cette propriété pour spécifier le format cible. Les encodeurs peuvent également retourner cette propriété en tant que fonctionnalité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




