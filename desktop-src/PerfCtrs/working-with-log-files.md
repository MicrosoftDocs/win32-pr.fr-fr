---
description: Pour ouvrir un fichier journal en lecture, appelez PdhOpenQuery et spécifiez un chemin d’accès au fichier journal.
ms.assetid: 1d8f8662-df1f-4f84-8b65-c152f79cc5c6
title: Utilisation des fichiers journaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2032b90036f8f58c07d8c7e80e7e7ac2b2701c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239610"
---
# <a name="working-with-log-files"></a>Utilisation des fichiers journaux

Pour ouvrir un fichier journal en lecture, appelez [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) et spécifiez un chemin d’accès au fichier journal. Pour ouvrir un fichier journal en écriture, vous devez appeler [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Pour fermer un fichier journal, appelez [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) ou [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) selon la fonction que vous avez utilisée pour ouvrir le fichier journal.

## <a name="reading-from-a-log-file"></a>Lire à partir d’un fichier journal

La lecture des données de performances à partir d’un fichier journal est identique à la lecture de données à partir d’une source en temps réel. pour cela, vous pouvez ouvrir une requête, ajouter des compteurs à la requête et appeler [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) pour collecter un exemple à partir du fichier journal. **PdhCollectQueryData** retourne PDH \_ aucune \_ \_ donnée quand vous atteignez la fin du fichier journal.

Chaque exemple dans le fichier journal contient un horodatage pour le moment où il a été initialement collecté et écrit dans le fichier journal. Pour récupérer l’horodatage du premier et du dernier échantillon dans le fichier journal, appelez la fonction [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) . Si vous souhaitez limiter les exemples que vous avez lus dans le journal à un intervalle de temps spécifique, consultez [définition d’une plage de temps pour une requête](setting-a-time-range-for-a-query.md).

Si vous ne connaissez pas les objets de performance et les compteurs présents dans le fichier journal, vous pouvez appeler [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) pour déterminer la liste des objets. À partir d’un objet, vous pouvez appeler [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) ou [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) pour récupérer une liste des instances et des compteurs de l’objet contenus dans le fichier journal.

Si vous appelez [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa), utilisez les listes d’instances et de compteurs pour créer un chemin d’accès pour chaque combinaison possible d’instance et de compteur. Quand vous appelez [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) pour ajouter le compteur à la requête, la fonction échoue si le fichier journal ne contient pas la combinaison donnée.

Si vous utilisez [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha), vous pouvez créer un chemin d’accès qui contient un caractère générique pour le nom et le compteur de l’instance, par exemple, \\ Object ( \* ) \\ \* . La fonction retourne le \_ \_ chemin d’accès PDH non valide si l’objet ne contient pas d’instance. Dans ce cas, appelez **PdhExpandWildCardPath** à l’aide d’un caractère générique pour le compteur uniquement, par exemple, \\ Object \\ \* .

Les systèmes d’exploitation plus récents peuvent lire les fichiers journaux qui ont été générés sur des systèmes d’exploitation plus anciens. toutefois, les fichiers journaux créés sur Windows Vista et les systèmes d’exploitation ultérieurs ne peuvent pas être lus sur les systèmes d’exploitation antérieurs.

Pour obtenir un exemple qui lit des données à partir d’un fichier journal, consultez [lecture des données de performances à partir d’un fichier journal](reading-performance-data-from-a-log-file.md).

## <a name="reading-from-multiple-log-files"></a>Lecture à partir de plusieurs fichiers journaux

Si vous avez besoin de créer une requête qui lit à partir de plusieurs fichiers journaux, appelez [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) pour lier les fichiers journaux. Vous devez ensuite utiliser des fonctions PDH qui se terminent par « H », par exemple, [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh).

## <a name="writing-to-a-log-file"></a>Écriture dans un fichier journal

Avant d’écrire dans un fichier journal, appelez [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) pour créer une requête et spécifier la source des données de performances, qu’il s’agisse de données en temps réel ou d’un fichier journal. Ensuite, ajoutez les compteurs que vous souhaitez interroger.

Pour ouvrir le fichier de destination, appelez [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Spécifiez la requête lorsque vous ouvrez le fichier journal. Pour collecter les données de performances et les écrire dans le fichier journal, appelez [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

Si les données du compteur sont écrites dans un fichier journal délimité par des virgules (.csv) ou délimité par des tabulations (. TSV) et que le chemin d’accès contient une instance de caractère générique, le chemin d’accès est développé et seules les instances qui existent au moment où le chemin d’accès est développé sont incluses dans le fichier journal. toutefois, pour les fichiers journaux binaires (. blg) ou SQL, le caractère générique n’est pas développé afin que le fichier journal contienne des instances créées lors de la journalisation.

Pour obtenir un exemple qui écrit des données dans un fichier journal, consultez [écriture de données de performances dans un fichier journal](writing-performance-data-to-a-log-file.md).

## <a name="compressing-a-log-file"></a>Compression d’un fichier journal

Vous pouvez utiliser la fonction [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) pour compresser un fichier journal. Par exemple, lisez dix enregistrements dans un fichier journal, appelez **PdhComputeCounterStatistics** pour calculer la valeur moyenne, puis écrivez la valeur moyenne dans un fichier journal de sortie.

La rubrique suivante fournit des informations supplémentaires sur l’utilisation d’un fichier journal.

-   [Obtention de la taille d’un fichier journal](getting-the-size-of-a-log-file.md)

 

 



