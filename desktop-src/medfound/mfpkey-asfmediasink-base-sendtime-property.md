---
description: Temps d’envoi de base pour le récepteur de média ASF, en millisecondes.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: MFPKEY_ASFMEDIASINK_BASE_SENDTIME, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414103"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a>MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME, propriété

Temps d’envoi de base pour le récepteur de média ASF, en millisecondes.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Notes

L’heure d’envoi est l’heure à laquelle un paquet ASF est envoyé sur le réseau. Il ne correspond pas directement à l’heure de présentation des données dans le paquet.

Vous pouvez utiliser cette propriété pour configurer le récepteur multimédia ASF. L’utilisation dépend de la fonction que vous appelez pour créer le récepteur multimédia ASF :

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): interroge le pointeur [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) récupéré pour l’interface **IPropertyStore** .

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sur le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) spécifié dans le paramètre *pContentInfo* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




