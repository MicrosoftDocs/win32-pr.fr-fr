---
title: Journalisation des données de flux
description: Journalisation des données de flux
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Windows Sélections de métafichiers multimédia, journalisation des données de flux
- sélections, journalisation des données de flux
- sélections de métafichiers, journalisation des données de flux
- Windows Sélections de métafichiers multimédia, journalisation des données de flux
- sélections, journalisation des données de flux
- sélections de métafichiers, journalisation des données de flux
- journalisation des données de flux
- journalisation des données de flux
- Lecteur Windows Media, journalisation des données de flux
- Lecteur Windows Media, journalisation des données de flux
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919223"
---
# <a name="logging-stream-data"></a>Journalisation des données de flux

Les informations journalisées peuvent être acquises et utilisées pour déterminer le comportement de la visionneuse, par exemple, la fréquence à laquelle un flux est affiché, ou si un utilisateur spécifique a affiché un flux et la durée de la qualité.

Les informations de journalisation sont automatiquement envoyées au serveur d’origine de la sélection. Vous pouvez également envoyer des informations de journalisation à des serveurs supplémentaires, y compris des serveurs Web que vous utilisez exclusivement pour la journalisation. Pour ce faire, utilisez l’élément **LOGURL** , en spécifiant une URL valide pour l’attribut **href** . Vous pouvez inclure des éléments **LOGURL** comme enfants de l’élément **ASX** et comme enfants d’éléments d' **entrée** individuels. Lorsque la sélection est ouverte pour la première fois, les informations de journalisation sont envoyées au serveur d’origine et à chaque URL spécifiée dans **LOGURL** Children de l’élément **ASX** . Ensuite, lorsque chaque entrée est atteinte, les informations de journalisation spécifiques à cette entrée sont envoyées à chaque URL spécifiée dans **LOGURL** Children de l’élément **entry** .

le kit de développement logiciel (SDK) Windows Media Format prend en charge l’élément **LOGURL** via l’interface **IWMSReaderNetworkConfig** et les méthodes suivantes :


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



En plus des informations qui sont journalisées automatiquement, une sélection de métafichiers peut consigner des informations personnalisées à l’aide de l’élément **param** . Pour utiliser l’élément **param** de cette manière, définissez l’attribut **Name** sur « log : » suivi d’un nom de champ de journal et d’un espace de noms XML facultatif, séparé du nom de champ par un autre signe deux-points («  : »). Tout ce qui suit le deuxième signe deux-points est traité comme un espace de noms, donc le nom du champ ne doit pas contenir de deux-points.

Le champ de journal spécifié dans l’attribut **Name** est défini sur la valeur de l’attribut **value** . Si le journal ne contient pas déjà un champ portant le nom spécifié, il sera ajouté.

**Exemple de code**


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




