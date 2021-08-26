---
title: À propos des services de bibliothèque
description: À propos des services de bibliothèque
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Lecteur Windows Media, bibliothèque
- Lecteur Windows Media modèle objet, bibliothèque
- modèle objet, bibliothèque
- Lecteur Windows Media ActiveX contrôle, bibliothèque pour le modèle objet
- contrôle ActiveX, bibliothèque pour le modèle objet
- Lecteur Windows Media contrôle Mobile ActiveX, bibliothèque pour le modèle objet
- Lecteur Windows Media Mobile, bibliothèque pour le modèle objet
- bibliothèque de Lecteur Windows Media, à propos de
- bibliothèque de Lecteur Windows Media, services
- bibliothèque, services
- bibliothèque, à propos de
- versions de Lecteur Windows Media, services de bibliothèque
- énumérations, services de bibliothèque
- événements, services de bibliothèque
- exemples, services de bibliothèque
- interfaces, services de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc6f073fa4c361f114589e080145a3cb3bb0a8c78736ba2dd1464332a7f7adc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004510"
---
# <a name="about-library-services"></a>À propos des services de bibliothèque

dans les versions antérieures de Lecteur Windows Media, le logiciel utilisait une base de données de bibliothèque unique pour chaque utilisateur. Cette base de données a été stockée sur l’ordinateur de l’utilisateur et était conceptuellement liée à l’utilisateur et à une instance particulière du lecteur.

Lecteur Windows Media 11 introduit les concepts de bibliothèques multiples et distantes. désormais, en plus de sa bibliothèque par défaut ou *locale*, Lecteur Windows Media pouvez afficher le contenu récupéré à partir de bibliothèques sur d’autres ordinateurs connectés à un réseau, ce qui peut inclure d’autres utilisateurs connectés au même ordinateur. Le lecteur peut également afficher des vues de bibliothèque à partir d’autres sources, telles que des périphériques compatibles MTP ou des CD de données. du point de vue de l’utilisateur final, cela signifie que le contenu multimédia numérique situé dans de nombreux emplacements différents peut être géré à partir de plusieurs emplacements à l’aide de la même interface utilisateur Lecteur Windows Media familière. du point de vue du développeur, cela signifie que vous pouvez utiliser les interfaces COM du kit de développement logiciel (SDK) Lecteur Windows Media pour énumérer les bibliothèques disponibles, puis les utiliser comme vous avez utilisé la bibliothèque locale dans les versions antérieures.

Pour énumérer les bibliothèques disponibles, utilisez l’interface **IWMPLibraryServices** . Cette interface expose la méthode [IWMPLibraryServices :: getCountByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) , qui récupère le nombre de bibliothèques d’un type donné. Les types de bibliothèque sont définis par l’énumération [WMPLibraryType](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) . Cette énumération comprend une valeur pour la bibliothèque locale, wmpltLocal. Cela est dû au fait que la fonctionnalité des services de bibliothèque vous permet toujours de travailler avec la bibliothèque locale à l’aide de **IWMPLibraryServices** et des interfaces associées.

> [!Note]  
> L’énumération **WMPLibraryType** comprend la valeur wmpltRemote, qui représente les bibliothèques multimédias partagées par le réseau. Pour accéder à ces bibliothèques partagées, le contrôle du lecteur doit s’exécuter en mode distant. pour plus d’informations sur l’exécution du contrôle Player en mode distant, consultez communication à distance [du contrôle Lecteur Windows Media](remoting-the-windows-media-player-control.md).

 

Après avoir récupéré le nombre de bibliothèques, vous pouvez effectuer une itération dans la collection de bibliothèques disponibles en appelant à plusieurs reprises [IWMPLibraryServices :: getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) dans une boucle, en passant une nouvelle valeur d’index à chaque itération. Cette méthode récupère un pointeur vers une interface [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) , qui représente la bibliothèque individuelle.

Après avoir récupéré un pointeur vers **IWMPLibrary**, vous pouvez appeler [IWMPLibrary :: obtenir \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) pour récupérer un pointeur vers une interface **IWMPMediaCollection** . Avec ce pointeur d’interface, vous pouvez utiliser une bibliothèque individuelle de la même façon que vous utilisez la bibliothèque locale. Vous pouvez également récupérer une chaîne contenant le nom de la bibliothèque en appelant [IWMPLibrary :: obtenir le \_ nom](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name), ce qui est utile si vous devez afficher le nom de la bibliothèque pour l’utilisateur. Vous pouvez appeler [IWMPLibrary :: obtenir le \_ type](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) pour obtenir le **WMPLibraryType** d’une bibliothèque particulière.

