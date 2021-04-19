---
description: La plupart des compteurs requièrent deux exemples de valeurs pour calculer une valeur affichable.
ms.assetid: 75e45baf-51c5-400c-a31f-92bdab4ee492
title: Affichage des données de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d913474b794585dd557fae2b1fc232336b637d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527895"
---
# <a name="displaying-performance-data"></a>Affichage des données de performances

La plupart des compteurs requièrent deux exemples de valeurs pour calculer une valeur affichable. La formule de chaque compteur détermine si le compteur requiert deux échantillons. Pour obtenir la liste des compteurs et leurs formules, consultez la section types de compteurs du [Kit de déploiement de Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).

La [collecte des données de performances](collecting-performance-data.md) montre comment récupérer des exemples de données. Une fois que vous avez les exemples, vous appelez généralement [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) pour calculer une valeur affichable.

Si vous devez mettre à l’échelle la valeur du compteur vers le haut ou vers le haut pour afficher la valeur, appelez la fonction [**PdhSetCounterScaleFactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor) avant d’appeler [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue). Les valeurs de compteur peuvent être mises à l’échelle d’une puissance de dix d’un facteur de-7 à 7.

Si le chemin d’accès au compteur contient un caractère générique pour le nom de l’instance, appelez [**PdhGetFormattedCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya) pour récupérer un tableau de valeurs de compteur mises en forme pour chaque instance collectée.

Vous pouvez également utiliser les fonctions [**PdhCalculateCounterFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue) et [**PdhFormatFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue) pour calculer une valeur affichable. Pour utiliser ces fonctions, vous devez récupérer l’exemple collecté après chaque appel [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) et stocker l’exemple vous-même. Pour récupérer l’exemple, appelez la fonction [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue) ou [**PdhGetRawCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya) . Pour les valeurs de compteur basées sur le temps, appelez [**PdhGetCounterTimeBase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase) avant **PdhFormatFromRawValue** pour récupérer la base de temps du compteur.

Si vous effectuez des calculs à l’aide des données brutes, vérifiez toujours le membre **CStatus** de la structure de [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) avant d’utiliser l’exemple. L’exemple n’est pas valide si la valeur de **CStatus** n’est pas PDH \_ CStatus \_ New \_ Data ou PDH \_ CStatus des \_ données valides \_ .

## <a name="displaying-statistics-for-a-counter"></a>Affichage des statistiques d’un compteur

Si vous souhaitez calculer les valeurs minimale, maximale et moyenne d’un compteur, appelez la fonction [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) . Lorsque vous collectez des exemples, stockez les structures de [**\_ \_ compteur bruts PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) dans un tableau que vous transmettez à **PdhComputeCounterStatistics**. La fonction retourne les valeurs statistiques dans une structure de [**\_ statistiques PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics) .

Vous pouvez également utiliser cette fonction pour compresser un fichier journal. Par exemple, lisez dix enregistrements dans un fichier journal, appelez [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) pour calculer la valeur moyenne, puis écrivez la valeur moyenne dans un fichier journal de sortie.

 

 
