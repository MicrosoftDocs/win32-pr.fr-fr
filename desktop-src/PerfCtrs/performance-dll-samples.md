---
description: le SDK Windows (WSDK) contient trois dll d’exemples de performances complètes.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Exemples de DLL de performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94e77ed35b1c328879ad5f83dded45fe92bf4a62ae15c794e5d9d9b23daeda1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143882"
---
# <a name="performance-dll-samples"></a>Exemples de DLL de performance

le SDK Windows (WSDK) contient trois dll d’exemples de performances complètes. Ces exemples se trouvent dans le répertoire Samples \\ WinBase \\ winnt \\ PerfTool \\ PerfDlls La racine de ce chemin d’accès est le répertoire d’installation de base de WSDK. vous pouvez télécharger le WSDK à partir du [kit de développement logiciel (SDK) de Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (recherchez SDK Windows et sélectionnez le téléchargement pour le dernier système d’exploitation publié).

Les exemples contenus dans ce répertoire sont les suivants :

-   **AppMem**: fournit les équivalents des fonctions [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)et [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) qui signalent les informations de performances. Les compteurs de performance dans le registre et l’outil performance peuvent lire les informations de performances.
-   **LeakyBin**: illustre l’utilisation des compteurs de performance de l’application.
-   **PerfGen**: fournit trois formes d’onde à cinq périodes différentes pour une utilisation avec l’outil performance pour fournir des données à une vitesse et une valeur connues. Cela peut être utile pour tester des applications qui utilisent des données de performances et nécessitent des valeurs prévisibles pour le test.

 

 
