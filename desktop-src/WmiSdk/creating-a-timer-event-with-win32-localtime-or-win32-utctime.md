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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210211"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a><span data-ttu-id="45d98-103">Création d’un événement de minuterie avec Win32 \_ localtime ou Win32 \_ UTCTime</span><span class="sxs-lookup"><span data-stu-id="45d98-103">Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime</span></span>

<span data-ttu-id="45d98-104">Vous pouvez utiliser le modèle standard d’événements intrinsèques et de filtres d’événements en association avec les classes [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) pour recevoir une notification minutée.</span><span class="sxs-lookup"><span data-stu-id="45d98-104">You can use the standard model of intrinsic events and event filters in combination with the [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes to receive a timed notification.</span></span> <span data-ttu-id="45d98-105">La méthode intrinsèque est une méthode recommandée pour générer des événements chronométrés, car elle est cohérente avec le reste du modèle d’événement Microsoft et prend en charge des conditions de planification complexes.</span><span class="sxs-lookup"><span data-stu-id="45d98-105">The intrinsic method is a recommended way of generating timed events, as it is consistent with the rest of the Microsoft event model and supports complex scheduling conditions.</span></span>

<span data-ttu-id="45d98-106">Les classes [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) et [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) sont des classes Singleton dans l' \\ espace de noms CIMV2 racine qui représentent l’horloge système.</span><span class="sxs-lookup"><span data-stu-id="45d98-106">The [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) and [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes are singleton classes in the root\\cimv2 namespace that represent the system clock.</span></span> <span data-ttu-id="45d98-107">Lorsqu’il est interrogé, **Win32 \_ localtime** retourne l’heure actuelle au moment de la récupération des données au format 24 heures avec une référence locale.</span><span class="sxs-lookup"><span data-stu-id="45d98-107">When queried, **Win32\_LocalTime** returns the current time at the moment of data retrieval in a 24-hour clock with local reference.</span></span> <span data-ttu-id="45d98-108">La **classe \_ UTCTime Win32** retourne l’heure actuelle avec la référence UTC.</span><span class="sxs-lookup"><span data-stu-id="45d98-108">The **Win32\_UTCTime** class returns the current time with UTC reference.</span></span>

<span data-ttu-id="45d98-109">**Pour générer des événements chronométrés ou répétitifs avec Win32 \_ localtime ou Win32 \_ UTCTime**</span><span class="sxs-lookup"><span data-stu-id="45d98-109">**To generate timed or repeating events with Win32\_LocalTime or Win32\_UTCTime**</span></span>

-   <span data-ttu-id="45d98-110">Configurez un filtre d’événement de notification intrinsèque pour [**les \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) [**\_ localtime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou Win32 qui demande une notification pour une date et une heure spécifiques.</span><span class="sxs-lookup"><span data-stu-id="45d98-110">Set up an intrinsic notification event filter for [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) that requests notification for a specific date and time.</span></span>

<span data-ttu-id="45d98-111">Par exemple, si l’heure locale de l’heure d’été est de 4 h 00</span><span class="sxs-lookup"><span data-stu-id="45d98-111">For example, if the local time under Daylight Savings Time is 4 P.M.</span></span> <span data-ttu-id="45d98-112">et l’emplacement est GMT-8, tandis que [**Win32 \_ localtime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) retourne 16 et [**Win32 \_ UTCTime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) retourne 23.</span><span class="sxs-lookup"><span data-stu-id="45d98-112">and the location is GMT -8, then [**Win32\_LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) returns 16 and [**Win32\_UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) returns 23.</span></span>

<span data-ttu-id="45d98-113">L’exemple de code suivant décrit comment créer un filtre d’événements qui signale un événement répété tous les jours à minuit.</span><span class="sxs-lookup"><span data-stu-id="45d98-113">The following code example describes how to create an event filter that signals a repeating event every day at midnight.</span></span>

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

 

 
