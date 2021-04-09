---
description: Les moniteurs reçoivent les trames réseau capturées en temps réel. Les trames sont capturées par un fournisseur de paquets réseau (NPP) à l’aide de l’interface COM des fournisseurs IRTC et transmises à l’analyse dans l’un des deux threads d’exécution du moniteur.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Captures de Real-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869033"
---
# <a name="real-time-captures"></a>Captures de Real-Time

Les moniteurs reçoivent les trames réseau capturées en temps réel. Les trames sont capturées par un [*fournisseur de paquets réseau*](n.md) (NPP) à l’aide de l’interface com [IRTC](irtc.md) du fournisseur et transmises à l’analyse dans l’un des deux threads d’exécution de l’analyse.

Les analyses peuvent limiter le nombre d’images qu’elles doivent traiter en passant un [*filtre de capture*](c.md) au NPP qui fournit les frames. En règle générale, une analyse spécifique est conçue pour surveiller des types spécifiques de trafic, tels que HTTP, RIPX ou SMB. À la différence des experts qui utilisent des analyseurs sophistiqués pour sélectionner les informations à analyser, un moniteur doit examiner chaque cadre pour déterminer les conditions qu’il a été prévu de détecter. La raison de cette approche Frame-by-frame est la performance. Une analyse doit traiter ses frames suffisamment rapidement pour ne pas se trouver derrière le pilote qui fournit les frames au NPP. Dans le cas contraire, les données seront perdues.

 

 



