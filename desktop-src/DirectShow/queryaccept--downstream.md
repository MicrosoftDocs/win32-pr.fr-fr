---
description: QueryAccept (en aval)
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: QueryAccept (en aval)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ec5c26209839f0dcd8351cc9a7ca84227faa2289d44d46c2c321fce0429e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747732"
---
# <a name="queryaccept-downstream"></a>QueryAccept (en aval)

Ce mécanisme permet à une broche de sortie de proposer un nouveau format à son homologue en aval. Le nouveau format ne doit pas nécessiter une plus grande taille de mémoire tampon. La broche de sortie effectue les opérations suivantes :

1.  Appelle [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) ou [**IPinConnection ::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) sur le code confidentiel en aval, pour vérifier si l’autre code confidentiel peut accepter le nouveau type de média (Voir l’illustration, étape A).
2.  Si la valeur de retour de l’étape 1 est \_ OK, le code PIN attache le type de média à l’exemple suivant. Pour ce faire, il appelle d’abord [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) pour obtenir l’exemple (B). Ensuite, il appelle [**IMediaSample :: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) pour attacher le type de média à cet exemple (C). En attachant le type de média à l’exemple, le filtre indique que le format a changé, en commençant par cet exemple.
3.  Le code PIN livre l’exemple (D).
4.  Lorsque le filtre en aval reçoit l’exemple, il appelle [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) pour récupérer le nouveau type de média.

    ![queryaccept (en aval)](images/dynformat3.png)

Tous les codes PIN prennent en charge la `QueryAccept` méthode. Toutefois, cette méthode est légèrement ambiguë, car une valeur de retour de S \_ OK ne garantit pas toujours que vous pouvez modifier le format lorsque le graphique est actif. Certains filtres peuvent retourner S \_ OK mais rejeter la modification si le graphique est actif. La méthode **DynamicQueryAccept** , qui est prise en charge par certaines broches d’entrée, définit explicitement \_ les S OK pour signifier que le code confidentiel peut changer de format pendant qu’il est actif. Si une broche d’entrée prend en charge l’interface **IPinConnection** , vous devez appeler **DynamicQueryAccept** plutôt que `QueryAccept` .

Dans la plupart des cas, ce mécanisme n’autorise pas les modifications radicales du format, telles que la modification de la profondeur de bit. Une situation dans laquelle il peut être utilisé est lorsqu’un décodeur vidéo change de palette. Les détails de base du format restent les mêmes, tels que les dimensions d’image et la profondeur de bits, mais le nouveau type de média a un ensemble différent d’entrées de palette.

**Note d’implémentation**

dans les classes de base DirectShow, [**CBasePin :: QueryAccept**](cbasepin-queryaccept.md) appelle la méthode **CheckMediaType** , qui est également appelée pendant la connexion du pin initial. Dans le cas d’un filtre de transformation, la méthode **CheckMediaType** du code confidentiel d’entrée doit toujours vérifier si la broche de sortie est connectée, et si tel est le cas, si le type de média d’entrée est compatible avec le type de média de sortie. Par conséquent, cette implémentation sera probablement valide pour `QueryAccept` . Si ce n’est pas le cas, vous devez remplacer afin `QueryAccept` d’effectuer les vérifications supplémentaires nécessaires. Notez également que la classe [**CTransformFilter**](ctransformfilter.md) encapsule cette logique dans les méthodes **CheckInputType** et **CheckTransform** . En revanche, la classe [**CTransInPlaceFilter**](ctransinplacefilter.md) appelle toujours `QueryAccept` sur le filtre en amont ou en aval suivant.

La méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) vérifie la présence d’un type de média sur l’exemple entrant et, le cas échéant, appelle **CheckMediaType**. Toutefois, il ne met pas à jour le membre **m \_ MT** du pin, qui contient le type de média actuel. Lorsque votre filtre traite l’exemple, vous devez vérifier l’exemple pour un type de média. S’il existe un nouveau type, vous devrez probablement le stocker en appelant **SetMediaType** sur votre code confidentiel ou en définissant la valeur de **m \_ MT** directement. En revanche, la classe [**CVideoTransformFilter**](cvideotransformfilter.md) , conçue pour les filtres de transformation vidéo, stocke le type de média lorsqu’il change. pour plus d’informations, consultez le code source de [**CVideoTransformFilter :: Receive**](cvideotransformfilter-receive.md) dans la bibliothèque de classes de base DirectShow.

Dans certains cas, vous pouvez simplement passer l' `QueryAccept` appel en aval, puis attacher le type de média à l’exemple de sortie et laisser le filtre en aval gérer le changement de format.

 

 



