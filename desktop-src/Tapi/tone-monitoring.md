---
description: La surveillance des tons surveille le flux multimédia d’un appel pour des tonalités spécifiées.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Analyse des tons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb811d91a70f439ae17123b35967800914bd6a04f1a30168754f602231f038e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034179"
---
# <a name="tone-monitoring"></a>Analyse des tons

La surveillance des tons surveille le flux multimédia d’un appel pour des tonalités spécifiées. Un ton est décrit par ses fréquences de composant et cadence. Une implémentation de l’API peut permettre la surveillance simultanée de plusieurs tonalités différentes. Une application peut étiqueter chaque nuance pour pouvoir distinguer les différentes tonalités pour lesquelles elle demande la détection.

Une application peut activer ou désactiver la surveillance des sons sur un appel spécifié avec [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones). Avec cette fonction, l’application indique les tonalités à détecter sur un appel spécifié. Lorsque la surveillance des tons est activée, les chiffres détectés entraînent la notification de l’application avec le message de [**ligne \_ MONITORTONE**](line-monitortone.md) . Ce message fournit le descripteur d’appel sur lequel le ton a été détecté, ainsi que la balise de l’application pour le ton.

L’étendue de la surveillance des tons est liée par la durée de vie de l’appel. La surveillance des tons sur un appel se termine dès que l’appel se *déconnecte* ou devient *inactif*.

> [!Note]  
> La surveillance des tonalités, des chiffres ou des types de média requiert souvent l’utilisation de ressources dont le fournisseur de services peut uniquement avoir une quantité finie. Une demande de surveillance peut être rejetée si les ressources ne sont pas disponibles. Pour la même raison, une application doit désactiver toute analyse inutile.

 

 

 



