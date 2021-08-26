---
title: À propos de IMFTransform
description: À propos de IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- plug-ins Lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
- plug-ins Lecteur Windows Media, interface IMFTransform
- plug-ins, interface IMFTransform
- plug-ins de traitement de signal numérique, interface IMFTransform
- Plug-ins DSP, interface IMFTransform
- Interface IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b410702d63657261faa2fc8e7db123e05dcdc12c3096a49f8c0e2e36a41ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903579"
---
# <a name="about-imftransform"></a>À propos de IMFTransform

L’interface **IMFTransform** est l’une des interfaces qui doivent être implémentées par un plug-in DSP à double mode. Lecteur Windows Media appelle les méthodes de l’interface **IMFTransform** pour fournir des données au plug-in et récupérer les données traitées à partir du plug-in. pour obtenir la documentation complète de l’interface **IMFTransform** , consultez la section Media Foundation de la SDK Windows.

Les méthodes de **IMFTransform** peuvent être classées comme suit.

## <a name="methods-that-handle-format-negotiation"></a>Méthodes qui gèrent la négociation de format

Lecteur Windows Media appelle les méthodes suivantes pour obtenir des informations sur les formats de données pris en charge par le plug-in.

-   **GetStreamCount**
-   **GetStreamLimits**
-   **GetInputStreamInfo**
-   **GetOutputStreamInfo**
-   **GetInputAvailableType**
-   **GetOutputAvailableType**
-   **SetInputType**
-   **SetOutputType**
-   **GetAttributes,**
-   **GetInputStreamAttributes**
-   **GetOutputStreamAttributes**
-   **GetStreamIDs**

## <a name="methods-that-specify-or-retrieve-state-information"></a>Méthodes qui spécifient ou récupèrent les informations d’État

Lecteur Windows Media appelle les méthodes suivantes pour récupérer ou définir des valeurs relatives à l’état actuel du plug-in.

-   **SetInputType**
-   **SetOutputType**
-   **GetInputCurrentType**
-   **GetOutputCurrentType**
-   **GetInputStatus**
-   **AddInputStreams**
-   **DeleteInputStreams**
-   **GetOutputStatus**
-   **SetOutputBounds**

> [!Note]  
> **SetInputType** et **SetOutputType** sont utilisés à la fois pour la négociation de format et pour la spécification et la récupération des informations d’État.

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>Méthodes qui gèrent la mise en mémoire tampon et le traitement des données

Lecteur Windows Media appelle les méthodes suivantes pour initier les différents processus que le plug-in effectue pour effectuer le traitement du signal numérique.

-   **ProcessInput**
-   **ProcessOutput**
-   **ProcessMessage**
-   **ProcessEvent**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interfaces requises**](required-interfaces.md)
</dt> </dl>

 

 




