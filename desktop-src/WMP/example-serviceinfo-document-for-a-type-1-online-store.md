---
title: Exemple de document ServiceInfo pour une boutique en ligne de type 1
description: Exemple de document ServiceInfo pour une boutique en ligne de type 1
ms.assetid: 7d997773-1c11-44d5-ae67-05ba3909c481
keywords:
- Windows Media Player Online stores, exemple de document ServiceInfo
- magasins en ligne, exemple de document ServiceInfo
- tapez 1 magasins en ligne, exemple de document ServiceInfo
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- Windows Media Player Online stores, exemple de code
- magasins en ligne, exemple de code
- magasins en ligne de type 1, exemple de code
- exemple de document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1378c30a8dbbb46844923e9c73c242a28d5da3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674522"
---
# <a name="example-serviceinfo-document-for-a-type-1-online-store"></a><span data-ttu-id="41f3c-114">Exemple de document ServiceInfo pour une boutique en ligne de type 1</span><span class="sxs-lookup"><span data-stu-id="41f3c-114">Example ServiceInfo Document for a Type 1 Online Store</span></span>

<span data-ttu-id="41f3c-115">L’exemple de code suivant affiche un document ServiceInfo.xml complet.</span><span class="sxs-lookup"><span data-stu-id="41f3c-115">The following code example shows a complete ServiceInfo.xml document.</span></span> <span data-ttu-id="41f3c-116">Vous pouvez utiliser ce code XML comme point de départ pour votre propre document ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="41f3c-116">You can use this XML as a starting point for your own ServiceInfo document.</span></span>


```C++
<?xml version="1.0" encoding="utf-8" ?>
<ServiceInfo Version="1.00" Key="Proseware" ContentPartner="true">

    <FriendlyName>Proseware Service</FriendlyName>

    <Description>
        Proseware Music has all your favorite songs.
    </Description>

    <Image 
        EulaURL = "https://www.proseware.com/service/images/eula.png"
        MenuURL = "https://www.proseware.com/service/images/menuicon.jpg"
        ServiceLargeURL = "https://www.proseware.com/service/images/45x13Large.png"
        ServiceSmallURL = "https://www.proseware.com/service/images/45x13Small.png" />

    <Color
        MediaPlayer = "#FF8040"
        MediaPlayerText = "#FFFFFF"/>

    <ServiceTask1
        URL = "https://www.proseware.com/service/html/Music.asp">
        <ButtonText>Proseware\nMusic</ButtonText>
        <ButtonTip>Proseware Music Store</ButtonTip>
    </ServiceTask1>

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

    <Install
        EULAURL="https://www.proseware.com/service/html/eula.txt"
        CodeURL="https://www.proseware.com/service/html/ProsewareInstall.cab"
        PrivacyInfoURL="https://www.proseware.com/service/html/PrivacyPolicy.htm"
        InstallApp="ProsewareSetup.exe"  
        CatalogURL="https://www.proseware.com/service/html/Catalog.asp"/>

</ServiceInfo>
```



## <a name="related-topics"></a><span data-ttu-id="41f3c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41f3c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41f3c-118">**Guide de programmation pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="41f3c-118">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="41f3c-119">**Document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="41f3c-119">**ServiceInfo Document for a Type 1 Online Store**</span></span>](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="41f3c-120">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="41f3c-120">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




