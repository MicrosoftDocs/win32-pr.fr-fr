---
title: Pour utiliser l’enregistreur Postview
description: Pour utiliser l’enregistreur Postview
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- ASF (Advanced Systems Format), writer postview
- ASF (Advanced Systems Format), writer postview
- ASF (Advanced Systems Format), postviewing
- ASF (format avancé des systèmes), postviewing
- postview d’écriture
- postviewing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7800f3ba50f9f1d61793a0d2ada2db0c03d6b88551ac1147e17872aa8e428c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196403"
---
# <a name="to-use-writer-postview"></a>Pour utiliser l’enregistreur Postview

L’objet Writer fournit des fonctionnalités postviewing pour vous permettre de vérifier le contenu écrit sans avoir à configurer l’objet lecteur. L’objet Writer ne prend pas en charge postviewing pour le contenu audio.

Le postviewer du writer fonctionne à peu près de la même façon que l’objet lecteur asynchrone, uniquement avec moins de fonctionnalités. Pour plus d’informations sur la lecture des médias numériques, consultez [lecture des fichiers ASF](reading-asf-files.md).

Pour implémenter postviewer, procédez comme suit.

1.  Implémentez le rappel [**IWMWriterPostViewCallback :: OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) . Cette méthode est fondamentalement identique à [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , sauf qu’elle spécifie des numéros de flux au lieu de sorties.
2.  Configuré pour l’écriture comme d’habitude.
3.  Obtenez un pointeur vers l’interface [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) de l’objet writer en appelant **IWMWriter :: QueryInterface**.
4.  Définissez le rappel pour le postviewer à utiliser en appelant [**IWMWriterPostView :: SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).
5.  Pour chaque flux pour lequel vous souhaitez recevoir des exemples postview, appelez [**IWMWriterPostView :: SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). Vous pouvez vérifier si un flux est configuré pour recevoir des exemples postview en appelant [**IWMWriterPostView :: GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).
6.  Vous pouvez manipuler les exemples de formats, comme vous le feriez avec les formats de sortie dans l’objet lecteur ou l’objet lecteur synchrone.
7.  Lorsque vous commencez à écrire le fichier, vous commencerez à recevoir des exemples dans votre implémentation de la méthode de rappel **OnPostViewSample** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




