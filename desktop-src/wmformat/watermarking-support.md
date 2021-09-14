---
title: Prise en charge du filigrane
description: Prise en charge du filigrane
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows Media Format SDK, prise en charge du filigrane
- Windows Media Format SDK, mise en filigrane numérique
- ASF (Advanced Systems Format), prise en charge du filigrane
- ASF (format des systèmes avancés), prise en charge du filigrane
- ASF (Advanced Systems Format), filigrane numérique
- ASF (format de systèmes avancés), filigrane numérique
- Windows Media Format SDK, DMO
- ASF (Advanced Systems Format), DMO
- ASF (format avancé des systèmes), DMO
- Windows Media Format SDK, interface IWMWatermarkInfo
- ASF (Advanced Systems Format), interface IWMWatermarkInfo
- ASF (format des systèmes avancés), interface IWMWatermarkInfo
- filigrane, à propos de
- filigrane numérique
- objet multimédia DirectX (DMO), à propos de
- DMO (objet DirectX Media), à propos de
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225793"
---
# <a name="watermarking-support"></a>Prise en charge du filigrane

Le filigrane numérique est un moyen d’incorporer des droits d’auteur ou d’autres informations dans les données d’un flux multimédia. Les techniques de filigrane varient considérablement d’une solution à l’autre. La forme la plus simple de filigrane est d’ajouter simplement une image d’identification à chaque image d’un flux vidéo. Les stations de télévision utilisent souvent cette technique pour insérer un logo semi-transparent dans le coin inférieur de leur diffusion. Des formes plus sophistiquées de filigrane numérique sont imperceptibles à l’utilisateur qui regarde ou écoute le contenu.

le kit de développement logiciel (SDK) Windows Media Format prend en charge l’utilisation de [*DMOs*](wmformat-glossary.md)de filigrane numérique. Dans la pratique, un système de filigrane est très similaire à un codec : il prend des exemples de supports, exécute des algorithmes sur les données et génère les exemples modifiés. lorsqu’un système de filigrane est spécifié pour un flux de données, l’objet writer comprend les DMO dans son traitement des exemples d’entrée.

Vous devez spécifier les informations de configuration du filigrane lorsque vous configurez un flux pour le filigrane. Les valeurs de configuration sont différentes en fonction de la DMO de filigrane. le DMO que vous utilisez doit être fourni avec des instructions décrivant les valeurs de configuration qu’il prend en charge.

Pour plus d’informations sur les paramètres utilisés pour spécifier un système de filigrane, consultez [ **IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)

Vous pouvez programmer votre application pour énumérer les DMOs de filigranes installés sur l’ordinateur client. Pour plus d’informations, consultez l’interface [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités d’écriture de fichier**](file-writing-features.md)
</dt> </dl>

 

 




