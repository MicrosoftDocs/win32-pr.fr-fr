---
description: spécifie la manière dont le récepteur de média ASF doit s’appliquer Windows media DRM.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: MFPKEY_ASFMEDIASINK_DRMACTION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313821"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>MFPKEY \_ ASFMEDIASINK \_ DRMACTION, propriété

spécifie la manière dont le récepteur de média ASF doit s’appliquer Windows media DRM.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Notes

La valeur de cette propriété est un membre de l’énumération [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .

Vous pouvez utiliser cet attribut pour configurer le récepteur multimédia ASF. L’utilisation dépend de la fonction que vous appelez pour créer le récepteur multimédia ASF :

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

 

 
