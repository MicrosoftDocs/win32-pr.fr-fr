---
description: Lorsqu’un appel est à l’État connected, les données peuvent être transmises via l’appel. Le type de média d’appel fournit une indication du type de données (par exemple, son type de données ou un protocole de niveau supérieur) de ce flux de données multimédia.
ms.assetid: 3281387e-3f72-4fda-8199-b3ce6e45e910
title: Surveillance des médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa29b26e422ecbb3f1cf66ce0babfee1147508ad8c42da20c5340793460d1c08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863079"
---
# <a name="media-monitoring"></a>Surveillance des médias

Lorsqu’un appel est à l’état *Connected* , les données peuvent être transmises via l’appel. Le type de média d’appel fournit une indication du type de données (par exemple, son type de données ou un protocole de niveau supérieur) de ce flux de données multimédia.

L’interface TAPI permet aux applications d’être fournies avec une notification concernant les modifications apportées au type de média d’un appel. La notification fournit une indication du nouveau type de média de l’appel. Le fournisseur de services décide de la manière dont il souhaite effectuer cette détermination. Par exemple, le fournisseur de services peut utiliser le traitement de signal du flux multimédia pour déterminer le type de média, ou il peut s’appuyer sur des modèles de sonnerie distinctifs affectés à différents flux multimédias ou sur des éléments d’information transmis dans un protocole de signalisation hors bande. Indépendamment de la façon dont la détermination du type de média est effectuée, l’application est simplement informée des modifications de type de média sur un appel existant.

Pour plus d’informations et pour obtenir la liste des modes ou types de médias TAPI actuellement définis, consultez [ \_ constantes LINEMEDIAMODE](linemediamode--constants.md). Les fournisseurs de services peuvent implémenter des types de médias spécifiques au fournisseur pour des appareils hautement spécialisés. Pour plus d’informations, consultez la documentation de l’appareil.

Les types de média définis par TAPI sont les suivants :

-   Inconnu. Le type de média de l’appel n’est pas actuellement connu : l’appel n’est pas classifié.
-   Voix interactive. L’énergie vocale a été détectée lors de l’appel, et l’appel est traité comme un appel vocal interactif avec une personne à la fin de l’application.
-   Voix automatique. L’énergie vocale a été détectée lors de l’appel, et l’appel est traité comme un appel vocal, mais sans personne à l’extrémité de l’application, par exemple avec une application de machine de réponse.
-   Modem de données. Une session de modem sur l’appel. Les protocoles de modem actuels requièrent la station appelée pour initier le protocole de transfert. Pour un appel de modem de données entrant, l’application ne peut généralement pas effectuer de détection positive. La manière dont le fournisseur de services effectue cette détermination est son choix. Par exemple, une période de silence juste après avoir répondu à un appel entrant peut être utilisée comme heuristique pour décider qu’il peut s’agir d’un appel de modem de données.
-   Télécopie G3. Une session de télécopie de groupe 3 sur l’appel.
-   Télécopie G4. Une session de télécopie de groupe 4 sur l’appel.
-   Piloté. Le flux multimédia de l’appel utilise les périphériques de téléphonie pour le protocole sourd.
-   Données numériques. Flux de données numériques d’un format non spécifié.
-   TELETEX, Videotex, télex, mixte. Celles-ci correspondent aux services télématiques portant le même nom.
-   Modification. Session d’interface des services d’affichage analogique sur l’appel. ADSI améliore les appels vocaux avec des informations alphanumériques téléchargées sur le téléphone et l’utilisation de boutons logiciels sur le téléphone.

Une application peut activer ou désactiver l’analyse des médias sur un appel spécifié avec [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia). L’application spécifie les types de médias qui doivent être analysés, et lorsque la surveillance du média est activée, la détection d’une modification de type de média entraîne la notification de l’application avec le message [**\_ MONITORMEDIA de ligne**](line-monitormedia.md) . Ce message fournit le descripteur d’appel sur lequel la modification du type de média a été détectée, ainsi que le nouveau type de média.

Il existe une distinction entre le type de média d’un appel signalé par [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) et les rapports d’événements de type de média par les messages de MONITORMEDIA de ligne \_ . Le type de média d’un appel est déterminé exclusivement par les applications propriétaires de l’appel et n’est pas automatiquement modifié par les événements de surveillance du support. La seule exception est la détermination initiale du type de média qui peut être effectuée par la bibliothèque de liens dynamiques TAPI pour sélectionner le premier propriétaire d’un appel. Il est possible que, dans ce cas, la bibliothèque soit le propriétaire de l’appel.

L’analyse du type de média par défaut est effectuée pour les types de médias pour lesquels le périphérique de ligne a été ouvert. Cela permet de déterminer le type de média d’un appel entrant avant que l’appel ne soit transmis à une application en fonction de ce que l’application demande. La portée de la surveillance des médias d’un appel est liée par la durée de vie de l’appel. La surveillance des médias sur un appel se termine dès que l’appel *se déconnecte* ou devient *inactif*.

Une application peut obtenir des identificateurs d’appareil pour différentes classes d’appareils associées à une ligne ouverte en appelant [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid). Cette fonction prend un handle de ligne, une adresse ou un handle d’appel et une description de classe d’appareil. Elle retourne l’identificateur de l’appareil de la classe d’appareil donnée associée à l’appareil, à l’adresse ou à l’appel de ligne ouverte. Si la classe d’appareil est « TAPI/Line », l’identificateur d’appareil de l’appareil de ligne est retourné. Si la classe d’appareil est « MCI/Wave », l’identificateur d’appareil d’un appareil WaveAudio MCI est retourné (si pris en charge), ce qui permet des activités telles que l’enregistrement ou la lecture des données audio sur l’appel sur la ligne.

L’application peut utiliser l’identificateur d’appareil retourné avec l’API multimédia correspondante pour interroger les fonctionnalités de l’appareil et ouvrir par la suite l’appareil multimédia. Par exemple, si votre application doit utiliser la ligne comme périphérique de forme d’onde, elle doit d’abord appeler [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) et/ou [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) pour déterminer les fonctionnalités de forme d’onde de l’appareil. Le format de données Waveform standard pris en charge par la téléphonie dans Amérique du Nord est m-Law 8 bits à 8000 échantillons par seconde, bien que le pilote de périphérique Wave puisse convertir ce taux d’échantillonnage et Companding en d’autres formats audio multimédia plus courants.

Pour ouvrir par la suite un appareil de ligne pour la lecture audio à l’aide de l’API Waveform, une application appelle [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen). L’implémentation de **waveOutOpen** est spécifique à l’appareil, et il existe de nombreuses options pour l’implémentation de cette fonction.

 

 
