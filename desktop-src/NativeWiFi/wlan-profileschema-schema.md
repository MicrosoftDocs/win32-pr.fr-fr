---
description: Définit un profil de réseau local sans fil utilisé par le service de configuration automatique WiFi natif.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: Schéma WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91bd1a5d04bcc265f2b9ba7c0533bb0beb4e2c861f01c8b5e286d59f8b4bcfc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619066"
---
# <a name="wlan_profile-schema"></a>\_Schéma de profil WLAN

Le \_ schéma de profil WLAN définit un profil de réseau local sans fil utilisé par le service de configuration automatique WiFi natif.

Le service de configuration automatique accepte les profils sans fil de l’agent stratégie de groupe, de l’interface de script (**netsh**), de l’interface utilisateur ou de l’interface de configuration flash USB.

Un profil reçu à partir de l’un de ces systèmes est mappé au \_ schéma de profil WLAN et stocké dans le magasin de profils. Les profils peuvent être exportés à partir du magasin de profils à l’aide des commandes netsh ou à l’aide d’éléments d’API tels que [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).

L’élément racine d’un profil WLAN est l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) . Chaque profil aura un seul élément racine. L’élément **WLANProfile** est dans l’espace de noms `https://www.microsoft.com/networking/WLAN/profile/v1` .

Pour afficher des exemples de profils WLAN, consultez la page exemples de profils [sans fil](wireless-profile-samples.md).

-   [\_Éléments de schéma de profil WLAN](wlan-profileschema-elements.md)
-   [\_Types simples de schéma de profil WLAN](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
