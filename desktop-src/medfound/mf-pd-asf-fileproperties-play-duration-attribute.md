---
description: Spécifie le temps nécessaire pour lire un fichier ASF (Advanced Systems Format), en unités de 100 nanosecondes.
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: Attribut MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0e4609f70fa96a0e08339e496b1d7ed6ac7004108ec56ff870ed6f4e7fcb6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104345"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a>\_Attribut de \_ \_ durée de \_ lecture \_ MF PD ASF

Spécifie le temps nécessaire pour lire un fichier ASF (Advanced Systems Format), en unités de 100 nanosecondes.

Cette valeur comprend le temps de préroll. Pour récupérer la durée de lecture réelle, récupérez la valeur de l’attribut de [**\_ \_ durée MF PD**](mf-pd-duration-attribute.md) . Toutefois, si la valeur du préroll est supérieure à la durée de lecture, la valeur de la **\_ \_ durée MF** est égale à zéro.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.

## <a name="examples"></a>Exemples


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> <dt>

[Descripteurs de présentation](presentation-descriptors.md)
</dt> </dl>

 

 




