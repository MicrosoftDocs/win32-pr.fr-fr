---
description: Les fonctionnalités multimédias sont différentes avec TAPI 2,2 (TAPI/C) par opposition à TAPI 3 (COM), principalement parce que l’API COM a accès aux fournisseurs de services multimédias (MSP).
ms.assetid: 73042eb1-b2d6-4dcb-b40e-f8f3933dcdb0
title: Accès aux supports
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f2fc67e18a85718a10a0489656d4b423dd2f9f849a876ea5eec0543017611f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575609"
---
# <a name="media-access"></a>Accès aux supports

Les fonctionnalités multimédias sont différentes avec TAPI 2,2 (TAPI/C) par opposition à TAPI 3 (COM), principalement parce que l’API COM a accès aux fournisseurs de services multimédias (MSP). Pour plus d’informations sur les MSP, voir [à propos du fournisseur de services de média (MSP)](./about-the-media-service-provider-msp-.md). Pour plus d’informations sur les opérations de flux de données multimédia, consultez [Media Control](./device-control.md).

Les deux concepts les plus importants pour une application sont le type de média (ou le mode) et le flux. Le type est le formulaire dans lequel les données sont transmises. Pour plus d’informations et pour obtenir la liste des types définis par TAPI, consultez [ \_ constantes LINEMEDIAMODE](linemediamode--constants.md). Le flux multimédia est le flux de données réel. Un MSP peut fournir un accès direct au flux. Les applications TAPI 2,2 ont un accès, mais référencent principalement d’autres API pour implémenter ces contrôles.

Ces API incluent l’API Waveform, l’API comm et l’interface MCI (Media Control Interface). L’API Waveform est utilisée pour la programmation multimédia, l’API comm est l’ensemble de fonctions de communication fourni par le kit de développement logiciel (SDK) de la plateforme, et la MCI fournit une interface généralisée de haut niveau pour le contrôle des appareils multimédias.

Par exemple, pour les appareils de ligne, une application peut utiliser TAPI 2,2 pour établir une connexion à une autre station. Une fois la connexion établie, l’application peut ensuite utiliser l’API Waveform (ou l’API WaveAudio MCI) sur l’appareil associé pour lire (envoyer) et enregistrer (recevoir) des données audio sur la connexion. De même, si le flux de média de connexion provient d’un modem, une application utilise les extensions de configuration de modem de l’API de communication pour contrôler le flux de média.

Pour fournir à TAPI 2,2 un accès multimédia en continu à un téléphone ou à un appel sur un appareil de ligne, le fournisseur de services doit implémenter à la fois le SPI de téléphonie et le SPI de flux de média approprié ou l’interface de pilote de périphérique (DDI). Le fournisseur de services peut prendre en charge les lignes et les téléphones simultanément.

Étant donné que ces classes d’appareils et opérations de flux de média fonctionnent indépendamment les unes des autres, la coordination de leur utilisation doit se produire au niveau de l’application. Plusieurs applications qui partagent des appels et des flux multimédias auront probablement besoin d’une coordination de leurs activités au niveau de l’application pour empêcher l’utilisation en conflit de l’interface TAPI et de l’API de flux multimédia.

L’interface TAPI signale les modifications apportées au type de flux multimédia (voix, télécopie, modem de données, etc.) dans les applications participantes. Ce processus est parfois appelé « [*classification des appels*](c-tapgloss.md)». Le mécanisme utilisé pour déterminer le type de flux multimédia est spécifique au fournisseur de services. Par exemple, un fournisseur de services peut filtrer le flux multimédia pour l’énergie ou les tonalités qui caractérisent le type de support, ou il peut utiliser la sonnerie distinctive, les données échangées dans les messages sur le réseau ou la connaissance de l’appelant ou de l’ID appelé pour effectuer cette détermination.

-   [Surveillance des appels](call-monitoring.md)
-   [Contrôle multimédia](/previous-versions/windows/desktop/legacy/ms736578(v=vs.85))
-   [Collecte des chiffres](digit-gathering.md)
-   [Génération de chiffres et de tonalités inbande](generating-inband-digits-and-tones.md)

 

 
