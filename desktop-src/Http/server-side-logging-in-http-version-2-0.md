---
title: Journalisation Server-Side
description: La journalisation côté serveur est disponible sur un groupe d’URL ou une session de serveur.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db8caf7475fe6d2b408f6e2a1f924bad73df64c315ef5e0acd1c7c317ce5eac6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829839"
---
# <a name="server-side-logging"></a>Journalisation Server-Side

La journalisation côté serveur est disponible sur un groupe d’URL ou une session de serveur. Lorsque la journalisation est activée sur une session de serveur, elle fonctionne comme une forme centralisée de journalisation pour tous les groupes d’URL sous la session serveur. Lorsque la journalisation est activée sur un groupe d’URL, la journalisation est exécutée uniquement sur les demandes routées vers le groupe d’URL. Les types de journalisation suivants sont pris en charge par l’API du serveur HTTP :

-   [Journalisation W3C](w3c-logging.md): disponible sur la session du serveur et le groupe d’URL.
-   [Journalisation du NCSA](ncsa-logging.md): disponible sur le groupe d’URL.
-   [Journalisation IIS](iis-logging.md): disponible sur le groupe d’URL.
-   [Journalisation centralisée binaire](centralized-binary-logging.md): disponible sur la session serveur.

Pour tirer parti de la fonctionnalité de journalisation HTTP, l’application active et configure un type de journalisation sur la session serveur ou le groupe d’URL. Pour plus d’informations, consultez [configuration et activation de la journalisation côté serveur](configuring-and-enabling-server-side-logging.md) .

 

 




