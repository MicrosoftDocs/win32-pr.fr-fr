---
title: Recherche d’un format spécifique
description: Recherche d’un format spécifique
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- le gestionnaire de compression audio (ACM), recherche de formats
- ACM (gestionnaire de compression audio), recherche de formats
- Exemples ACM, recherche de formats
- recherche de formats
- acmFormatEnum fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc291a6dff0c6b2befec6afd001a32735a54e95fd65a464378adb690a95019c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691529"
---
# <a name="finding-a-specific-format"></a>Recherche d’un format spécifique

Une application ne peut avoir qu’une spécification partielle pour un format lorsqu’elle a besoin de la spécification complète. Par exemple, la spécification peut stipuler un format ADPCM à 16 bits, qui n’est pas le nombre moyen d’octets par seconde. L’application peut obtenir le format complet sans intervention de l’utilisateur à l’aide de la fonction [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) et en spécifiant des indicateurs dans le paramètre *fdwEnum* .

 

 




