---
description: Le tableau suivant répertorie les
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Outils des compteurs de performances
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: a4f1640a269b87cce7452e54a2557dcc9c34fe154ae9e9f95fdd3794e275b59e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033399"
---
# <a name="performance-counters-tools"></a>Outils des compteurs de performances

## <a name="data-collection-tools"></a>Outils de collecte de données

les outils suivants sont utiles lors de l’utilisation ou de la manipulation de Windows données de compteur de performances.

|Outil|Description
|----|-----------
| [PerfMon](/windows-server/administration/windows-commands/perfmon) | Outil d’interface graphique pour la collecte et l’affichage des données des compteurs de performances. `perfmon.exe` lance la console MMC avec le composant logiciel enfichable analyseur de performances, qui permet d’accéder à l’analyseur de performances, aux ensembles de collecteurs de données et aux outils de rapports.
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |Outil en ligne de commande pour collecter et imprimer les données des compteurs de performances. Peut être utilisé pour répertorier les countersets disponibles, répertorier les compteurs disponibles, imprimer les données de compteur sur la console ou collecter les données de compteur dans un fichier journal (CSV, TDF, BLG).
| [Rejournaliser](/windows-server/administration/windows-commands/relog) |Outil en ligne de commande permettant de transformer et de fusionner les fichiers journaux (CSV, TDF, BLG) capturés via `typeperf.exe` ou via les `PDH.dll` API.
| [LogMan](/windows-server/administration/windows-commands/logman) |Outil en ligne de commande pour contrôler les ensembles de collecteurs de données.

## <a name="data-provider-tools"></a>Outils du fournisseur de données

les outils suivants sont utiles lors de la publication Windows données de compteur de performances.

|Outil|Description
|----|-----------
| [CtrPP](ctrpp.md) | outil de génération à partir de la ligne de commande de la SDK Windows qui valide et compile vos compteurs de Performance manifeste du fournisseur V2. Cet outil génère les `.h` en-têtes et les `.rc` scripts de ressources nécessaires à la création d’un fournisseur v2.
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | Outil de ligne de commande utilisé pour installer votre fournisseur sur un système.
| [UnlodCtr](/windows-server/administration/windows-commands/unlodctr_1) | Outil de ligne de commande utilisé pour désinstaller votre fournisseur d’un système.
