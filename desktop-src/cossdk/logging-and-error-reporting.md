---
description: Journalisation et rapports d’erreurs
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Journalisation et rapports d’erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514548"
---
# <a name="logging-and-error-reporting"></a>Journalisation et rapports d’erreurs

## <a name="log-file"></a>Fichier journal

COMREPL génère un fichier journal contenant les messages d’État et d’erreur. Ce fichier est stocké sur l’ordinateur où COMREPL a été lancé dans% systemdir% \\ com \\ Replication \\ comrepl. log.

Ce fichier journal est effacé au démarrage d’une phase de copie. L’installation suivante sur les cibles sera ajoutée au fichier.

## <a name="error-handling"></a>Gestion des erreurs

Les erreurs sont signalées dans le fichier journal décrit ci-dessus. Des informations détaillées sur l’erreur sont également disponibles dans le journal des événements sur les ordinateurs source ou cible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des fichiers](file-management.md)
</dt> <dt>

[Phases de réplication](replication-phases.md)
</dt> <dt>

[Utilisation de COMREPL](using-comrepl.md)
</dt> <dt>

[Ce qui est répliqué](what-gets-replicated.md)
</dt> </dl>

 

 



