---
title: Pour implémenter des messages de lecture dans le rappel OnStatus
description: Pour implémenter des messages de lecture dans le rappel OnStatus
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- ASF (Advanced Systems Format), implémentation de messages de lecture
- ASF (format des systèmes avancés), implémentation des messages de lecture
- ASF (Advanced Systems Format), rappel OnStatus
- ASF (format avancé des systèmes), rappel OnStatus
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, implémentation des messages de lecture
- OnStatus méthode de rappel, implémentation des messages de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05865d07c94f34807b35e46c625a2c82d943aaca37da77b90a6d94b3d1cace84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084039"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a>Pour implémenter des messages de lecture dans le rappel OnStatus

Pour utiliser le lecteur asynchrone pour distribuer du contenu à partir d’un fichier ASF, vous devez implémenter au moins deux méthodes de rappel, [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) et [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Cette section décrit comment implémenter **IWMStatusCallback :: OnStatus** pour recevoir les messages d’État envoyés par le lecteur et y répondre. **OnStatus** est utilisé par d’autres objets dans le kit de développement logiciel (SDK) de Format multimédia Windows. Pour obtenir des informations générales sur **OnStatus**, consultez [utilisation du rappel OnStatus](using-the-onstatus-callback.md).

Lorsque vous utilisez le lecteur asynchrone, vous devez intercepter les messages suivants dans **IWMStatusCallback :: OnStatus**.



| Message d’état | Description                                     |
|----------------|-------------------------------------------------|
| WMT \_ ouvert    | Envoyé lorsque les opérations d’ouverture de fichier sont terminées. |
| WMT \_ fermé    | Envoyé lorsque les opérations de fermeture de fichier sont terminées. |



 

Vous devez utiliser les messages d’État listés ci-dessus pour contrôler l’exécution de votre application de lecture. Par exemple, vous devez attendre la réception du message **WMT \_ ouvert** pour démarrer le lecteur ou appeler d’autres méthodes qui nécessitent que le lecteur dispose d’un fichier prêt. Souvent, les applications générées avec le lecteur asynchrone utilisent un événement pour signaler l’achèvement des appels asynchrones et poursuivre le traitement. Pour plus d’informations sur l’utilisation d’événements pour signaler l’achèvement des opérations, consultez [utilisation d’événements avec des appels asynchrones](using-events-with-asynchronous-calls.md).

De nombreux autres messages sont envoyés à **OnStatus** par l’objet lecteur pour permettre à l’application de répondre à l’état des opérations de lecture. Les valeurs de message d’État possibles sont définies dans le type d’énumération d' [**\_ État WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Utilisation du rappel OnStatus**](using-the-onstatus-callback.md)
</dt> </dl>

 

 




