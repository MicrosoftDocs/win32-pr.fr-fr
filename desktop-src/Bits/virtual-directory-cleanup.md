---
title: Nettoyage de répertoire virtuel
description: BITS étend les répertoires virtuels IIS pour prendre en charge les téléchargements.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941159"
---
# <a name="virtual-directory-cleanup"></a>Nettoyage de répertoire virtuel

BITS étend les répertoires virtuels IIS pour prendre en charge les téléchargements. Chaque répertoire virtuel a une propriété de délai d’expiration de session (la propriété de métabase IIS [BITSSessionTimeout](bits-iis-extension-properties.md) ) qui spécifie la période pendant laquelle le client bits doit progresser dans le téléchargement du fichier. Si aucune progression n’est effectuée pendant cette période (la minuterie est réinitialisée lorsque la progression est effectuée), le service BITS ferme la session. Le délai d’expiration de session par défaut est de 14 jours.

BITS ajoute un élément de travail au [Planificateur de tâches](/windows/desktop/TaskSchd/task-scheduler-start-page) pour chaque répertoire virtuel que vous créez et activez. L’élément de travail supprime les ressources associées aux sessions fermées. Par défaut, le nettoyage se produit toutes les 12 heures. Si deux répertoires virtuels pointent vers le même répertoire physique, le processus de nettoyage initié par l’un des répertoires supprime les ressources associées à toutes les sessions fermées dans le répertoire physique.

Utilisez l’onglet extension BITS ou les interfaces [Planificateur de tâches](/windows/desktop/TaskSchd/task-scheduler-start-page) pour modifier la planification de nettoyage en fonction de votre application. Vous pouvez également appeler la méthode [**IBITSExtensionSetup :: GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) pour récupérer un pointeur d’interface vers la tâche de nettoyage associée au répertoire virtuel.

> [!Note]  
> Si le Planificateur de tâches est désactivé une fois que le répertoire virtuel est activé, le processus de nettoyage du répertoire virtuel ne fonctionnera pas.

 

 

 