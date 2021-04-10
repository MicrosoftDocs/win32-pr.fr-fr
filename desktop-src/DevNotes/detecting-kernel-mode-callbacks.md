---
description: Si un thread attend la fin d’un rappel en mode noyau, le côté mode utilisateur du thread retarde lors d’un appel à la fonction ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Détection des rappels de Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950742"
---
# <a name="detecting-kernel-mode-callbacks"></a>Détection des rappels de Kernel-Mode

La majeure partie du code pour le système d’exploitation Windows s’exécute en mode noyau. Le mode de processeur passe du mode utilisateur au mode noyau chaque fois qu’un thread d’application appelle une fonction à partir de l’API Windows qui, à son tour, appelle une fonction système interne qui doit s’exécuter en mode noyau. Le mode de processeur revient en mode utilisateur avant que le contrôle ne retourne à la fonction afin que les données système soient protégées.

Si un thread attend la fin d’un rappel en mode noyau, le côté mode utilisateur du thread retarde lors d’un appel à la fonction **ZwCallbackReturn** .

 

 



