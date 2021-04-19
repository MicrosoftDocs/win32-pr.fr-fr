---
description: Le filtre d’encodeur vidéo Microsoft MPEG-2 encode MPEG-2 et MPEG-1 Video.
ms.assetid: d52c1299-0641-405c-8960-edd738b56823
title: Encodeur vidéo Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c96db605586c6abf0f51537689a9365df2842c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106543437"
---
# <a name="microsoft-mpeg-2-video-encoder"></a>Encodeur vidéo Microsoft MPEG-2

Le filtre d’encodeur vidéo Microsoft MPEG-2 encode MPEG-2 et MPEG-1 Video.

Pour encoder et multiplexer des flux audio/vidéo, utilisez le filtre d' [**encodeur Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md) , qui encapsule les fonctions de ce filtre et du filtre d' [**encodeur audio Microsoft MPEG-2**](microsoft-mpeg-2-audio-encoder.md) .

> [!Note]  
> Ce filtre n’est pas pris en charge sur les plateformes IA-64.

 



Informations de filtre

Interfaces de filtre

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Types de média de broche d’entrée

**MediaType \_ Vidéo**, **MEDIASUBTYPE \_ I420**<br/> **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ IYUV**<br/> **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ Rgb24**<br/> **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ UYVY**<br/> **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ YUY2**<br/> **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ YV12**<br/>

Interfaces pin d’entrée

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Types de média de broche de sortie

**MediaType \_ Flux**, **\_ \_ vidéo MEDIASUBTYPE MPEG2**<br/> **MediaType \_ Stream**, **\_ \_ programme MEDIASUBTYPE MPEG2**<br/> **MediaType \_ Flux**, **\_ \_ transport MEDIASUBTYPE MPEG2**<br/> **MediaType \_ Vidéo**, **\_ \_ vidéo MEDIASUBTYPE MPEG2**<br/>

Interfaces de broche de sortie

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID du filtre

**CLSID \_ CMPEG2EncoderVideoDS** (déclaré dans wmcodecdsp. h)

Exécutable

msmpeg2enc.dll

[Mérite](merit.md)

**MÉRITE \_ n' \_ \_ utilise pas**

[Catégorie de filtre](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Notes

L’encodeur vidéo MPEG-2 peut générer les types de sortie suivants :

-   Flux élémentaire vidéo
-   Vidéo dans un flux de programme MPEG-2
-   Vidéo dans un flux de transport MPEG-2

Il prend en charge les profils et niveaux MPEG-2 suivants :



| Profil        | Niveaux                     | Notes                                            |
|----------------|----------------------------|----------------------------------------------------|
| Profil simple | Principal                       |                                                    |
| Profil Main   | Faible, main, haute, haute-1440 |                                                    |
| Profil élevé   | Principale, haute, haute-1440      | Aucune évolutivité ni prise en charge 4:2:2/4:4:4 (seulement 4:2:0) |
| Profil 4:2:2  | Principale, haute                 | Aucune évolutivité ni prise en charge 4:2:2 (seulement 4:2:0)       |



 

### <a name="codec-properties"></a>Propriétés du codec

Le filtre prend en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi).



