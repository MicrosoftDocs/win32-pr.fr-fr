---
description: Les analyses peuvent examiner des frames en mode local uniquement ou en mode promiscuité.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Modes de Local-Only et de promiscuité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8155c968f82154712ec8926f114e63380cdb1099bf7908d5a4dde86d7646dc20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555889"
---
# <a name="local-only-and-promiscuous-modes"></a>Modes de Local-Only et de promiscuité

Les analyses peuvent examiner des frames en mode local uniquement ou en mode promiscuité.

En mode local uniquement, le fournisseur de paquets réseau (NPP) renvoie les trames envoyées vers ou à partir de l’ordinateur sur lequel le moniteur est exécuté, y compris les diffusions et les multidiffusions dirigées vers l’ordinateur local. Bien que limité à des frames dirigés localement, le mode local est également beaucoup moins gourmand en ressources processeur.

En mode promiscuité, le moniteur peut également surveiller le trafic qui n’est pas dirigé vers ou à partir de l’ordinateur local. À moins que l’analyse n’ait spécifié l’indicateur, MCS \_ Create \_ PMODE \_ not \_ Required, dans la fonction [OnLoadingDLL](onloadingdll.md) , le service de contrôle d’analyse (MCSVC) suppose que le moniteur nécessite un mode de proximité lorsqu’il charge la dll du moniteur.

 

 



