---
description: Transformations de prétraitement du décodeur MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Transformations de prétraitement du décodeur MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70df51b26ec3fa25d67a03a4e494869a2f25760
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747053"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a>Transformations de prétraitement du décodeur MPEG

**Bandes et PanScan**

L’image 4x3 peut être formée en remplissant le haut et le bas de l’image (appelée « image de la zone de bandes »), soit en extrayant une partie 4x3 de l’image (appelée image PanScan). Les flux des menus et des sous-images sont superposés au-dessus de l’image vidéo finale. Les images de rapport 16 x 9 sont stockées dans un format anamorphique 4x3. L’étirement de la vidéo source 720 x 480 de l’aspect 4x3 anamorphique en un proportions 16 x 9 forme l’image de l’aspect 16 x 9 d’origine.

Vous trouverez ci-dessous une description de l’affichage correct de chacun des modes et de leurs points de vue :

-   **Panoramique :** Vidéo source étirée dans la plus grande zone 16 x 9 de la fenêtre sortie. Les surbrillances sont relatives à l’intérieur de la zone 16 x 9. Les barres noires doivent être ajoutées à la partie supérieure et inférieure, ou aux côtés pour maintenir une zone 16 x 9.
-   **Analyse panoramique :** À partir de la vidéo 16 x 9, utilisez le décalage horizontal fourni dans le flux MPEG2 pour extraire une sous-fenêtre 4x3. Placez la sous-fenêtre 4x3 dans la zone 4x3 la plus grande de la fenêtre cliente de sortie. Les coordonnées de la surbrillance sont relatives à la fenêtre de sortie 4x3 et n’ont aucune relation avec la vidéo 16 x 9 source. Les barres noires doivent être ajoutées à la partie supérieure et inférieure, ou aux côtés pour maintenir une zone 4x3.
-   **Bandes de bandes :** Calculez la plus grande zone 4x3 de la fenêtre sortie. Les barres noires doivent être ajoutées à la partie supérieure et inférieure, ou aux côtés pour maintenir une zone 4x3. La vidéo 4x3 anamorphique source (représentant une image 16 x 9) est placée dans la plus grande sous-fenêtre 16 x 9 à l’intérieur de la zone 4x3. Des barres noires doivent être ajoutées en haut et en bas de la sous-fenêtre pour tenir à jour une zone 16 x 9. Les coordonnées de la surbrillance sont relatives à la zone 4x3 et n’ont aucune relation avec la vidéo 16 x 9 source. Un disque peut spécifier une mise en surbrillance qui se trouve en dehors de la zone 16 x 9 (mais toujours dans la fenêtre 4x3). Pour 4x3 vidéo, la vidéo est placée dans la zone de sortie 4x3 la plus grande de la fenêtre cliente de sortie. Les barres noires doivent être ajoutées à la partie supérieure et inférieure, ou aux côtés pour maintenir une zone 4x3.

**Prétraitement MPEG avec le navigateur DVD et VMR**