| Propriété                                                                                      | Default                                                          | Valeurs prises en charge                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                             | Vidéo MPEG-2                                                     | **\_GUID CODECAPI \_ AVEncMPEG1Video**<br/> **\_GUID CODECAPI \_ AVEncMPEG2Video**<br/>                                                                                                                        |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)                         | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)                       | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                               | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)                   | Non spécifié                                                      | **CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified** (aucune contrainte de format)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V** (DVD-vidéo)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatVCD** (CD vidéo)<br/> |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                               | 9,8 millions (9,8 Mbits/s)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                             | 7 millions (7,0 Mbits/s)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                               | 128                                                              |                                                                                                                                                                                                                      |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)                         | 1                                                                | 1                                                                                                                                                                                                                    |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                                     | 100                                                              | 1 — 100                                                                                                                                                                                                              |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)                       | 75                                                               | 0 — 100                                                                                                                                                                                                              |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)                     | CBR                                                              | **eAVEncCommonRateControlMode \_ CBR**<br/> **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**<br/> **\_qualité eAVEncCommonRateControlMode**<br/>                                                   |
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                               | Non spécifié                                                      | eAVEncInputVideoSystem \_ non spécifié<br/> eAVEncInputVideoSystem \_ PAL<br/> eAVEncInputVideoSystem \_ NTSC<br/>                                                                                        |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)                 | 2                                                                | 0 – 2                                                                                                                                                                                                                |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                             | Mode image                                                       |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)         | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)                 | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                           | **FALSE**                                                        |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                       | 1                                                                | 0 – 1                                                                                                                                                                                                                |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                           | 18 frames (36 champs) pour NTSC ; 15 frames (30 champs) dans le cas contraire. | 1:30 ; Voir les notes                                                                                                                                                                                                  |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                         | 9                                                                | 8-10                                                                                                                                                                                                               |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                               | Élevé                                                             |                                                                                                                                                                                                                      |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                           | Principal                                                             |                                                                                                                                                                                                                      |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)   | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)               | Interlaced                                                       | **eAVEncVideoSourceScan \_ entrelacé**<br/> **eAVEncVideoSourceScan \_ progressif**<br/>                                                                                                                   |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)           | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)         | Identique à la source                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)         | Identique à la source                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)               | Identique à la source                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md) | Identique à la source                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)     | Identique à la source                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)               | [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1          | 0 ou [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                                                                                                                                                         |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                 | 0                                                                |                                                                                                                                                                                                                      |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)         | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                       |                                                                  | Doit être identique à la fréquence d’images d’entrée.                                                                                                                                                                            |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                         | Comme dans l’entrée                                                    | **eAVEncVideoOutputScan \_ SameAsInput**                                                                                                                                                                               |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                     | 1:1                                                              |                                                                                                                                                                                                                      |



 

Il est recommandé de définir des propriétés dans l’ordre suivant :

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncCodecType**](avenccodectype-property.md)
3.  [**AVEncMPVProfile**](avencmpvprofile-property.md)
4.  [**AVEncMPVLevel**](avencmpvlevel-property.md)
5.  [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)

