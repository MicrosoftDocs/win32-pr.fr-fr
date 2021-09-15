---
description: Démarrage et récupération COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Démarrage et récupération COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403549"
---
# <a name="com-crm-startup-and-recovery"></a>Démarrage et récupération COM+ CRM

Si la case à cocher **activer les gestionnaires de ressources de compensation** est activée pour une application serveur (à l’aide de l’outil d’administration Services de composants, sous l’onglet **avancé** de la page de propriétés de l’application com+), la première fois qu’elle démarre, elle crée un fichier journal CRM qui sera utilisé par tous les composants CRM dans ce processus d’application serveur. (Pour obtenir des instructions détaillées sur la configuration de CRM, consultez [Configuration des composants CRM de com+](configuring-com--crm-components.md).)

Le nom du fichier journal CRM créé pour l’application serveur est basé sur l’AppId (un GUID) de l’application serveur, et le fichier journal CRM est placé dans le même répertoire que le fichier journal DTC (normalement, votre répertoire% SystemRoot% \\ winnt \\ system32 \\ DtcLog). Les fichiers journaux CRM portent l’extension. crmlog.

> [!Note]  
> Il peut être nécessaire de modifier l’emplacement par défaut d’un fichier journal CRM pour des raisons de performances (pour que le fichier journal DTC soit situé sur un disque différent de celui du fichier journal CRM) ou peut-être en raison de l’utilisation du CRM dans un environnement de cluster. L’emplacement des fichiers journaux CRM peut être modifié à l’aide du kit de développement logiciel (SDK) d’administration COM+. Le nom de la propriété est CRMLogFile, et il existe sur l’objet de collection d' [**applications**](applications.md) .

 

Lorsqu’une application serveur (compatible CRM) démarre et détecte qu’un fichier journal CRM existe déjà pour cette application serveur, elle effectue la récupération sur ce fichier journal CRM. La *récupération* est le processus qui consiste à effectuer toutes les transactions qui ont été interrompues par une défaillance et qui implique que l’infrastructure CRM lit le fichier journal CRM pour toutes les transactions qui n’ont pas été entièrement terminées. S’il en trouve, il contacte le DTC pour déterminer le résultat de la transaction. Il crée ensuite le compensateur CRM et transmet les notifications de validation ou d’abandon comme requis, ainsi que les enregistrements de journal associés.

Les notifications de préparation ne sont pas reçues par le compensateur CRM pendant la récupération. Le compensateur CRM a un indicateur pour déterminer s’il est appelé pendant un fonctionnement normal ou pendant la récupération.

La récupération trouvera normalement des transactions non terminées uniquement si l’application serveur a été arrêtée anormalement, en raison d’un blocage de processus d’application serveur ou d’un incident d’ordinateur. Si l’application serveur est autorisée à s’arrêter normalement, en raison de l’expiration du délai d’inactivité ou de l’arrêt manuel via l’outil d’administration Services de composants, le fichier journal est nettoyé.

Le démarrage d’une application de serveur CRM pour la récupération n’est pas initié automatiquement. Certaines actions externes doivent être effectuées pour démarrer l’application CRM Server où la récupération est requise. En général, cela crée un composant dans cette application serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Processus de fonctionnement COM+ CRM](com--crm-operating-process.md)
</dt> </dl>

 

 



