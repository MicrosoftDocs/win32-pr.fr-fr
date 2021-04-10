---
title: Pour récupérer des exemples de médias avec le lecteur asynchrone
description: Pour récupérer des exemples de médias avec le lecteur asynchrone
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- ASF (Advanced Systems Format), récupération des exemples de supports
- ASF (format des systèmes avancés), récupération des exemples de média
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, récupération d’exemples de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030789"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a>Pour récupérer des exemples de médias avec le lecteur asynchrone

Une fois que vous avez reçu le \_ message d’état d’ouverture de WMT dans votre implémentation de [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), vous pouvez commencer à recevoir des exemples en appelant [**IWMReader :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start). Le lecteur asynchrone fournit des exemples à votre implémentation de [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Les exemples sont fournis dans l’ordre de la présentation.

**Start** est un appel asynchrone. Elle retourne presque immédiatement et continue de s’exécuter sur des threads distincts. Le lecteur asynchrone utilise plusieurs threads lors du décodage du contenu et de la diffusion des exemples. Quand la fin du fichier est atteinte, le lecteur envoie un message d' \_ État d’un EOF WMT à votre implémentation du rappel **OnStatus** . Lors de \_ l’envoi d’un EOF WMT, le lecteur arrête son propre traitement. vous n’avez pas besoin de répondre à la fin de la \_ demande WMT avec un appel à [**IWMReader :: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Pour implémenter des messages de lecture dans le rappel OnStatus**](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[**Pour implémenter le rappel OnSample**](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