Définissez les propriétés restantes dans n’importe quel ordre. (Toutefois, consultez [structure GOP](#gop-structure).)

Il est possible de définir des propriétés pendant l’exécution du graphique de filtre. Il y a un délai d’au moins un groupe d’images avant que les nouveaux paramètres prennent effet.

### <a name="encoder-operation"></a>Opération d’encodeur

Lors de l’encodage d’une vidéo MPEG-1, l’encodeur définit automatiquement le code de l' **\_ \_ indicateur de paramètres restreints** 1 bit dans l’en-tête de séquence si toutes les contraintes sont satisfaites.

Si nécessaire, l’encodeur arrondit les dimensions de la vidéo d’entrée de sorte que les dimensions de la vidéo de sortie correspondent aux exigences MPEG. Pour une vidéo progressive, les dimensions de sortie sont arrondies à un multiple de 16 en largeur et en hauteur. Pour la vidéo entrelacée, la largeur est arrondie à un multiple de 16 et la hauteur est arrondie à un multiple de 32. Cette opération d’arrondi utilise le remplissage en fonction des besoins.

Si la vidéo est entrelacée, l’encodeur effectue la détection automatique de télécinéma (3:2 Pull-up). La vidéo d’entrée peut contenir des paires d’images de champ, en plus des images entrelacées.

Le format interne de l’encodeur est 4:2:0 IYUV (identique à i420). Il peut effectuer une conversion de couleur à partir de formats vidéo YUY2, YV12, UYVY et RGB-24.

Pour contraindre le flux binaire à un format cible (DVD ou VCD), définissez la propriété [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md) . Si cette propriété a une valeur autre que **GUID \_ AVEncCommonFormatUnSpecified**, l’encodeur limite la syntaxe MPEG à celle autorisée par le format cible.

Pour l’encodage en temps réel, définissez la propriété [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) sur zéro. Cela provoque l’optimisation de l’encodeur pour la vitesse.

### <a name="encoding-modes"></a>Modes d’encodage

L’encodeur prend en charge plusieurs modes d’encodage :

-   Vitesse de transmission constante à un passage (CBR).
-   Vitesse de transmission variable (VBR) basée sur la qualité d’un passage, à l’aide d’une taille d’étape de quantification constante. Dans ce mode, l’encodeur tente de respecter un niveau de qualité cible, jusqu’à une vitesse de transmission maximale.
-   VBR avec une limite de pic à un passage. Dans ce mode, l’encodeur tente d’obtenir un débit binaire moyen cible dans certaines limites internes.

Pour configurer le mode d’encodage, définissez les propriétés suivantes :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mode</th>
<th>Propriétés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CBR</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_CBR</strong><br/> <a href="avenccommonqualityvsspeed-property.md"><strong>AVEncCommonQualityVsSpeed</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
<tr class="even">
<td>VBR basé sur la qualité</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_Quality</strong><br/> <a href="avenccommonquality-property.md"><strong>AVEncCommonQuality</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/>
<blockquote>
[!Note]<br />
Dans ce mode, les propriétés <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a> et <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a> ne sont pas utilisées. La vitesse de transmission minimale est supposée être égale à zéro.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>VBR avec un pic restreint</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong><br/> <a href="avenccommonmultipassmode-property.md"><strong>AVEncCommonMultipassMode</strong></a> = 1<br/> <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Le VBR en deux passes n’est pas pris en charge.

 

### <a name="aspect-ratio"></a>Proportions

Les proportions d’affichage et les proportions en pixels (PAR) sont liés par la formule suivante :

<dl> Afficher les proportions = PAR × (largeur d’image/hauteur d’image)  
</dl>

L’encodeur utilise cette formule pour calculer la valeur de la \_ \_ proportion PEL pour les flux de données MPEG-1 ou les informations de proportions \_ \_ pour les flux de données MPEG-2. (Voir les normes ISO/IEC 11172 et ISO/IEC 138181-2, respectivement).

L’encodeur essaie les paramètres suivants, dans l’ordre :

1.  Si l’application définit la propriété [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md) à tout moment avant l’exécution du graphique de filtre, cette propriété est utilisée pour le pair.
2.  Sinon, si les membres **dwPictAspectRatioX** et **dwPictAspectRatioY** de la structure [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) sont non null, ces membres sont utilisés pour les proportions d’affichage, et le par est calculé à partir des proportions d’affichage.
3.  Si aucune de ces valeurs n’est présente, le pair est supposé être 1,0 et les proportions de l’affichage sont calculées en conséquence.

Dans le mode d’encodage en temps réel ([**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) égal à zéro), les proportions de l’affichage doivent être 4:3 ou 16:9, avec une valeur par défaut de 4:3. Si les proportions de l’affichage calculé ne sont pas 4:3 ou 16:9, l’encodeur utilise la valeur 4:3.

### <a name="gop-structure"></a>GOP, structure

Pour spécifier la structure du groupe d’images (GOP), définissez les propriétés suivantes dans l’ordre :

1.  [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)
2.  [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)
3.  [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)

En fonction de ces paramètres, l’encodeur produit l’une des structures GOP suivantes :



| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md) | [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md) | GOP, structure |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| 0                                                                               | 0                                                                             | IIII...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 0                                                                             | IPPP...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 1                                                                             | IBPBP...      |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 2                                                                             | IBBPBBP...    |



 

La structure GOP par défaut est IBBPBBP... avec une taille GOP de 15 frames.

Si l’application limite le format cible au DVD (par le biais de la propriété [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md) ) et définit la propriété [**AVEncInputVideoSystem**](avencinputvideosystem-property.md) sur NTSC ou PAL, l’encodeur prend en charge les tailles de groupe d’images suivantes :



| Système vidéo | Tailles de groupe d’images valides | Taille de groupe d’images par défaut |
|--------------|-----------------|------------------|
| NTSC         | 1-18            | 18 (champs 36)   |
| PAL          | 1-15            | 15 (30 champs)   |



 

### <a name="codec-property-change-lists"></a>Listes de modifications de propriétés de codec

La définition de la valeur d’une propriété de codec peut modifier la plage valide d’une autre propriété. (Par exemple, la limitation du format cible limite la vitesse de transmission moyenne.) Chaque fois que l’application définit une propriété, l’encodeur vérifie si d’autres propriétés se trouvent à l’extérieur de la plage valide. Si c’est le cas, l’encodeur réinitialise cette propriété à sa nouvelle valeur par défaut. Pour recevoir des notifications lorsque cela se produit, procédez comme suit :

1.  Appelez [**ICodecAPI :: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) avec la valeur **CODECAPI \_ CHANGELISTS**.
2.  Utilisez l’interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pour surveiller les événements à partir du graphique de filtre.
3.  Si la plage ou la valeur par défaut d’une propriété change, l’encodeur envoie un événement d' [**\_ \_ événement EC CODECAPI**](ec-codecapi-event.md) avec une liste de propriétés modifiées.

### <a name="iencoderapi-support"></a>Support IEncoderAPI

Pour la compatibilité descendante, le filtre prend en charge les propriétés suivantes par le biais de l’interface **IEncoderAPI** :



| Propriété                       | Description                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------|
| **\_débit binaire ENCAPIPARAM**       | Équivalent à [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).         |
| **\_débit maximal de pic ENCAPIPARAM \_** | Équivalent à [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md).           |
| **\_Mode débit \_ ENCAPIPARAM** | Équivalent à [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md). |



 

Lors de la définition de la propriété **\_ \_ mode de débit ENCAPIPARAM** , les valeurs sont mappées comme suit :



| **\_Mode débit \_ ENCAPIPARAM** | [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) |
|--------------------------------|---------------------------------------------------------------------------|
| **ConstantBitRate**            | **eAVEncCommonRateControlMode \_ CBR**                                      |
| **VariableBitRateAverage**     | Consultez Remarque.                                                                 |
| **VariableBitRatePeak**        | **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       |



 

> [!Note]  
> Actuellement, l’encodeur vidéo MPEG-2 ne prend pas en charge le mode d’encodage **VariableBitRateAverage** . Si vous définissez cette valeur, l’encodeur par défaut est l’encodage CBR (**eAVEncCommonRateControlMode \_ CBR**).

 

Lors de l’obtention de la propriété du **\_ \_ mode de débit binaire ENCAPIPARAM** , les valeurs sont mappées comme suit :



| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) | **\_Mode débit \_ ENCAPIPARAM** |
|---------------------------------------------------------------------------|--------------------------------|
| **eAVEncCommonRateControlMode \_ CBR**                                      | **ConstantBitRate**            |
| **\_qualité eAVEncCommonRateControlMode**                                  | **VariableBitRatePeak**        |
| **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       | **VariableBitRatePeak**        |



 

### <a name="limitations"></a>Limites

Actuellement, l’encodeur ne prend pas en charge les fonctionnalités suivantes :

-   Génération de paquets d’extension de flux élémentaires (PES) paquets.
-   Conversion de la fréquence des images. Le flux d’entrée doit avoir une fréquence d’images valide pour un flux de données MPEG-2.
-   Extensions de fréquence d’images pour MPEG-2 **( \_ extension de fréquence d’images \_ \_ n**, extension de fréquence d’images **\_ \_ \_ d**).
-   Positions de mémoire tampon d’entrée/sortie (VBV) pour un clip.
-   Insertion de données de ligne-21 (informations de sous-titres) dans le flux élémentaire vidéo.
-   Définition du champ de **\_ Code de temps** de 25 bits dans l’en-tête de groupe d’images pour MPEG-2.
-   Filtre de dénoise.
-   Gestion des droits numériques (DRM).

L’encodeur introduit une latence d’encodage d’au moins un groupe d’images.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista Édition familiale Premium, Windows Vista Édition intégrale, Windows 7 Édition familiale Premium, Windows 7 professionnel, Windows 7 entreprise, applications de bureau Windows 7 édition intégrale \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[**Types de média du démultiplexeur MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
