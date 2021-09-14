---
description: Spécifie si le récepteur multimédia ASF ajuste automatiquement la vitesse de transmission.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414104"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a>\_Propriété MFPKEY ASFMEDIASINK de vitesse de \_ \_ transmission

Spécifie si le récepteur multimédia ASF ajuste automatiquement la vitesse de transmission.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**VARIANT \_ booléen**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Notes

Si la valeur de cette propriété est \_ true, le récepteur multimédia ASF ajuste automatiquement la vitesse de transmission du contenu ASF en réponse aux caractéristiques des flux multiplexés.

Cette propriété affecte la façon dont le récepteur multimédia ASF se comporte lorsqu’un flux dépasse les paramètres « compartiment perdu » du récepteur :



| Valeur              | Comportement                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANTE \_ true**  | Le récepteur multimédia ASF ajuste automatiquement la vitesse de transmission du contenu ASF en réponse aux caractéristiques des flux en cours de multiplexage. |
| **VARIANTE \_ false** | Le récepteur multimédia ASF utilise la valeur de vitesse de transmission de flux fournie par l’application.                                                                |



 

La valeur par défaut **est \_ false**.

Définissez cette propriété lorsque vous configurez le récepteur multimédia ASF. L’utilisation dépend de la fonction que vous appelez pour créer le récepteur multimédia ASF :

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): interroge le pointeur [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) récupéré pour l’interface **IPropertyStore** .

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sur le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) spécifié dans le paramètre *pContentInfo* .

Si vous affectez à cette propriété la \_ valeur variant true, le récepteur multimédia ASF définit l’indicateur de **\_ \_ \_ débit binaire MFASF multiplexer** sur le multiplexeur ASF. Consultez [**IMFASFMultiplexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).

pour plus d’informations sur le concept de compartiment avec fuite, consultez la rubrique « modèle de tampon de compartiment perdu » dans la documentation du kit de développement logiciel (SDK) Windows Media Format.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**\_LEAKYBUCKET1 ASFSTREAMCONFIG \_ MF**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[**\_LEAKYBUCKET2 ASFSTREAMCONFIG \_ MF**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




