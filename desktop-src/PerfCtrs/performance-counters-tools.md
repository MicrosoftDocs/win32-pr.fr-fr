---
description: Le tableau suivant répertorie les
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Outils des compteurs de performances
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951996"
---
# <a name="performance-counters-tools"></a>Outils des compteurs de performances

## <a name="data-collection-tools"></a>Outils de collecte de données

Les outils suivants sont utiles lors de l’utilisation ou de la manipulation des données des compteurs de performances Windows.

|Outil|Description
|----|-----------
| [PerfMon](/windows-server/administration/windows-commands/perfmon) | Outil d’interface graphique pour la collecte et l’affichage des données des compteurs de performances. `perfmon.exe` lance la console MMC avec le composant logiciel enfichable analyseur de performances, qui permet d’accéder à l’analyseur de performances, aux ensembles de collecteurs de données et aux outils de rapports.
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |Outil en ligne de commande pour collecter et imprimer les données des compteurs de performances. Peut être utilisé pour répertorier les countersets disponibles, répertorier les compteurs disponibles, imprimer les données de compteur sur la console ou collecter les données de compteur dans un fichier journal (CSV, TDF, BLG).
| [Rejournaliser](/windows-server/administration/windows-commands/relog) |Outil en ligne de commande permettant de transformer et de fusionner les fichiers journaux (CSV, TDF, BLG) capturés via `typeperf.exe` ou via les `PDH.dll` API.
| [LogMan](/windows-server/administration/windows-commands/logman) |Outil en ligne de commande pour contrôler les ensembles de collecteurs de données.

## <a name="data-provider-tools"></a>Outils du fournisseur de données

Les outils suivants sont utiles lors de la publication de données de compteur de performances Windows.

|Outil|Description
|----|-----------
| [CtrPP](ctrpp.md) | Outil de génération à partir de la ligne de commande de la SDK Windows qui valide et compile vos compteurs de performance manifeste du fournisseur v2. Cet outil génère les `.h` en-têtes et les `.rc` scripts de ressources nécessaires à la création d’un fournisseur v2.
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | Outil de ligne de commande utilisé pour installer votre fournisseur sur un système.
| [UnlodCtr](/windows-server/administration/windows-commands/unlodctr_1) | Outil de ligne de commande utilisé pour désinstaller votre fournisseur d’un système.
