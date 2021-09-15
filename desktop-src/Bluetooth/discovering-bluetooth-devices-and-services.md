---
title: Détection des appareils et services Bluetooth
description: pour faciliter la découverte des appareils et des services Bluetooth, Windows mappe le protocole SDP (Service discovery Protocol) Bluetooth sur les interfaces d’espace de noms Windows sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tâches, détection des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414029"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Détection des appareils et services Bluetooth

pour faciliter la découverte des appareils et des services Bluetooth, Windows mappe le protocole SDP (Service discovery Protocol) Bluetooth sur les interfaces d’espace de noms Windows sockets. Les fonctions principales utilisées pour ce mappage sont les fonctions [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)et [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) . La structure [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) est également utilisée conjointement avec ces fonctions.

étant donné que certains concepts et paramètres du Bluetooth SDP ne sont pas nécessairement mappés directement dans la structure [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) , vous devez être attentif à la façon dont ses membres sont créés et utilisés. pour de nombreuses opérations de Bluetooth complexes, telles que la création d’enregistrements SDP, le membre **lpBlob** du **WSAQUERYSET** est utilisé. lorsqu’une telle considération particulière est nécessaire, elle est spécifiquement décrite, par exemple dans les pages de référence, telles que [**Bluetooth et WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), entre autres.

Il est important de comprendre que l’inscription SDP est distincte du contrôle Socket. quand une application serveur est préparée à accepter la connexion cliente, elle doit appeler la fonction [**WSASetService**](bluetooth-and-wsasetservice.md) pour inscrire un Bluetooth enregistrement SDP qui correspond à ce service. cette Bluetooth application doit rappeler la fonction **WSASetService** avant de fermer, pour annuler l’inscription de l’enregistrement SDP Bluetooth.

Lorsque vous utilisez les fonctions de mappage décrites sur cette page, l' \_ espace de noms NS BTH est assigné.

Pour plus d’informations sur la découverte des appareils et des services, consultez les pages de référence suivantes :

-   [**Bluetooth et WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth et WSALookupServiceBegin pour la consultation des appareils**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth et WSALookupServiceBegin pour la détection de Service**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth et WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth et WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth et objet BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth et WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

vous pouvez également télécharger l’exemple de [connexion Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) pour obtenir un exemple complet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bluetooth programmation avec des sockets Windows](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[exemple de connexion Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




