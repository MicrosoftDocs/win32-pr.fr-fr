---
title: À propos de Windows Connect Now
description: Windows Connect Now (WCN) fournit un mécanisme simple et sécurisé pour les points d’accès réseau et les appareils (tels que les imprimantes, les appareils photo et les pc) pour se connecter et échanger des paramètres.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46e0acbf2d2eb728b0b62610040aaa08e06d466c5bbd5ab47237c46a8612ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593709"
---
# <a name="about-windows-connect-now"></a>À propos de Windows Connect Now

Windows Connect Now (WCN) fournit un mécanisme simple et sécurisé pour les points d’accès réseau et les appareils (tels que les imprimantes, les appareils photo et les pc) pour se connecter et échanger des paramètres. Cette API est l’implémentation Microsoft du protocole Wi-Fi Protected Setup (WPS)/Wi-Fi simple configuration (WSC), qui a été créé par l’Alliance Wi-Fi en tant que solution pour la mise en réseau à distance et les petites entreprises. Cette technologie n’est pas destinée aux scénarios d’entreprise.

> [!Note]  
> Le nom de la spécification a été modifié entre la version 1.0 h et la version 2. La spécification de la version 1.0 a était nommée Wi-Fi Protected Setup (WPS). À partir de la spécification de la version 2, la spécification est nommée Wi-Fi configuration simple (WSC). Dans notre documentation, les termes WPS et WSC sont utilisés indifféremment, sauf mention contraire.

 

Windows Connect Now permet aux applications de rechercher des appareils qui gèrent WCN à l’aide de l' [API de détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal). L’étendue d’une recherche peut être limitée à un SSID, un État, une catégorie ou même élargi pour inclure tous les appareils avec la compatibilité WCN. Une fois que les appareils sont localisés, l’API WCN autorise la communication avec l’appareil qui prend en charge WCN afin de faciliter la configuration ou la connectivité.

 

 