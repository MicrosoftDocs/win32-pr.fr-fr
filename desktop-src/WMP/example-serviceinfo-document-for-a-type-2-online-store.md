---
title: Exemple de document ServiceInfo pour un magasin de type 2 en ligne
description: Exemple de document ServiceInfo pour un magasin de type 2 en ligne
ms.assetid: d9bbce89-15b4-495f-8995-24dda99a4f40
keywords:
- Lecteur Windows Media des magasins en ligne, exemple de document ServiceInfo
- magasins en ligne, exemple de document ServiceInfo
- type 2 magasins en ligne, exemple de document ServiceInfo
- Lecteur Windows Media les magasins en ligne, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- magasins en ligne Lecteur Windows Media, exemple de code
- magasins en ligne, exemple de code
- types 2 magasins en ligne, exemple de code
- exemple de document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02214b9d7180296fa11bb877f978c6bde85f3a4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217113"
---
# <a name="example-serviceinfo-document-for-a-type-2-online-store"></a>Exemple de document ServiceInfo pour un magasin de type 2 en ligne

L’exemple de code suivant affiche un document ServiceInfo.xml complet. Vous pouvez utiliser ce code XML comme point de départ pour votre propre document ServiceInfo.


```C++
<?xml version="1.0" encoding="utf-8" ?>
<ServiceInfo Version="1.00" Key="Proseware">
    <FriendlyName>Proseware Service</FriendlyName>
    <Image 
        MenuURL = "https://www.proseware.com/service/images/menuicon.jpg"
        ServiceLargeURL = "https://www.proseware.com/service/images/30x30.jpg" />
    <Color
        MediaPlayer = "#FF8040"
        MediaPlayerText = "#FFFFFF"/>
    <ServiceTask1
        URL = "https://www.proseware.com/service/html/Music.asp">
        <ButtonText>Proseware\nMusic</ButtonText>
        <ButtonTip>Proseware Music Store</ButtonTip>
    </ServiceTask1>
    <ServiceTask2
        URL = "https://www.proseware.com/service/html/Video.asp">
        <ButtonText>Proseware\nVideo</ButtonText>
        <ButtonTip>Proseware Video</ButtonTip>
    </ServiceTask2>
    <ServiceTask3
        URL = "https://www.proseware.com/service/html/Radio.asp">
        <ButtonText>Proseware\nRadio</ButtonText>
        <ButtonTip>Proseware Radio</ButtonTip>
    </ServiceTask3>
    <Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
    </Navigate>
    <InfoCenter
        URL = "https://www.proseware.com/service/html/InfoCenter.asp"/>
    <AlbumInfo
        URL = "https://www.proseware.com/service/html/AlbumInfo.asp"/>
    <BuyCD
        MediaPlayerURL = "https://www.proseware.com/service/html/BuyCDMediaPlayer.asp"
        MediaCenterURL = "https://www.proseware.com/service/html/BuyCDMediaCenter.asp"
        BrowserURL = "https://www.proseware.com/service/html/BuyCDBrowser.asp"/>
    <DownloadStatus
        URL = "https://www.proseware.com/service/html/Music_Download.htm"/>
    <HTMLView
        BaseURL = "https://www.proseware.com/"/>
</ServiceInfo>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins en ligne de type 2**](programming-guide-for-type-2-online-stores.md)
</dt> <dt>

[**Document ServiceInfo pour un magasin de type 2 en ligne**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