Actuellement, le décodeur reçoit un type de \_ média vidéo MPEG2 de format \_ (dont le bloc de format pointe vers une structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ). Sur les broches de sortie, le décodeur produit un \_ type de média VIDEOINFO2 format, dont le bloc de format pointe vers une structure [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Le champ **dwReserved** de la structure a été renommé en indicateurs **dwControls** .

Le membre **dwControlFlags** contient maintenant les nouveaux bits.



|                          |            |
|--------------------------|------------|
| AMCONTROL \_ utilisé          | 0x00000001 |
| AMCONTROL \_ \_ à \_ 4x3  | 0x00000002 |
| AMCONTROL \_ \_ à \_ 16 x 9 | 0x00000004 |



 

AMCONTROL \_ utilisé est utilisé pour tester si ces nouveaux indicateurs sont pris en charge. Un filtre source doit définir l' \_ indicateur AMCONTROL utilisé et voir si QueryAccept (MediaType) parvient au code pin en aval. Si elle est rejetée, les indicateurs AMCONTROL ne peuvent pas être utilisés et dwReserved1 doit avoir la valeur 0.

AMCONTROL \_ Pad \_ à \_ 4x3 indique que l’image doit être remplie et affichée dans une zone de 4x3.

AMCONTROL \_ Pad \_ à \_ 16 x 9 indique que l’image doit être remplie et affichée dans une zone de 16 x 9.

Le décodeur doit soit copier, soit traiter en aveugle les bits. Si le décodeur exécute cadre lui-même, il doit modifier les proportions de pixels, remplir l’image et supprimer les bits AMCONTROL correspondants \_ \* .

MPEG2VIDEOINFO. dwFlags contient désormais trois indicateurs pour contrôler le mode d’affichage du contenu :

-   `AMMPEG2_DoPanScan (0x00000001)`: Si cet indicateur est défini, le décodeur vidéo MPEG-2 doit rogner l’image de sortie en fonction de vecteurs d’analyse panoramique dans l’extension d’affichage des images \_ \_ et modifier les proportions de l’image en 4x3. VMR ne doit pas recevoir un exemple 16 x 9 avec cet indicateur. Une implémentation simple peut modifier le rectangle source pour indiquer une région source largeur 540 avec un bord gauche égal au décalage d’affichage dans l’extension d’affichage de l’image \_ \_ .
-   `AMMPEG2_LetterboxAnalogOut (0x00000020)`: Lorsqu’un décodeur matériel affiche ce flux dans une sortie vidéo (généralement un connecteur SVIDEO sur la carte), il doit appliquer les règles d’affichage d’un exemple 16 x 9 sur un 4x3 Display.

    Un décodeur logiciel (ou un décodeur matériel produisant une sortie envoyée à VMR) a deux options lors du traitement des images :

    1.  Ignorez cet indicateur et passez le contenu VideoInfoHeader2 à VMR (l' \_ indicateur AMCONTROL Pad \_ to \_ 4x3 sera déjà défini par le [navigateur DVD](dvd-navigator-filter.md) sur l’exemple). VMR rencontre un exemple de vidéo 16 x 9 avec le bloc AMCONTROL \_ \_ pour l' \_ indicateur 4x3 et un flux de sous-image 4x3. L’application doit définir les rectangles de destination normalisés de sortie des deux flux pour qu’ils aient la même largeur.
    2.  Convertissez le flux anamorphique en image 4x3 en complétant le haut et le bas de l’image et en définissant les proportions de l’image sur 4x3 (voir la zone de la zone de rapport au-dessus), puis en supprimant le \_ bloc AMCONTROL \_ à \_ 4X3 bit du VIDEOINFOHEADER2.

    Les décodeurs DirectXVA qui mélangent les flux vidéo et sous-image doivent traiter cet indicateur. Si le matériel ne peut pas mettre à l’échelle la sous-image fusionnée, le décodeur doit produire un flux de sous-image séparé pour VMR à mélanger avec la vidéo.

-   `AMMPEG2_WidescreenAnalogOut (0x00000200)`: Lorsqu’un décodeur matériel affiche ce flux dans une sortie vidéo (généralement un connecteur SVIDEO sur la carte), il doit supposer un affichage 16 x 9 (anamorphique).

    Un décodeur logiciel (ou un décodeur matériel produisant une sortie envoyée à VMR) a deux options lors du traitement d’une image anamorphique :

    1.  Ignorez cet indicateur et copiez le contenu VideoInfoHeader2 dans VMR. VMR remplira les images 4x3 à 16 x 9 s’ils disposent du \_ Pad AMCONTROL \_ pour \_ 16 x 9 défini.
    2.  Remplissez l’image de sortie sur une image 16 x 9 et supprimez le \_ bloc AMCONTROL \_ pour \_ 16 x 9 bit.

La plupart des décodeurs doivent utiliser **GetMediaType** pour détecter une modification de média sur la broche d’entrée et copier le contenu de **VIDEOINFOHEADER2** (contenu dans **MPEG2INFOHEADER**) sur la broche de sortie. Ils ne traiteront probablement que le bit PanScan.

L’exemple de code suivant montre comment copier le contenu **VIDEOINFOHEADER2** d’une broche d’entrée vers une broche de sortie.


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



