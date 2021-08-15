---
description: Si un thread attend la fin d’un rappel en mode noyau, le côté mode utilisateur du thread retarde lors d’un appel à la fonction ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Détection des rappels de Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029ecf7d5b1f9220de51c2ecffe4bdf30da4cbd088d9d251fd0d24bab04934e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691449"
---
# <a name="detecting-kernel-mode-callbacks"></a>Détection des rappels de Kernel-Mode

la majeure partie du code pour le système d’exploitation Windows s’exécute en mode noyau. le mode de processeur passe du mode utilisateur au mode noyau chaque fois qu’un thread d’application appelle une fonction à partir de l’API Windows qui, à son tour, appelle une fonction système interne qui doit s’exécuter en mode noyau. Le mode de processeur revient en mode utilisateur avant que le contrôle ne retourne à la fonction afin que les données système soient protégées.

Si un thread attend la fin d’un rappel en mode noyau, le côté mode utilisateur du thread retarde lors d’un appel à la fonction **ZwCallbackReturn** .

 

 



