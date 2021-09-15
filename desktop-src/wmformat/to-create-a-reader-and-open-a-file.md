---
title: Pour créer un lecteur et ouvrir un fichier
description: Pour créer un lecteur et ouvrir un fichier
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- ASF (Advanced Systems Format), création de lecteurs
- ASF (format avancé des systèmes), création de lecteurs
- ASF (Advanced Systems Format), ouvrir des fichiers
- ASF (format des systèmes avancés), ouvrir des fichiers
- lecteurs asynchrones, création
- lecteurs asynchrones, ouverture de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294406"
---
# <a name="to-create-a-reader-and-open-a-file"></a>Pour créer un lecteur et ouvrir un fichier

Avant de pouvoir travailler avec le lecteur, vous devez créer un objet lecteur et charger un fichier en lecture. Pour initialiser le lecteur et ouvrir un fichier, procédez comme suit.

1.  Créez un objet lecteur en appelant la fonction [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) . Vous devez spécifier le niveau de gestion des droits souhaité pour le nouvel objet lecteur. Les modes disponibles sont répertoriés dans le type d’énumération des [**\_ droits WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .
2.  Spécifiez un fichier à lire en appelant [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open). Vous devez spécifier une interface de rappel de lecteur pour le lecteur à utiliser. Pour plus d’informations sur le rappel de lecteur, consultez [pour implémenter des messages de lecture dans le rappel OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md).
3.  Attendez que le lecteur ouvre le fichier. Quand vous appelez **Open** pour charger un fichier, il retourne presque immédiatement et continue le traitement sur un autre thread. Vous devez attendre que les opérations se terminent, en signalant un événement lorsque le rappel **OnStatus** reçoit le \_ message d’état ouvert WMT.

Le lecteur prend également en charge l’utilisation de l’interface com **IStream** pour ouvrir des fichiers. Vous pouvez implémenter l’interface **IStream** comme vous le souhaitez. Une fois le fichier souhaité ouvert dans **IStream**, vous pouvez suivre les étapes décrites ci-dessus, sauf que vous devez appeler [**IWMReaderAdvanced2 :: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) au lieu de **IWMReader :: Open** à l’étape 2.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interface IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Utilisation des méthodes de rappel**](using-the-callback-methods.md)
</dt> </dl>

 

 




