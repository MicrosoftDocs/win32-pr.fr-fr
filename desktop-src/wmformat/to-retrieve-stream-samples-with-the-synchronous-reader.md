---
title: Pour récupérer des exemples de flux avec le lecteur synchrone
description: Pour récupérer des exemples de flux avec le lecteur synchrone
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- ASF (Advanced Systems Format), récupération d’exemples de flux
- ASF (format des systèmes avancés), récupération des exemples de flux
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs synchrones, récupération des exemples de flux
- flux, récupérer des exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101253"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a>Pour récupérer des exemples de flux avec le lecteur synchrone

Comme pour le lecteur asynchrone, le lecteur synchrone peut récupérer des échantillons par numéro de flux. Contrairement au lecteur asynchrone, le lecteur synchrone peut fournir des exemples de flux, compressés ou décompressés.

Pour recevoir des exemples de flux, procédez comme suit.

1.  À tout moment avant ou pendant la lecture, appelez [**IWMSyncReader :: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) en passant le numéro de flux souhaité.
2.  Récupérez des exemples avec des appels continus à [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).

Vous pouvez vérifier si un flux est sélectionné pour l’exemple de remise en appelant [**IWMSyncReader :: GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




