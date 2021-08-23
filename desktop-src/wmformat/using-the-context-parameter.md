---
title: Utilisation du paramètre de contexte
description: Utilisation du paramètre de contexte
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Media Format SDK, paramètre de contexte
- Windows Media Format SDK, paramètre pvContext
- paramètre pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102315470243910158fd3bf474a209fa1e0888536671e3ede3764be519c672f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585199"
---
# <a name="using-the-context-parameter"></a>Utilisation du paramètre de contexte

certains des rappels utilisés par le kit de développement logiciel (SDK) de Format multimédia Windows prennent un paramètre appelé *pvContext*. Les objets appelants passent le long de la valeur que vous spécifiez dans la méthode qui a démarré l’action asynchrone. Par exemple, quand vous appelez [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), vous pouvez passer une valeur pour *pvContext*. Quand la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) est appelée par l’objet lecteur pour informer votre application que le fichier a été ouvert, elle transmet la valeur que vous avez utilisée dans votre appel à **Open** en tant que paramètre *pvContext* de **OnStatus**. Ce paramètre de contexte est fourni pour votre utilisation et vous pouvez l’utiliser comme vous le souhaitez.

Le paramètre *pvContext* est le plus souvent utilisé lorsque plusieurs objets doivent partager le même rappel. Par exemple, plusieurs objets utilisent la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Vous pouvez utiliser *pvContext* pour permettre aux différents objets de partager une implémentation de **OnStatus** en passant une valeur différente pour *pvContext* sur votre appel d’origine. Dans votre implémentation de **OnStatus**, vous pouvez créer une branche de la logique de gestion des messages en fonction de la valeur de *pvContext*.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des méthodes de rappel**](using-the-callback-methods.md)
</dt> </dl>

 

 




