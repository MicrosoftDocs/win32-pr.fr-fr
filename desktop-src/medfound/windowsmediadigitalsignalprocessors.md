---
description: Processeurs de signaux numériques
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Processeurs de signaux numériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f5c9aa0ee3c4cc2a8c7f725b3a8444f4852c8c5b52ee3713b533ec435f4a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100941"
---
# <a name="digital-signal-processors"></a>Processeurs de signaux numériques

Cette section décrit les objets DSP (digital signal Processor) fournis par Windows.

Microsoft utilise le terme « *processeur de signal numérique* » pour désigner un ensemble d’objets COM qui effectuent des transformations sur des données audio et vidéo non compressées. Les DSP décrits dans ce kit de développement logiciel (SDK) transforment l’audio et la vidéo dans différents formats non compressés.

Les DSP peuvent être utilisés par eux-mêmes, ou en combinaison avec des codecs audio et vidéo. À l’exception du DSP de capture vocale, chaque DSP répertorié ici implémente deux interfaces distinctes mais similaires.



| Interface                              | Description                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatible avec Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatible avec DirectShow.                 |



 

Vous pouvez configurer le DSP à l’aide de l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour définir les propriétés. Certains DSP ont des interfaces supplémentaires qui définissent des propriétés. Pour utiliser ces interfaces, appelez la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de toute autre interface du DSP. La rubrique de référence pour chaque DSP répertorie les propriétés, interfaces et autres fonctionnalités prises en charge.

Cette section contient les rubriques suivantes :



| DSP                                                      | Description                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [Modèle de rééchantillonnage audio DSP](audioresampler.md)                | Convertit le taux d’échantillonnage d’un flux audio.       |
| [Transformation de contrôle de couleur DSP](colorcontroltransform.md) | Ajuste les caractéristiques de couleur d’un flux vidéo. |
| [Convertisseur de couleurs DSP](colorconverter.md)                | Convertit un flux vidéo entre des formats de couleur.       |
| [Convertisseur de fréquence d’images DSP](framerateconverter.md)       | Modifie la fréquence d’images d’un flux vidéo.            |
| [Dimensionnement vidéo DSP](videoresizer.md)                    | Redimensionne un flux vidéo.                              |
| [DSP de capture vocale](voicecapturedmo.md)                 | Encapsule plusieurs DSP associés à la capture vocale.  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de programmation Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
