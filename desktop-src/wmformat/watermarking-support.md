---
title: Prise en charge du filigrane
description: Prise en charge du filigrane
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows Media Format SDK, prise en charge du filigrane
- Kit de développement logiciel (SDK) Windows Media format, filigrane numérique
- ASF (Advanced Systems Format), prise en charge du filigrane
- ASF (format des systèmes avancés), prise en charge du filigrane
- ASF (Advanced Systems Format), filigrane numérique
- ASF (format de systèmes avancés), filigrane numérique
- SDK Windows Media format, DMO
- ASF (Advanced Systems Format), DMO
- ASF (format des systèmes avancés), DMO
- Windows Media Format SDK, interface IWMWatermarkInfo
- ASF (Advanced Systems Format), interface IWMWatermarkInfo
- ASF (format des systèmes avancés), interface IWMWatermarkInfo
- filigrane, à propos de
- filigrane numérique
- DirectX Media Object (DMO), à propos de
- DMO (objet multimédia DirectX), à propos de
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511876"
---
# <a name="watermarking-support"></a>Prise en charge du filigrane

Le filigrane numérique est un moyen d’incorporer des droits d’auteur ou d’autres informations dans les données d’un flux multimédia. Les techniques de filigrane varient considérablement d’une solution à l’autre. La forme la plus simple de filigrane est d’ajouter simplement une image d’identification à chaque image d’un flux vidéo. Les stations de télévision utilisent souvent cette technique pour insérer un logo semi-transparent dans le coin inférieur de leur diffusion. Des formes plus sophistiquées de filigrane numérique sont imperceptibles à l’utilisateur qui regarde ou écoute le contenu.

Le kit de développement logiciel (SDK) Windows Media format prend en charge l’utilisation de [*DMOs*](wmformat-glossary.md)de filigrane numérique. Dans la pratique, un système de filigrane est très similaire à un codec : il prend des exemples de supports, exécute des algorithmes sur les données et génère les exemples modifiés. Lorsqu’un système de filigrane est spécifié pour un flux de données, l’objet Writer comprend le module DMO dans son traitement d’exemples d’entrée.

Vous devez spécifier les informations de configuration du filigrane lorsque vous configurez un flux pour le filigrane. Les valeurs de configuration sont différentes en fonction du filigrane DMO. La DMO que vous utilisez doit être accompagnée d’instructions décrivant les valeurs de configuration qu’elle prend en charge.

Pour plus d’informations sur les paramètres utilisés pour spécifier un système de filigrane, consultez [ **IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)

Vous pouvez programmer votre application pour énumérer les DMOs de filigranes installés sur l’ordinateur client. Pour plus d’informations, consultez l’interface [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités d’écriture de fichier**](file-writing-features.md)
</dt> </dl>

 

 




