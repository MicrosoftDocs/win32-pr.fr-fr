---
description: Cette rubrique fournit des instructions pour l’implémentation d’un décodeur ou d’un encodeur en tant que transformation de Media Foundation (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implémentation d’une table MFT de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415816"
---
# <a name="implementing-a-codec-mft"></a>Implémentation d’une table MFT de codec

Cette rubrique fournit des instructions pour l’implémentation d’un décodeur ou d’un encodeur en tant que transformation de Media Foundation (MFT).

-   [Encodeurs](#encoders)
    -   [Négociation du format d’encodeur](#encoder-format-negotiation)
-   [Décodeurs](#decoders)
    -   [Décodeurs de transcodage uniquement](#transcode-only-decoders)
    -   [Attributs Telecine](#telecine-attributes)
-   [Rubriques connexes](#related-topics)

## <a name="encoders"></a>Encodeurs

### <a name="encoder-format-negotiation"></a>Négociation du format d’encodeur

La procédure suivante est utilisée pour initialiser un encodeur :

1.  Interrogez la MFT pour l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .
2.  Appelez [**ICodecAPI :: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) pour définir les propriétés d’encodage.
3.  Appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le format d’encodage.
4.  Appelez [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) pour obtenir la liste des types d’entrée compatibles. (Cette étape peut être ignorée.)
5.  Appelez [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) pour définir le format d’entrée non compressé.

Une fois que le type de sortie est défini à l’étape 3, la méthode [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) doit retourner une liste de types d’entrée compatibles avec le type de sortie actuel. En d’autres termes, tous les types retournés par **GetInputAvailableType** à ce stade doivent être valides pour [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

Pour les décodeurs, l’ordre dans lequel les types sont définis est inversé : le type d’entrée est défini en premier, suivi du type de sortie. Une fois le type d’entrée défini, la méthode [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) doit retourner une liste de types qui peuvent être passés à la méthode [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) .

Les encodeurs et les décodeurs doivent prendre en charge NV12 comme format non compressé courant. Cela permet de s’assurer que les composants de pipeline peuvent interagir avec des conversions colorspace minimales. Bien entendu, d’autres formats peuvent également être pris en charge.

## <a name="decoders"></a>Décodeurs

### <a name="transcode-only-decoders"></a>Décodeurs Transcode-Only

Certains décodeurs sont optimisés pour le transcodage (décodage et recodage d’un flux) et ne peuvent pas être utilisés pendant la lecture.

Si une table MFT du décodeur est destinée uniquement au transcodage, définissez l’indicateur de l' **\_ indicateur d’énumération MFT \_ \_ \_ uniquement** lorsque vous inscrivez la table MFT. (Voir [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)

Par défaut, les décodeurs de transcodage ne sont pas retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) . Pour énumérer les décodeurs de transcodage, appelez **MFTEnumEx** et définissez l’indicateur **MFT \_ enum enum \_ \_ \_ only** dans le paramètre *Flags* . Lorsqu’il est utilisé dans la fonction **MFTEnumEx** , cet indicateur énumère à la fois les décodeurs de transcodage et les autres décodeurs.



| **Indicateur d' \_ énumération MFT MFTRegister \_ \_ \_ uniquement** | **Indicateur d' \_ énumération MFT MFTEnumEx \_ \_ \_ uniquement** | La table MFT est-elle énumérée ? |
|--------------------------------------------------|------------------------------------------------|--------------------|
| 1                                                | 1                                              | Oui                |
| 1                                                | 0                                              | Non                 |
| 0                                                | 1                                              | Oui                |
| 0                                                | 0                                              | Oui                |



 

### <a name="telecine-attributes"></a>Attributs Telecine

La source du média peut attacher les attributs de télécinéma suivants aux exemples de supports qu’elle remet.



| Attribut                                                                                   | Description                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md) | Équivaut à l’indicateur « REPEAT First Field » (RFF). |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) | Inverse de l’indicateur « Top Field First » (TFF).       |



 

Ces indicateurs fournissent un indicateur au convertisseur vidéo amélioré (EVR) lorsqu’il effectue une désentrelacement. Un décodeur doit propager ces indicateurs en aval en les copiant dans les exemples de sortie, afin qu’ils atteignent le EVR.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)
</dt> </dl>

 

 
