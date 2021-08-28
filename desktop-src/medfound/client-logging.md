---
description: En savoir plus sur la journalisation client pour Microsoft Media Foundation. La journalisation permet au serveur multimédia d’effectuer le suivi de l’activité des clients qui s’y connectent.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Journalisation du client (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3874c413f61b3495dc7e67f082a83e789a7a1357
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483085"
---
# <a name="client-logging-microsoft-media-foundation"></a>Journalisation du client (Microsoft Media Foundation)

La source réseau prend en charge la journalisation du client, ce qui permet au serveur multimédia d’effectuer le suivi de l’activité des clients qui s’y connectent. Les journaux du client permettent à un serveur d’enregistrer les statistiques de connexion, de rendu et de diffusion en continu. Ces journaux peuvent être utilisés par les fournisseurs de contenu dans divers scénarios, tels que, pour suivre l’utilisation du serveur multimédia et générer la facturation, ou pour fournir un contenu de qualité appropriée en fonction de la vitesse du réseau du client.

Un fichier journal contient plusieurs entrées d’événement client. Chaque entrée de journal contient un certain nombre de champs délimités par des espaces. Il existe deux types de journaux client : le *rendu* (lecture) et la *diffusion en continu* (réception). Étant donné que le contenu peut être lu et diffusé simultanément, le client peut envoyer une combinaison des deux types de données de journal. Dans certains cas, deux entrées de journal peuvent exister pour la même session. Par exemple, lorsque la mise en cache rapide est activée, le client peut finir de recevoir le contenu diffusé en continu avant de terminer son rendu. Dans ce cas, les données du journal de diffusion en continu sont envoyées avant les données du journal de rendu.

Le client envoie des données de journal au serveur lorsque le client passe d’un état de lecture (lecture, rapide ou rembobinage) à un état de non-lecture (arrêter, suspendre, terminer le flux et début du flux). Lorsque les données d’un journal de rendu sont soumises, une connexion est établie directement sur le serveur multimédia ou sur un serveur proxy configuré.

Si le contenu est stocké dans un fichier de cache local temporaire sur l’ordinateur qui exécute le client, le client peut lire un fichier à partir de son cache local et envoyer les données du journal de rendu pour indiquer qu’il a lu le contenu. Dans ce cas, le client lit un fichier à partir de son cache local, l’entrée du journal de rendu ne contient pas de statistiques réseau et le protocole est défini sur cache.

Le client envoie des données de journal de diffusion sur le serveur pour indiquer comment le client a reçu le contenu, mais pas comment il a été rendu. Le client peut envoyer le journal de diffusion en continu longtemps avant que le client n’ait terminé le rendu du contenu.

Cette rubrique ne fournit pas d’informations sur tous les champs de journal. pour obtenir une référence complète, consultez [Windows Structure de données du journal des médias](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).

## <a name="configuring-log-fields"></a>Configuration des champs du journal

Media Foundation permet au client de configurer la source réseau à l’aide de propriétés. L’application doit définir les propriétés appropriées dans une banque de propriétés et la passer à l’une des méthodes de programme de résolution source. Le programme de résolution source crée la source réseau comme demandé et ouvre une connexion avec le serveur. Si la connexion réussit, le client envoie des informations sur lui-même.

Le tableau suivant décrit les champs du journal et les propriétés correspondantes qu’une application peut définir par le biais du programme de résolution source. Ces informations ne changent pas au cours de la session.




| Champ de journalisation | Description | 
|---------------|-------------|
| c-playerid | Identification unique du joueur. Ces informations sont envoyées au début de la connexion. En général, il s’agit d’un GUID du client. Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> .<br /> Le client envoie ces informations au serveur au début de la connexion.<br /> Exemple de valeur : « {c579d042-CECC-11D1-bb31-00a0c9603954} »<br /> | 
| c-playerversion | Numéro de version du lecteur qui est envoyé au début de la connexion. Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> .<br /> Le client envoie ces informations au serveur au début de la connexion.<br /> | 
| CS (agent utilisateur) | Type de navigateur utilisé si le lecteur a été incorporé dans un navigateur. Cette valeur peut être définie par le client dans la propriété <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .<br /> Si le lecteur n’a pas été incorporé, ce champ fait référence à l’agent utilisateur du client qui a généré le journal. Dans ce cas, le client doit définir la propriété <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .<br /> Le client envoie ces informations au serveur au début de la connexion.<br /> Exemple de valeur : « Mozilla/4.0 _ (compatible ; _MSIE_4.01 ; _Windows_98) »<br /> | 
| CS (référant) | URL de la page Web dans laquelle le lecteur a été incorporé (s’il a été incorporé). Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> .<br /> Le client envoie ces informations au serveur à la fin de la connexion.<br /> Exemple de valeur : " https://www.example.microsoft.com "<br /> | 
| c-hostexe | Pour les entrées de journal du lecteur, le programme hôte (.exe) qui a été exécuté. par exemple, une page web dans un navigateur, une applet Microsoft Visual Basic ou un lecteur autonome. Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> .<br /> Le client envoie ces informations au serveur à la fin de la connexion.<br /> Exemples de valeurs :<br /><ul><li>« iexplore.exe »</li><li>« myplayer.exe »</li></ul> | 
| c-hostexever | Numéro de version du programme hôte (.exe). Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> .<br /> Le client envoie ces informations au serveur à la fin de la connexion.<br /> | 




 

L’exemple de code suivant montre comment une application cliente configure la source réseau. Cet exemple définit le champ de Journal « c-hostexe ».


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a>Récupération des statistiques réseau

Lorsque l’application appelle l’une des méthodes de résolution de source, elle crée la source réseau, définit les propriétés spécifiées dans la Banque de propriétés et ouvre une session avec le serveur multimédia. Outre les informations configurables décrites dans la section précédente, les données supplémentaires sont transférées entre le serveur et le client au début de la session, pendant la diffusion en continu et lorsque la session est fermée.

L’application peut récupérer des statistiques réseau à l’aide de l’identificateur de service **MFNETSOURCE \_ Statistics \_ service** . Pour utiliser ce service, l’application peut appeler la fonction [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer la Banque de propriétés qui contient les statistiques réseau dans la propriété [**MFNETSOURCE \_ Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) . Des valeurs spécifiques peuvent être récupérées en fournissant l’identificateur correspondant défini dans l’énumération **MFNETSOURCE \_ Statistics \_ ID** .

L’exemple de code suivant montre comment utiliser le service pour récupérer le nombre de paquets reçus par le client.


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



La liste suivante décrit certains identificateurs de statistiques réseau définis dans [**MFNETSOURCE \_ Statistics \_ ID**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).



| Identificateur des statistiques réseau              | Description                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ID AVGBANDWIDTHBPS \_ MFNETSOURCE**       | Bande passante moyenne (en bits par seconde) à laquelle le client a été connecté au serveur. La valeur est calculée sur toute la durée de la connexion.                                                              |
| **\_ID BUFFERINGCOUNT \_ MFNETSOURCE**        | Nombre de fois où le client met en mémoire tampon lors de la diffusion du flux.                                                                                                                                                              |
| **\_ID BYTESRECEIVED \_ MFNETSOURCE**         | Nombre d’octets reçus par le client à partir du serveur. La valeur n’inclut aucune surcharge ajoutée par la pile réseau. Le même contenu diffusé en continu à l’aide de différents protocoles peut aboutir à des valeurs différentes. |
| **\_ID LINKBANDWIDTH \_ MFNETSOURCE**         | Bande passante disponible maximale du client en bits par seconde.                                                                                                                                                              |
| **\_ID LOSTPACKETS \_ MFNETSOURCE**           | Nombre de paquets envoyés par le serveur mais perdus pendant la transmission et jamais joués par le client. La valeur n’inclut pas les paquets TCP ou UDP.                                                                          |
| **\_ID RECVPACKETS \_ MFNETSOURCE**           | Nombre de paquets reçus à partir du serveur la valeur n’inclut pas les paquets TCP ou UDP.                                                                                                                                  |
| **\_ID RECOVEREDBYECCPACKETS \_ MFNETSOURCE** | Paquets perdus sur le réseau qui ont été réparés et récupérés au niveau de la couche client. Cette valeur n’inclut pas les paquets TCP ou UDP.                                                                                          |
| **\_ID RESENDSREQUESTED \_ MFNETSOURCE**      | Nombre de demandes effectuées par le client pour recevoir de nouveaux paquets. Cette valeur n’inclut pas les paquets TCP ou UDP.                                                                                                          |
| **\_ID RECOVEREDPACKETS \_ MFNETSOURCE**      | Nombre de paquets récupérés, car ils ont été renvoyés via UDP. Cette valeur n’inclut pas les paquets TCP ou UDP. Ce champ contient un zéro, sauf si le client utilise le renvoi UDP.                                        |
| **\_ID BUFFERPROGRESS \_ MFNETSOURCE**        | Pourcentage de la mémoire tampon de diffusion rempli pendant la mise en mémoire tampon.                                                                                                                                                              |
| **\_ID de protocole MFNETSOURCE \_**              | Protocole utilisé pour accéder au flux. Cela peut différer du protocole demandé par le client.                                                                                                                             |
| **\_ID de transport MFNETSOURCE \_**             | Protocole de transport utilisé pour remettre le flux. Il doit s’agir du protocole UDP ou TCP.                                                                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités de la source réseau](network-source-features.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

