---
description: Redimensionne un flux vidéo.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Dimensionnement vidéo DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519578"
---
# <a name="video-resizer-dsp"></a>Dimensionnement vidéo DSP

Redimensionne un flux vidéo.

## <a name="clsid"></a>CLSID

CLSID \_ CResizerDMO

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResizerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a>Formats

Le redimensionnement vidéo DSP prend en charge les sous-types de médias d’entrée/sortie suivants lorsqu’il agit comme un objet de média DirectX (DMO).

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ AYUV
-   MEDIASUBTYPE \_ V216
-   MEDIASUBTYPE \_ YV12

Le redimensionnement vidéo DSP prend en charge les sous-types de médias d’entrée/sortie suivants lorsqu’il joue le rôle d’une transformation de Media Foundation (MFT).

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ Rgb24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ AYUV
-   MFVideoFormat \_ V216
-   MFVideoFormat \_ YV12

## <a name="properties"></a>Propriétés

-   [MFPKEY \_ REdimensionner \_ SRC à \_ gauche](mfpkey-resize-src-left.md)
-   [MFPKEY \_ REdimensionner \_ SRC en \_ haut](mfpkey-resize-src-top.md)
-   [MFPKEY \_ REdimensionner la \_ \_ largeur SRC](mfpkey-resize-src-width.md)
-   [MFPKEY \_ REdimensionner la \_ \_ hauteur SRC](mfpkey-resize-src-height.md)
-   [MFPKEY \_ REdimensionner l' \_ heure d’été à \_ gauche](mfpkey-resize-dst-left.md)
-   [MFPKEY \_ REdimensionner l' \_ heure d’été en \_ haut](mfpkey-resize-dst-top.md)
-   [largeur de l' \_ heure d’été de REdimensionnement MFPKEY \_ \_](mfpkey-resize-dst-width.md)
-   [\_hauteur MFPKEY REdimensionner l' \_ heure d’été \_](mfpkey-resize-dst-height.md)
-   [\_qualité de REdimensionnement MFPKEY \_](mfpkey-resize-quality.md)
-   [\_entrelacement de REdimensionnement MFPKEY \_](mfpkey-resize-interlace.md)
-   [MFPKEY \_ REdimensionner \_ GEOMAPX](mfpkey-resize-geomapx.md)
-   [MFPKEY \_ REdimensionner \_ GEOMAPY](mfpkey-resize-geomapy.md)
-   [MFPKEY \_ REdimensionner \_ GEOMAPWIDTH](mfpkey-resize-geomapwidth.md)
-   [MFPKEY \_ REdimensionner \_ GEOMAPHEIGHT](mfpkey-resize-geomapheight.md)
-   [MFPKEY \_ REdimensionner \_ MINAPX](mfpkey-resize-minapx.md)
-   [MFPKEY \_ REdimensionner \_ MINAPY](mfpkey-resize-minapy.md)
-   [MFPKEY \_ REdimensionner \_ MINAPWIDTH](mfpkey-resize-minapwidth.md)
-   [MFPKEY \_ REdimensionner \_ MINAPHEIGHT](mfpkey-resize-minapheight.md)
-   [MFPKEY \_ REdimensionner \_ PANSCANAPX](mfpkey-resize-panscanapx.md)
-   [MFPKEY \_ REdimensionner \_ PANSCANAPY](mfpkey-resize-panscanapy.md)
-   [MFPKEY \_ REdimensionner \_ PANSCANAPWIDTH](mfpkey-resize-panscanapwidth.md)
-   [MFPKEY \_ REdimensionner \_ PANSCANAPHEIGHT](mfpkey-resize-panscanapheight.md)
-   [MFPKEY \_ PIXELASPECTRATIO](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a>Notes

Le rôle d’application vidéo redimensionnement DSP est implémenté en tant qu’objet COM pouvant agir comme DMO ou MFT. L’objet a un identificateur de classe unique (CLSID), qu’il agisse comme DMO ou MFT. Pour plus d’informations sur le moment où un DSP agit comme DMO ou MFT, consultez [processeurs de signal numérique](windowsmediadigitalsignalprocessors.md).

Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un DSP fait office de modèle DMO ou MFT. Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un DSP agisse comme DMO ou MFT. Pour plus d’informations sur les GUID qui représentent des sous-types de médias, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).

Ce DSP peut effectuer des opérations de rognage et de mise à l’échelle sur l’image vidéo. Le format du type de sortie doit correspondre au format du type d’entrée. Le DSP n’effectue pas de conversions de l’espace colorimétrique.

Avant de définir le type de sortie, vous pouvez définir l’une des régions suivantes à l’aide des propriétés listées dans ce tableau.



| Région                   | Propriétés                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rectangle source         | MFPKEY \_ REdimensionner \_ SRC à \_ gauche<br/> MFPKEY \_ REdimensionner \_ SRC en \_ haut<br/> MFPKEY \_ REdimensionner la \_ \_ largeur SRC<br/> MFPKEY \_ REdimensionner la \_ \_ hauteur SRC<br/>            |
| Rectangle de destination    | MFPKEY \_ REdimensionner l' \_ heure d’été à \_ gauche<br/> MFPKEY \_ REdimensionner l' \_ heure d’été en \_ haut<br/> largeur de l' \_ heure d’été de REdimensionnement MFPKEY \_ \_<br/> \_hauteur MFPKEY REdimensionner l' \_ heure d’été \_<br/>            |
| Ouverture géométrique       | MFPKEY \_ REdimensionner \_ GEOMAPX<br/> MFPKEY \_ REdimensionner \_ GEOMAPY<br/> MFPKEY \_ REdimensionner \_ GEOMAPWIDTH<br/> MFPKEY \_ REdimensionner \_ GEOMAPHEIGHT<br/>             |
| Ouverture minimale de l’affichage | MFPKEY \_ REdimensionner \_ MINAPX<br/> MFPKEY \_ REdimensionner \_ MINAPY<br/> MFPKEY \_ REdimensionner \_ MINAPWIDTH<br/> MFPKEY \_ REdimensionner \_ MINAPHEIGHT<br/>                 |
| Région Pan/Scan          | MFPKEY \_ REdimensionner \_ PANSCANAPX<br/> MFPKEY \_ REdimensionner \_ PANSCANAPY<br/> MFPKEY \_ REdimensionner \_ PANSCANAPWIDTH<br/> MFPKEY \_ REdimensionner \_ PANSCANAPHEIGHT<br/> |



 

Dans chaque cas, vous devez définir toutes les propriétés associées pour que le paramètre prenne effet.

Le DSP copie la partie de l’image source définie par le rectangle source et l’étire ou le compresse sur le rectangle de destination de la mémoire tampon de sortie. Les rectangles source et de destination n’ont pas besoin d’être de la même taille. La taille de trame dans le type de média de sortie doit être suffisamment grande pour contenir le rectangle de destination.

L’ouverture géométrique, la zone d’affichage minimale et la région de panoramique/numérisation n’affectent pas la manière dont le DSP redimensionne la vidéo. Toutefois, ils peuvent affecter la façon dont le composant en aval interprète la trame vidéo. En particulier, le convertisseur vidéo amélioré (EVR) utilise ces valeurs lorsqu’il calcule les proportions de l’image et la zone d’affichage.

Si vous utilisez Media Foundation types de média, vous pouvez définir l’ouverture géométrique, l’ouverture minimale d’affichage et les régions Pan/Scan directement dans le type de média de sortie. Dans le cas contraire, si vous utilisez des types de média DMO, définissez-les à l’aide des propriétés.

Pour plus d'informations, voir les rubriques suivantes :

-   [**\_ \_ ouverture géométrique MF \_ MF**](mf-mt-geometric-aperture-attribute.md)
-   [**\_ouverture de \_ l' \_ affichage \_ de la version MF**](mf-mt-minimum-display-aperture-attribute.md)
-   [**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vidreszr.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Processeurs de signaux numériques](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
