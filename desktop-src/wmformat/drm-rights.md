---
title: DRM_Rights
description: La \_ propriété droits DRM spécifie les droits requis par l’application lors de la prochaine tentative d’ouverture d’un fichier protégé.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- Format Windows Media DRM_Rights
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219540"
---
# <a name="drm_rights"></a>\_Droits DRM

La **propriété \_ droits DRM** spécifie les droits requis par l’application lors de la prochaine tentative d’ouverture d’un fichier protégé.

## <a name="global-constant"></a>Constante globale

\_droits wszWMDRM \_ g

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Il s’agit d’une propriété en lecture-écriture qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) et définie à l’aide de [**IWMDRMReader :: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) ou [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

Le tableau suivant répertorie les droits pris en charge.



| Right                                           | Littéral de chaîne      | Description                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_wszWMDRM la \_ sauvegarde à droite g \_                      | « Backup »            | Droit de sauvegarder la licence.                                                                                                                                                                                        |
| wszWMDRM de la \_ \_ bonne \_ \_ lecture collaborative         | "CollaborativePlay" | Droit de lire le fichier dans le cadre d’une sélection collaborative.                                                                                                                                                          |
| \_wszWMDRM g \_ droit de \_ copie                        | "Copy"              | Droit de copier le fichier sur un appareil. Ce droit remplace les droits de copie plus anciens (g \_ wszWMDRM \_ droit Copy \_ \_ sur \_ CD, g \_ wszWMDRM \_ Right \_ Copy \_ to \_ non \_ SDMI \_ Device et g \_ wszWMDRM \_ Right \_ Copy \_ to \_ SDMI \_ Device). |
| \_wszWMDRM g \_ droit \_ \_ de copie sur le \_ CD                | « Print. Redbook »     | Droit de copier le fichier sur un CD (format de livre rouge). dans Windows DRM Media 10, ce droit est remplacé par g \_ wszWMDRM \_ right \_ COPY.<br/>                                                                             |
| g \_ wszWMDRM \_ droit \_ \_ de copie sur un \_ \_ appareil non SDMI \_ | « Transfer. NONSDMI »  | Droit de copier le fichier sur un appareil non-SDMI. dans Windows DRM Media 10, ce droit est remplacé par g \_ wszWMDRM \_ right \_ COPY.<br/>                                                                                  |
| g \_ wszWMDRM \_ droit \_ \_ de copie sur l' \_ \_ appareil SDMI      | « Transfer. SDMI »     | Droit de copier le fichier sur un appareil compatible SDMI. dans Windows DRM Media 10, ce droit est remplacé par g \_ wszWMDRM \_ right \_ COPY.<br/>                                                                           |
| \_ \_ lecture droite g \_ wszWMDRM                    | Répétition              | Droit de lire le fichier multimédia.                                                                                                                                                                                        |



 

Cette propriété contient une chaîne de caractères larges d’un ou plusieurs droits séparés par des points-virgules, par exemple : L "lecture ; Reprographie CollaborativePlay".

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 





