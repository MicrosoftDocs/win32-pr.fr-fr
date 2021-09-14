---
title: Création du document ServiceInfo de manière dynamique
description: Création du document ServiceInfo de manière dynamique
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Lecteur Windows Media des magasins en ligne, création d’un document ServiceInfo
- magasins en ligne, créer un document ServiceInfo
- tapez 1 magasins en ligne, création d’un document ServiceInfo
- type 2 magasins en ligne, création d’un document ServiceInfo
- Lecteur Windows Media des magasins en ligne, créer dynamiquement un document ServiceInfo
- magasins en ligne, créer dynamiquement un document ServiceInfo
- tapez 1 magasins en ligne, en créant dynamiquement le document ServiceInfo
- tapez 2 magasins en ligne, en créant dynamiquement le document ServiceInfo
- Lecteur Windows Media les magasins en ligne, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- création dynamique d’un document ServiceInfo
- création du document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90159e72046536cf6b69521586a0640935478eb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919255"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>Création du document ServiceInfo de manière dynamique

Vous pouvez utiliser ASP pour créer votre document ServiceInfo. Cela peut vous offrir une plus grande flexibilité dans votre boutique en ligne en utilisant les techniques suivantes :

-   Génération dynamique du nom d’hôte pour les URL.
-   Modification des URL pour la localisation basée sur les paramètres régionaux et GeoId.
-   Ajout dynamique des paramètres de chaîne de requête de l’URL ServiceInfo à d’autres URL, telles que l’URL de la page de navigation.

L’exemple de code suivant montre une page ASP simple qui crée dynamiquement un document ServiceInfo :


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



L’exemple de code précédent utilise ASP pour récupérer le nom d’hôte du serveur Web et créer dynamiquement les URL dans le document. Le code récupère également le paramètre de chaîne de requête *locale* à partir de la demande serviceInfo et l’ajoute à l’URL de la page Navigate.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Navigation pour les magasins de type 2 en ligne**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**Document ServiceInfo pour une boutique en ligne de type 1**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Document ServiceInfo pour un magasin de type 2 en ligne**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




