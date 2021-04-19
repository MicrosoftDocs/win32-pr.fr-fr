---
title: Détection des appareils et services Bluetooth
description: Pour faciliter la découverte des appareils et services Bluetooth, Windows mappe le protocole de détection de service Bluetooth (SDP) sur les interfaces d’espace de noms Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tâches, détection des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "106527554"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Détection des appareils et services Bluetooth

Pour faciliter la découverte des appareils et services Bluetooth, Windows mappe le protocole de détection de service Bluetooth (SDP) sur les interfaces d’espace de noms Windows Sockets. Les fonctions principales utilisées pour ce mappage sont les fonctions [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)et [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) . La structure [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) est également utilisée conjointement avec ces fonctions.

Étant donné que certains concepts et paramètres du SDP Bluetooth ne sont pas nécessairement mappés directement dans la structure [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) , vous devez faire attention à la façon dont les membres sont créés et utilisés. Pour de nombreuses opérations Bluetooth complexes, telles que la création d’enregistrements SDP, le membre **lpBlob** du **WSAQUERYSET** est utilisé. Lorsqu’une telle considération particulière est nécessaire, elle est spécifiquement décrite, par exemple dans les pages de référence telles que [**Bluetooth et WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), entre autres.

Il est important de comprendre que l’inscription SDP est distincte du contrôle Socket. Quand une application serveur est préparée à accepter la connexion cliente, elle doit appeler la fonction [**WSASetService**](bluetooth-and-wsasetservice.md) pour inscrire un enregistrement SDP Bluetooth qui correspond à ce service. Cette application Bluetooth doit rappeler la fonction **WSASetService** avant de fermer, pour annuler l’inscription de l’enregistrement SDP Bluetooth.

Lorsque vous utilisez les fonctions de mappage décrites sur cette page, l' \_ espace de noms NS BTH est assigné.

Pour plus d’informations sur la découverte des appareils et des services, consultez les pages de référence suivantes :

-   [**Bluetooth et WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth et WSALookupServiceBegin pour la consultation des appareils**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth et WSALookupServiceBegin pour la détection de service**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth et WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth et WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth et objet BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth et WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

Vous pouvez également télécharger l' [exemple de connexion Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) pour obtenir un exemple complet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Programmation Bluetooth avec Windows Sockets](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Exemple de connexion Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




