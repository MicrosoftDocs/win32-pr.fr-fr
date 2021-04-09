---
description: Formats de fichiers personnalisés
ms.assetid: 4dc77cfa-0cab-4055-9e11-f036e2d1dcca
title: Formats de fichiers personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361dca97fcd34b30e3c29d6ba189ad26968d4fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950191"
---
# <a name="custom-file-formats"></a>Formats de fichiers personnalisés

Si vous disposez d’un filtre MUX ou d’enregistreur de fichiers personnalisé qui prend en charge votre propre format de fichier, vous pouvez spécifier le CLSID comme premier paramètre de la méthode [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



Pour plus d’informations sur cette utilisation, consultez [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo dans un fichier](capturing-video-to-a-file.md)
</dt> </dl>

 

 



