---
description: Si la source de données est un fichier journal, vous pouvez spécifier une plage de temps pour la requête.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Définition d’une plage de temps pour une requête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007170"
---
# <a name="setting-a-time-range-for-a-query"></a>Définition d’une plage de temps pour une requête

Si la source de données est un fichier journal, vous pouvez spécifier une plage de temps pour la requête. La requête récupère les données de compteur à partir du fichier journal qui a été collecté au cours de la période spécifiée. Pour définir l’intervalle de temps, appelez la fonction [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) . **PdhSetQueryTimeRange** n’est pas utilisé pour interroger les données de performances à partir de sources de données en temps réel.

Pour créer une valeur d’heure, procédez comme suit.

1.  Allouez une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) et initialisez les champs avec la valeur de temps souhaitée.
2.  Appelez [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) pour convertir la valeur de temps de la structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en heure de structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
3.  Effectuez un cast de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) en variable LongLong, en gardant à l’esprit les conventions de remplissage des membres de la structure de votre plateforme et du compilateur.
4.  Copiez la valeur LONGLONG dans le champ approprié dans la structure d' [**\_ \_ informations de temps PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .

Pour récupérer la plage horaire de toutes les données de performances contenues dans un fichier journal, appelez la fonction [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .

 

 
