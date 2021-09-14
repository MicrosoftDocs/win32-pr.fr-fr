---
title: Paramètres réseau par défaut
description: Paramètres réseau par défaut
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media Format SDK, paramètres de mise en réseau par défaut
- ASF (Advanced Systems Format), paramètres de mise en réseau par défaut
- ASF (format des systèmes avancés), paramètres de mise en réseau par défaut
- Windows Media Format SDK, paramètres de mise en réseau
- ASF (Advanced Systems Format), paramètres de mise en réseau
- ASF (format des systèmes avancés), paramètres de mise en réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226009"
---
# <a name="default-networking-settings"></a>Paramètres réseau par défaut

les tableaux suivants décrivent les paramètres par défaut des paramètres de mise en réseau dans le kit de développement logiciel (SDK) de Format multimédia Windows, regroupés par interface.



| IWMReaderNetworkConfig                | Paramètre par défaut              |
|---------------------------------------|------------------------------|
| Temps de mise en mémoire tampon                        | 5 secondes                    |
| UseFixedUDPPort                       | FALSE                        |
| FixedUDPPort                          | 0 (non valide)                |
| ProxySetting : HTTP                    | \_navigateur des \_ paramètres \_ proxy WMT |
| ProxySetting : MMS                     | \_paramètre de proxy WMT \_ \_ aucun    |
| ProxySetting : RTSP                    | \_paramètre de proxy WMT \_ \_ aucun    |
| ProxyHostName (HTTP, MMS, RTSP)       | ""                           |
| ProxyPort : HTTP                       | 80                           |
| ProxyPort : MMS                        | 1755                         |
| ProxtPort : RTSP                       | 554                          |
| ProxyExceptionList (HTTP, MMS, RTSP)  | ""                           |
| ProxyBypassForLocal (HTTP, MMS, RTSP) | FALSE                        |
| ForceRerunAutoDetection               | FALSE                        |
| EnableMulticast                       | TRUE                         |
| EnableHTTP                            | TRUE                         |
| EnableTCP                             | TRUE                         |
| EnableUDP                             | TRUE                         |
| Bande passante de connexion                  | 0 (détection automatique)              |



 



| IWMReaderNetworkConfig2        | Paramètre par défaut        |
|--------------------------------|------------------------|
| Durée de diffusion en continu accélérée | 100 millions (10 secondes) |
| Activer la mise en cache du contenu         | TRUE                   |
| Activer le cache rapide              | TRUE                   |
| Activer les renvois                 | TRUE                   |
| Activer le réglage de la largeur du contenu        | TRUE                   |
| Limite de reconnexion                | 25                     |



 



| IWMWriterNetworkSink | Paramètre par défaut         |
|----------------------|-------------------------|
| Nombre maximum de clients      | 5                       |
| Protocole réseau     | 0 ( \_ protocole WMT \_ http) |
| URL de l’hôte             | 0 (non valide)           |



 



| IWMWriterAdvanced2  | Paramètre par défaut             |
|---------------------|-----------------------------|
| Taille maximale des paquets | 1400                        |
| ID de client du journal       | FALSE                       |
| Mode de lecture           | \_sélection d' \_ autosélectionner le mode de lecture WMT \_ |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation des fonctionnalités réseau**](implementing-network-functionality.md)
</dt> </dl>

 

 




