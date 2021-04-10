---
description: Pour créer une requête qui collecte des données de performances à partir d’une source ou d’un fichier journal en temps réel, appelez la fonction PdhOpenQuery. La fonction retourne un handle vers la requête que vous utilisez dans les appels de fonction PDH ultérieurs.
ms.assetid: 6fd4716e-b163-47a3-b0cb-5f9599f8681f
title: Création d'une requête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9d50ec52966529a3476a6d375606ba3d0b538b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115566"
---
# <a name="creating-a-query"></a>Création d'une requête

Pour créer une requête qui collecte des données de performances à partir d’une source ou d’un fichier journal en temps réel, appelez la fonction [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) . La fonction retourne un handle vers la requête que vous utilisez dans les appels de fonction PDH ultérieurs.

Après avoir créé la requête, appelez la fonction [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) pour chaque compteur que vous souhaitez ajouter à la requête. Vous pouvez utiliser l’une des méthodes suivantes pour fournir le chemin d’accès complet au compteur.

-   Définissez le chemin d’accès du compteur comme une chaîne statique. Utilisez cette méthode si vous surveillez toujours le même compteur et si vous êtes familiarisé avec la syntaxe correcte d’un chemin d’accès de compteur. Pour plus d’informations sur la syntaxe correcte utilisée pour spécifier un compteur, consultez [spécification d’un chemin d’accès de compteur](specifying-a-counter-path.md).
-   Initialisez une [**structure \_ \_ d' \_ éléments de chemin d’accès de compteur PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) avec les noms de l’ordinateur, de l’objet, du compteur et de l’instance. Transmettez cette structure à [**PdhMakeCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha) , qui retournera un chemin de compteur pour les éléments spécifiés.
-   Spécifiez un chemin d’accès de compteur qui contient des caractères génériques et appelez [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) pour obtenir une liste de noms de compteurs qui correspondent aux caractères génériques du chemin d’accès. Parcourez la liste des noms de compteurs et ajoutez à la requête les compteurs que vous souhaitez dans cette liste.
-   Appelez la fonction [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) pour afficher une boîte de dialogue qui permet à l’utilisateur de parcourir et de sélectionner les compteurs de performances. Pour plus d’informations, consultez [exploration des compteurs](browsing-counters.md).

Notez que si une instance de compteur spécifiée n’existe pas, [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) ne signale pas de condition d’erreur. Au lieu de cela, elle retourne la réussite de l’erreur \_ . Ce comportement est dû au fait qu’il n’est pas connu si une instance de compteur inexistante a été spécifiée ou si elle existe, mais n’a pas encore été créée.

L’instance de compteur manquante sera signalée par [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata), [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)ou [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue). Lors de l’appel de **PdhCollectQueryData** pour une seule instance de compteur, et que l’instance de compteur n’existe toujours pas, il est supposé que l’instance de compteur n’existe pas et que la fonction retourne PDH \_ aucune \_ donnée. Toutefois, si plusieurs compteurs sont interrogés, **PdhCollectQueryData** peut toujours retourner une erreur \_ de réussite même si l’une des instances de compteur n’existe pas encore. Dans ce cas, appelez **PdhGetRawCounterValue** ou **PdhGetFormattedCounterValue** pour chacune des instances de compteur intéressantes. Si l’instance n’existe pas lors de l’appel de **PdhGetRawCounterValue**, la fonction retourne la \_ réussite de l’erreur et définit le membre **CStatus** du [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) sur l' \_ État PDH \_ aucune \_ instance. Si l’instance n’existe pas lors de l’appel de **PdhGetFormattedCounterValue**, la fonction retourne des \_ données non valides PDH \_ et définit le membre **CStatus** du [**\_ fmt PDH \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue) sur PDH \_ CStatus \_ aucune \_ instance.

Notez que le chemin d’accès au compteur spécifié dans la fonction [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) doit être localisé. La fonction [**PdhAddEnglishCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera) fournit un moyen indépendant des paramètres régionaux pour ajouter des compteurs de performances à la requête. Cette fonction est la méthode recommandée pour ajouter des compteurs de paramètres régionaux neutres à une requête.

Pour supprimer un compteur d’une requête, appelez la fonction [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter) .

Une fois que vous avez terminé la collecte des données pour une requête, appelez la fonction [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) pour fermer la requête et libérer toutes les ressources système allouées. **PdhCloseQuery** ferme tous les descripteurs de compteur associés à la requête.

 

 



