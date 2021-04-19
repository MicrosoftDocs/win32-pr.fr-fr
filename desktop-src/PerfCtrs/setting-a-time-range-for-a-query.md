---
description: Si la source de données est un fichier journal, vous pouvez spécifier une plage de temps pour la requête.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Définition d’une plage de temps pour une requête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534515"
---
# <a name="setting-a-time-range-for-a-query"></a><span data-ttu-id="ee49f-103">Définition d’une plage de temps pour une requête</span><span class="sxs-lookup"><span data-stu-id="ee49f-103">Setting a Time Range for a Query</span></span>

<span data-ttu-id="ee49f-104">Si la source de données est un fichier journal, vous pouvez spécifier une plage de temps pour la requête.</span><span class="sxs-lookup"><span data-stu-id="ee49f-104">If the data source is a log file, you can specify a time range for the query.</span></span> <span data-ttu-id="ee49f-105">La requête récupère les données de compteur à partir du fichier journal qui a été collecté au cours de la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ee49f-105">The query retrieves counter data from the log file that was collected during the specified time range.</span></span> <span data-ttu-id="ee49f-106">Pour définir l’intervalle de temps, appelez la fonction [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) .</span><span class="sxs-lookup"><span data-stu-id="ee49f-106">To set the time range, call the [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) function.</span></span> <span data-ttu-id="ee49f-107">**PdhSetQueryTimeRange** n’est pas utilisé pour interroger les données de performances à partir de sources de données en temps réel.</span><span class="sxs-lookup"><span data-stu-id="ee49f-107">**PdhSetQueryTimeRange** is not used to query performance data from real time data sources.</span></span>

<span data-ttu-id="ee49f-108">Pour créer une valeur d’heure, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="ee49f-108">To create time value, use the following steps.</span></span>

1.  <span data-ttu-id="ee49f-109">Allouez une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) et initialisez les champs avec la valeur de temps souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ee49f-109">Allocate a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure and initialize the fields with the desired time value.</span></span>
2.  <span data-ttu-id="ee49f-110">Appelez [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) pour convertir la valeur de temps de la structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en heure de structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="ee49f-110">Call [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) to convert the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure time value to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure time.</span></span>
3.  <span data-ttu-id="ee49f-111">Effectuez un cast de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) en variable LongLong, en gardant à l’esprit les conventions de remplissage des membres de la structure de votre plateforme et du compilateur.</span><span class="sxs-lookup"><span data-stu-id="ee49f-111">Cast the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure as a LONGLONG variable, keeping in mind the structure member padding conventions of your platform and compiler.</span></span>
4.  <span data-ttu-id="ee49f-112">Copiez la valeur LONGLONG dans le champ approprié dans la structure d' [**\_ \_ informations de temps PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .</span><span class="sxs-lookup"><span data-stu-id="ee49f-112">Copy the LONGLONG value to the appropriate field in the [**PDH\_TIME\_INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) structure.</span></span>

<span data-ttu-id="ee49f-113">Pour récupérer la plage horaire de toutes les données de performances contenues dans un fichier journal, appelez la fonction [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .</span><span class="sxs-lookup"><span data-stu-id="ee49f-113">To retrieve the time range of all of the performance data contained in a log file, call the [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) function.</span></span>

 

 
