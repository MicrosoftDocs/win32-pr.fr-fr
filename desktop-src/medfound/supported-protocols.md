---
description: Protocoles pris en charge
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocoles pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753837"
---
# <a name="supported-protocols"></a>Protocoles pris en charge

Media Foundation prend en charge les protocoles suivants :

-   Protocole RTSP (Real Time Streaming Protocol)

    RTSP est principalement utilisé pour la diffusion en continu de contenu multimédia. Il peut utiliser UDP ou TCP comme protocoles de transport. Le protocole UDP est le plus efficace pour la distribution de contenu, car la surcharge de bande passante est inférieure à celle des protocoles basés sur TCP. Même si le protocole TCP garantit la remise fiable des paquets, TCP n’est pas adapté aux flux de médias numériques, où l’utilisation efficace de la bande passante est plus importante que les paquets perdus occasionnellement.

-   Hypertext Transfer Protocol (HTTP)

    HTTP utilise TCP et est utilisé par les serveurs Web. Le schéma « httpd:// » indique que la source peut être téléchargée à partir d’un serveur Web. Le protocole HTTP est également utilisé dans le cas de pare-feu, qui sont généralement configurés pour accepter les requêtes HTTP et rejetent généralement d’autres protocoles de diffusion en continu.

L’application peut récupérer les protocoles pris en charge par Media Foundation à l’aide de l’interface [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) . Pour ce faire, l’application doit d’abord récupérer le nombre de protocoles, en appelant [**IMFNetSchemeHandlerConfig :: GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) , puis obtenir le type de protocole en fonction de l’index en appelant [**IMFNetSchemeHandlerConfig :: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype). Cette méthode retourne l’une des valeurs définies dans l’énumération de [**\_ \_ type de protocole MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .

L’application peut également récupérer les schémas pris en charge par le programme de résolution source en appelant la fonction [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .

## <a name="protocol-rollover"></a>Substitution de protocole

Lorsqu’une application spécifie « mms:// » comme schéma d’URL, le programme de résolution source effectue une opération de *substitution de protocole* . Dans ce processus, le programme de résolution source détermine le meilleur protocole pour la source réseau à utiliser pour obtenir le contenu. En général, pour la diffusion de contenu multimédia, RTSP avec UDP (RTSP) est plus efficace que HTTP. Toutefois, si le contenu est hébergé sur un serveur Web, le protocole HTTP est un meilleur choix.

La substitution de protocole peut également se produire lorsqu’une tentative d’utilisation du protocole spécifié dans le schéma d’URL échoue. Par exemple, un protocole peut échouer lorsqu’un pare-feu bloque les paquets UDP. Dans ce cas, le programme de résolution source bascule vers HTTP.

La substitution de protocole ne s’applique pas si le schéma d’URL contient un protocole spécifique, tel que « rtspu:// ». En outre, la substitution n’est pas effectuée si l’authentification échoue ou si le serveur a atteint une limite de connexions client. Il est recommandé que les applications spécifient le schéma « mms:// » et autorisent le programme de résolution source à sélectionner le meilleur protocole pour le scénario.

Le tableau suivant répertorie l’ordre de substitution.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Schémas autorisés</th>
<th>Ordre de substitution des protocoles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>mms://ou rtsp://</td>
<td>Mise en cache rapide activée :<br/>
<ol>
<li>RTSP avec TCP (RTSPt)<br/></li>
<li>RTSP avec UDP (RTSP)<br/></li>
<li>Streaming HTTP<br/></li>
<li>Téléchargement HTTP (HTTPD)<br/></li>
</ol>
Mise en cache rapide désactivée :<br/>
<ol>
<li>RTSP<br/></li>
<li>RTSPt<br/></li>
<li>Streaming HTTP<br/></li>
<li>Téléchargement HTTP<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>rtspu://</td>
<td>RTSP</td>
</tr>
<tr class="odd">
<td>rtspt://</td>
<td>RTSPt</td>
</tr>
<tr class="even">
<td>https://</td>
<td><ol>
<li>HTTP<br/></li>
<li>HTTPD<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>httpd://</td>
<td>HTTPD</td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a>Récupération du protocole en cours

Après une opération de substitution de protocole, la source réseau peut utiliser un autre protocole que celui spécifié par l’application dans le schéma d’URL. Le résultat de substitution de protocole est disponible pour l’application une fois que la source réseau a établi la connexion avec le serveur multimédia.

Pour obtenir le protocole et le transport utilisés pour obtenir le contenu, l’application peut récupérer les valeurs de propriété pour la propriété de [ \_ protocole MFNETSOURCE](mfnetsource-protocol-property.md) et la propriété de [ \_ transport MFNETSOURCE](mfnetsource-transport-property.md) d’un objet **IPropertyStore** à partir de la source réseau.

Le code suivant montre comment récupérer ces valeurs.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



Dans l’exemple de code précédent, **IPropertyStore :: GetValue** récupère la \_ valeur de protocole MFNETSOURCE, qui est un membre de l’énumération de [**\_ \_ type de protocole MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) . Pour le \_ transport MFNETSOURCE, la valeur est un membre de l’énumération du [**\_ \_ type de transport MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .

L’application peut également récupérer les mêmes valeurs à l’aide du service MFNETSOURCE \_ Statistics \_ service. Pour utiliser ce service, l’application peut appeler la fonction [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer la Banque de propriétés à partir de la source réseau. Cette banque de propriétés contient des statistiques réseau dans la propriété [MFNETSOURCE \_ Statistics](mfnetsource-statistics-property.md) . Les valeurs de protocole et de transport peuvent être récupérées en spécifiant \_ l’ID de protocole MFNETSOURCE \_ et \_ \_ l’ID de transport MFNETSOURCE, définis dans l’énumération des [**\_ \_ ID de statistiques MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) . Le code suivant montre comment récupérer les valeurs de protocole et de transport à l’aide du \_ service MFNETSOURCE Statistics \_ service.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a>Activation et désactivation des protocoles

L’application peut configurer la source réseau afin que certains protocoles soient ignorés pendant le processus de substitution. Pour ce faire, les propriétés de la source réseau sont utilisées pour désactiver des protocoles spécifiques. Le tableau suivant présente les propriétés et les protocoles qu’ils contrôlent.



| Propriété                                                                    | Description                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE \_ activer \_ http](mfnetsource-enable-http-property.md)           | Active ou désactive les protocoles HTTP et HTTPD.         |
| [MFNETSOURCE \_ activer \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Active ou désactive RTSP et RTSPt.        |
| [MFNETSOURCE \_ activer \_ TCP](mfnetsource-enable-tcp-property.md)             | Active ou désactive le protocole RTSPt.                  |
| [MFNETSOURCE \_ activer \_ UDP](mfnetsource-enable-udp-property.md)             | Active ou désactive RTSP.                  |
| [MFNETSOURCE \_ activer le \_ Téléchargement](mfnetsource-enable-download-property.md)   | Active ou désactive le HTTPD.                  |
| [MFNETSOURCE \_ activer la \_ diffusion en continu](mfnetsource-enable-streaming-property.md) | Active ou désactive RTSP, RTSPt et HTTP. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




