---
description: Le SDK Windows (WSDK) contient trois dll d’exemples de performances complètes.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Exemples de DLL de performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534262"
---
# <a name="performance-dll-samples"></a>Exemples de DLL de performance

Le SDK Windows (WSDK) contient trois dll d’exemples de performances complètes. Ces exemples se trouvent dans le répertoire Samples \\ WinBase \\ winnt \\ PerfTool \\ PerfDlls La racine de ce chemin d’accès est le répertoire d’installation de base de WSDK. Vous pouvez télécharger le WSDK à partir du [Kit de développement logiciel (SDK) Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (recherchez SDK Windows, puis sélectionnez Télécharger pour le dernier système d’exploitation publié).

Les exemples contenus dans ce répertoire sont les suivants :

-   **AppMem**: fournit les équivalents des fonctions [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)et [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) qui signalent les informations de performances. Les compteurs de performance dans le registre et l’outil performance peuvent lire les informations de performances.
-   **LeakyBin**: illustre l’utilisation des compteurs de performance de l’application.
-   **PerfGen**: fournit trois formes d’onde à cinq périodes différentes pour une utilisation avec l’outil performance pour fournir des données à une vitesse et une valeur connues. Cela peut être utile pour tester des applications qui utilisent des données de performances et nécessitent des valeurs prévisibles pour le test.

 

 
