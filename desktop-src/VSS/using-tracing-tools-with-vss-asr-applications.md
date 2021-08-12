---
description: Vous pouvez utiliser l’outil Logman pour collecter des informations de traçage pour les applications VSS qui utilisent la récupération automatique du système (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Utilisation des outils de suivi avec les applications ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2d22dbb1488b5fd60836926d3c5ef2de5913ff1cc1529fdb278773b2ccd8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590868"
---
# <a name="using-tracing-tools-with-asr-applications"></a>Utilisation des outils de suivi avec les applications ASR

Vous pouvez utiliser l’outil Logman pour collecter des informations de traçage pour les applications VSS qui utilisent la [récupération automatique du système (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md). Logman (logman.exe) est un contrôleur de trace pour les événements de trace et les compteurs de performance. il est inclus dans Windows XP et les versions ultérieures de Windows. Ou, si vous préférez, vous pouvez utiliser l’outil tracelog pour collecter les mêmes informations de suivi ASR. Tracelog est inclus dans le Kit de pilotes Windows (WDK).

Pour utiliser les outils de suivi avec VSS, consultez [utilisation des outils de suivi avec VSS](using-tracing-tools-with-vss.md).

## <a name="using-logman"></a>Utilisation de logman

La procédure suivante décrit comment utiliser logman avec votre application ASR.

**Pour utiliser logman avec votre application ASR**

1.  Utilisez la commande suivante pour démarrer le suivi :

    **logman start ASR-o** *x : \\ * * * ASR. etl-ETS-p {6407345b-94f2-44C8-b3db-4e076be46816} 0xFF 0xFF**

    > [!Note]  
    > Remplacez « x : \\ » par le chemin d’accès au répertoire où vous souhaitez que le fichier journal des traces soit stocké. Pour des performances optimales, le fichier journal de trace doit se trouver sur un volume qui ne fait pas partie du cliché instantané.

     

2.  Utilisez la commande suivante pour arrêter le suivi :

    **logman arrêter ASR-ETS**

Le fichier journal des traces est *x \\ :* ASR. etl.

Pour plus d’informations sur l’outil Logman, consultez [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Utilisation de tracelog

La procédure suivante décrit comment utiliser tracelog.

**Pour utiliser tracelog**

1.  Créez un fichier texte nommé ASR. CTL qui contient uniquement le texte suivant :

    **ASR 6407345b-94f2-44C8-b3db-4e076be46816**

2.  Utilisez la commande suivante pour démarrer le suivi :

    **tracelog-Start ASR-f** *x : \\ * * * ASR. etl-GUID ASR. Ctrl-Flag-niveau 0xFF-niveau 0xFF**

    > [!Note]  
    > Remplacez « x : \\ » par le chemin d’accès au répertoire où vous souhaitez que le fichier journal des traces soit stocké. Pour des performances optimales, le fichier journal de trace doit se trouver sur un volume qui ne fait pas partie du cliché instantané.

     

3.  Utilisez la commande suivante pour arrêter le suivi :

    **tracelog-arrêter ASR**

Le fichier journal des traces est *x \\ :* ASR. etl.

Pour plus d’informations sur l’outil tracelog, consultez [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
