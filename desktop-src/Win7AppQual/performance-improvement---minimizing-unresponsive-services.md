---
description: Meilleures pratiques pour réduire les services qui ne répondent pas
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Meilleures pratiques pour réduire les services qui ne répondent pas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3f37620fc00834b3c25a92292c889785818c2810cac7c12e788de8bf1fb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994849"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Meilleures pratiques pour réduire les services qui ne répondent pas

## <a name="affected-platform"></a>Plateforme affectée

 **Clients** – Windows Vista \| Windows 7  

## <a name="description"></a>Description

Les services qui ne répondent pas peuvent entraîner des délais d’attente, des sessions terminées et même des données perdues. L’utilisation des meilleures pratiques peut réduire de manière considérable l’occurrence de services qui ne répondent pas.

## <a name="best-practices"></a>Meilleures pratiques

Assurez-vous que vos applications et tous leurs services et pilotes dépendants répondent aux notifications d’arrêt et de puissance système.

-   Toutes les applications doivent répondre rapidement et de manière appropriée aux messages d’arrêt tels que WM \_ QUERYENDSESSION et WM \_ ENDSESSION qui indiquent un arrêt en cours.
-   Tous les services doivent répondre rapidement aux notifications d’arrêt SCM. S’ils ne parviennent pas à le faire, l’ordinateur les traite comme ne répondant pas et démarre un délai de 20 secondes et les arrête, ce qui permet d’éviter la perte de données. Cela ajoute également 20 secondes à l’heure d’arrêt d’un arrêt de l’ordinateur.
-   Tous les services qui ont des dépendances de pilote de périphérique en mode noyau doivent répondre rapidement et de manière appropriée à \_ la notification d’arrêt d’IRP MJ \_ dans leurs routines DispatchShutdown.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

<dl>

[Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



