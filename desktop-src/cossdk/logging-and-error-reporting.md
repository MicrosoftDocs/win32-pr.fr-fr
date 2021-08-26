---
description: Journalisation et rapports d’erreurs
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Journalisation et rapports d’erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d974b4043b4365839aec6a4fae392ae1d84900e8b8347949147b8df13326bd1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990759"
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

 

 



