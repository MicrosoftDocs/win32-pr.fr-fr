---
description: Définit l’ouverture géométrique d’un type de média vidéo.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: Attribut MF_MT_GEOMETRIC_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951534"
---
# <a name="mf_mt_geometric_aperture-attribute"></a>\_Attribut d' \_ ouverture géométrique MF MT \_

Définit l’ouverture géométrique d’un type de média vidéo.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

La valeur de cet attribut est une structure [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Les proportions de l’image sont calculées par rapport à l’ouverture géométrique, à l’aide de la formule suivante : proportions de l’image = (largeur d’ouverture géométrique/hauteur d’ouverture géométrique) × proportions de pixels.

Si cet attribut n’est pas défini, l’ouverture géométrique est supposée être la totalité de l’image vidéo. Vous devez définir cet attribut uniquement lorsque le type de média décrit une norme vidéo avec une zone active définie.

Par exemple, dans la télévision NTSC, le cadre vidéo est 720 × 480 avec une zone active de 704 × 480 et un rapport hauteur/largeur des pixels de 10:11. L’image résultante a un rapport hauteur/largeur de (704/480) × (10/11) = 4:3.

> [!Note]  
> Le présentateur par défaut pour le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR) affiche l’ouverture géométrique de la vidéo, si elle est spécifiée.

 

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="examples"></a>Exemples


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Rapport hauteur/largeur des images](picture-aspect-ratio.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_ouverture de \_ l' \_ affichage \_ de la version MF**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




