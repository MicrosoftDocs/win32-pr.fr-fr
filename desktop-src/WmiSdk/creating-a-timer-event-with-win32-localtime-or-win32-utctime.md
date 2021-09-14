---
description: Vous pouvez utiliser le modèle standard d’événements intrinsèques et de filtres d’événements en association avec les \_ classes Win32 localtime ou Win32 \_ UTCTime pour recevoir une notification minutée.
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: Création d’un événement de minuterie avec Win32_LocalTime ou Win32_UTCTime
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 011b2270a80f6b632e832f77e8e7c528228801b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120449"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>Création d’un événement de minuterie avec Win32 \_ localtime ou Win32 \_ UTCTime

Vous pouvez utiliser le modèle standard d’événements intrinsèques et de filtres d’événements en association avec les classes [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) pour recevoir une notification minutée. La méthode intrinsèque est une méthode recommandée pour générer des événements chronométrés, car elle est cohérente avec le reste du modèle d’événement Microsoft et prend en charge des conditions de planification complexes.

Les classes [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) et [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) sont des classes Singleton dans l' \\ espace de noms CIMV2 racine qui représentent l’horloge système. Lorsqu’il est interrogé, **Win32 \_ localtime** retourne l’heure actuelle au moment de la récupération des données au format 24 heures avec une référence locale. La **classe \_ UTCTime Win32** retourne l’heure actuelle avec la référence UTC.

**Pour générer des événements chronométrés ou répétitifs avec Win32 \_ localtime ou Win32 \_ UTCTime**

-   Configurez un filtre d’événement de notification intrinsèque pour [**les \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) [**\_ localtime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou Win32 qui demande une notification pour une date et une heure spécifiques.

Par exemple, si l’heure locale de l’heure d’été est de 4 h 00 et l’emplacement est GMT-8, tandis que [**Win32 \_ localtime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) retourne 16 et [**Win32 \_ UTCTime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) retourne 23.

L’exemple de code suivant décrit comment créer un filtre d’événements qui signale un événement répété tous les jours à minuit.

``` syntax
// Win32_LocalTime and Win32_UTCTime reside in root\cimv2 namespace. 
// Defining the EventNamespace allows the filter
// to be compiled in any namespace.
instance of __EventFilter as $FILT1
{
 Name  = "wake-up call";
 Query = "SELECT * FROM __InstanceModificationEvent WHERE "    
 "TargetInstance ISA \"Win32_LocalTime\" AND "
 "TargetInstance.Hour = 0 AND TargetInstance.Minute = 0 AND "
 "TargetInstance.Second = 0";
 QueryLanguage = "WQL";
 EventNamespace = "root\\cimv2";
};
```

 

 
