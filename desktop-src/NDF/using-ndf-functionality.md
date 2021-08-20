---
title: Utilisation des fonctionnalités NDF
description: Microsoft fournit un accès à la fonctionnalité NDF par le biais d’une API publique. Lorsqu’un problème se produit, l’application peut utiliser cette API pour tirer parti de cette fonctionnalité dans le contexte d’une application spécifique.
ms.assetid: db06b9a9-a64a-43ff-9b77-95230208cfd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85d1386971207330579f5395989e14c4b2315dc578f5bb3509695b99d6e215a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133226"
---
# <a name="using-ndf-functionality"></a>Utilisation des fonctionnalités NDF

Microsoft fournit un accès à la fonctionnalité NDF par le biais d’une API publique. Lorsqu’un problème se produit, l’application peut utiliser cette API pour tirer parti de cette fonctionnalité dans le contexte d’une application spécifique.

Il existe trois étapes de diagnostic avec NDF : création d’un incident, exécution du diagnostic et réparations et fermeture de l’incident. Cette vue d’ensemble indique les fonctions NDF qui peuvent être pertinentes pour un scénario spécifique. Vous trouverez des informations détaillées sur chaque fonction dans la section [référence NDF](ndf-reference.md) .

## <a name="creating-an-incident"></a>Création d’un incident

Une session de diagnostics NDF requiert un incident spécifique pour le diagnostic. Il existe plusieurs fonctions qui peuvent être utilisées pour créer un incident. Choisissez la fonction qui correspond le mieux à ce que l’application essayait de faire lorsque la défaillance s’est produite.

-   [**NdfCreateConnectivityIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident): problèmes généraux de connectivité Internet qui n’ont pas besoin d’informations supplémentaires.
-   [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) / [**NdfCreateWebIncidentEx**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex): connexion à une URL HTTP ou HTTPS.
-   [**NdfCreateSharingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident): accès à un chemin d’accès UNC ou à un partage de fichiers.
-   [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident): résolution d’un nom d’hôte DNS.
-   [**NdfCreatePnrpIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident): résolution d’un nom d’homologue PNRP.
-   [**NdfCreateGroupingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident): jointure d’un groupe d’égal à égal.
-   [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident): connexion à une destination à l’aide d’un socket (si aucune autre fonction ne s’applique spécifiquement).
-   [**NdfCreateIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident): utilisé quand aucun autre scénario n’est approprié et que la classe d’assistance NDF spécifique à appeler est connue (avec les arguments requis). Principalement utilisé à des fins de test par des développeurs d’applications qui ont écrit leur propre classe d’assistance.

## <a name="running-diagnosis-and-repairs"></a>Exécution du diagnostic et des réparations

Il existe deux façons de lancer la fonctionnalité de diagnostic et de réparation.

-   utilisation de l’Interface utilisateur Windows (recommandé)

    lors de l’exécution dans l’interface utilisateur standard Windows, vous pouvez simplement appeler la fonction [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) . L’Assistant NDF démarre et aide l’utilisateur à identifier (et, si possible, et à résoudre) le problème. La fonction est retournée une fois ce processus terminé. L’interface utilisateur est éventuellement modale pour votre application.

-   utilisation d’une Interface utilisateur personnalisée (Windows 7 et versions ultérieures uniquement)

    différentes fonctions peuvent être utilisées dans les scénarios où aucune interface utilisateur n’est affichée ou lorsque l’expérience de Windows standard n’est pas utilisée (par exemple, Media Center, des applications incorporées et l’invite de commandes). Cette option ignore la fonctionnalité expérience utilisateur fournie dans l’Assistant NDF, qui comprend la limitation des résultats aux causes de la prise en charge intégrale, ainsi que des heuristiques pour présenter les réparations à l’utilisateur dans l’ordre recommandé. Lorsque vous utilisez ces fonctions, vous devez fournir vous-même ces fonctionnalités. Vous devez également veiller à libérer de la mémoire utilisée par les résultats du diagnostic.

    Pour commencer le diagnostic, appelez la fonction [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) . Tous les problèmes détectés sont retournés à l’application sous la forme d’une collection de structures [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) décrivant les causes racines identifiées et les réparations possibles.

    Après avoir sélectionné une réparation (ou demandé à l’utilisateur de sélectionner une réparation), [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) doit être appelé pour tenter la réparation et déterminer si le problème a été résolu.

    Dans certains cas, une réparation peut être effectuée avec succès, mais ne résout pas le problème. Dans ce cas, il est recommandé de fermer l’incident existant et d’en ouvrir un nouveau. Cela permet de s’assurer que les nouveaux problèmes démasqués par la réparation initiale sont identifiés. Par exemple, supposez qu’aucun réseau sans fil n’avait été visible. Après la réinitialisation de l’adaptateur, les réseaux sans fil sont visibles, mais aucun d’eux n’est répertorié dans la liste par défaut. Il s’agit d’un nouveau problème qui nécessiterait un nouveau diagnostic pour identifier. Si une deuxième tentative de diagnostic n’identifie pas de problèmes supplémentaires, une réparation différente peut être tentée pour résoudre le problème d’origine, ou l’utilisateur peut être informé que le problème n’a pas pu être résolu.

    [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) et [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) sont des API synchrones. Si vous souhaitez annuler l’activité initiée par ces fonctions, appelez [**NdfCancelIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident) à partir d’un autre thread. La fonction retourne au point d’arrêt disponible suivant dans le processus de diagnostic ou de réparation.

    À tout moment, vous pouvez éventuellement appeler [**NdfGetTraceFile**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile) pour récupérer une copie du journal NDF pour la session de diagnostic en cours et l’inclure dans les journaux de vos applications. Le journal est vidé une fois récupéré, et les appels suivants récupèrent uniquement les événements qui se sont produits après le dernier appel à cette fonction.

## <a name="closing-an-incident"></a>Fermeture d’un incident

Lorsque vous avez terminé le diagnostic d’un incident, appelez [**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident) pour libérer des ressources système associées à l’exécution de diagnostics sur cet incident. (Notez que cela ne libère pas les objets créés par [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident).