Vous pouvez gérer l’événement [IWMPEvents3 :: LibraryConnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) pour savoir quand une bibliothèque devient disponible et l’événement [IWMPEvents3 :: LibraryDisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) savoir quand une bibliothèque se déconnecte. Chacun de ces événements fournit un pointeur **IWMPLibrary** qui représente la bibliothèque qui est connectée ou déconnectée. Vous pouvez appeler [IWMPLibrary :: isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) pour déterminer si la bibliothèque qui est connectée ou déconnectée est une bibliothèque que vous utilisez actuellement.

Il existe quelques différences importantes lorsque vous utilisez une bibliothèque récupérée par le biais de l’interface **IWMPLibraryServices** par rapport à l’utilisation d’une bibliothèque Récupérée à l’aide de [IWMPCore :: obtenir \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection). Les différences suivantes s’appliquent :

-   Vous pouvez généralement récupérer des résultats de requête beaucoup plus rapidement à partir des bibliothèques récupérées via **IWMPLibraryServices**. (Cela suppose que d’autres facteurs tels que les temps d’accès du réseau et du disque dur sont égaux).
-   La liste des attributs de métadonnées d’éléments multimédias disponibles à partir des bibliothèques récupérées via **IWMPLibraryServices** est généralement un sous-ensemble de ceux qui sont disponibles à partir de la bibliothèque locale récupérée via [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore).
-   Si vous récupérez la bibliothèque locale par le biais de **IWMPLibraryServices**, tous les mêmes attributs sont disponibles pour votre utilisation que ceux disponibles lorsque vous récupérez la bibliothèque locale par le biais de **IWMPCore**. Toutefois, vous serez en mesure de récupérer des résultats de requête beaucoup plus rapidement pour les attributs les plus couramment utilisés.
-   Vous devez utiliser des collections de chaînes pour créer des éléments d’interface utilisateur lorsque vous travaillez avec des bibliothèques récupérées par le biais de **IWMPLibraryServices**. Par exemple, [IWMPMediaCollection2 :: getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) vous permet d’utiliser une requête personnalisée (représentée par l’interface **IWMPQuery** ) pour récupérer une collection de chaînes.
-   Les bibliothèques distantes récupérées via l’interface **IWMPLibraryServices** peuvent ne pas toujours être connectées à l’instance actuelle du lecteur. Cela signifie qu’il est important de gérer les événements **LibraryConnect** et **LibraryDisconnect** pour savoir quand la disponibilité de la bibliothèque change, et pour gérer l’événement [IWMPEvents3 :: StringCollectionChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) de savoir quand des chaînes sont ajoutées ou supprimées dans les collections de chaînes que vous utilisez pour afficher les éléments de l’interface utilisateur. Vous devez également gérer les événements **StringCollectionChange** pour la bibliothèque locale pour des raisons similaires.

Il est important de comprendre que les collections de chaînes pour une bibliothèque particulière peuvent changer à tout moment. Une collection de chaînes peut être vide quand vous la récupérez pour la première fois, comme dans le cas d’une bibliothèque qui a été connectée récemment mais que le lecteur n’a pas encore énuméré son contenu. À l’inverse, une collection de chaînes peut déjà contenir toutes les informations dont vous avez besoin. Dans ce cas, vous risquez de ne jamais recevoir un événement **StringCollectionChange** , car le contenu de la bibliothèque a été complètement énuméré avant que vous n’ayez créé votre requête et rien d’autre ne change.

Par conséquent, pour maintenir à jour votre interface utilisateur, vous devez énumérer le contenu de la collection de chaînes lorsque vous récupérez l’interface **IWMPStringCollection** et gérer l’événement **StringCollectionChange** pour connaître les mises à jour lorsqu’elles se produisent.

## <a name="sample"></a>Exemple

L’exemple nommé WMPML montre comment utiliser les services de bibliothèque. pour plus d’informations sur les exemples du kit de développement logiciel (SDK) Lecteur Windows Media, consultez [exemples](samples.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos de la bibliothèque**](about-the-library.md)
</dt> <dt>

[**À propos de l’objet de requête**](about-the-query-object.md)
</dt> <dt>

[**Interface IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Interface IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
</dt> <dt>

[**Interface IWMPLibrary (VB et C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Interface IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
</dt> <dt>

[**Interface IWMPLibraryServices (VB et C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)
</dt> <dt>

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)
</dt> <dt>

[**Interface IWMPStringCollection (VB et C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
</dt> <dt>

[**Interface IWMPQuery (VB et C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Utilisation de la bibliothèque**](working-with-the-library.md)
</dt> </dl>

 

 




