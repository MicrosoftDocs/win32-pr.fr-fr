---
title: Configuration de la restauration du système
description: la restauration du système utilise Windows Management Instrumentation (WMI) pour fournir un moyen scriptable de configurer et d’utiliser ses fonctionnalités. Il expose deux classes, SystemRestore et SystemRestoreConfig, dans l' \\ espace de noms racine par défaut.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5627233d22025d8cead43f9fc31323ae13f85ff2ec7bde0ebfa07e171c1f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968048"
---
# <a name="configuring-system-restore"></a>Configuration de la restauration du système

la restauration du système utilise [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) pour fournir un moyen scriptable de configurer et d’utiliser ses fonctionnalités. Il expose deux classes, [**SystemRestore**](systemrestore.md) et [**SystemRestoreConfig**](systemrestoreconfig.md), dans l' \\ espace de noms racine par défaut.

La classe [**SystemRestore**](systemrestore.md) fournit des méthodes pour les tâches suivantes :

-   Désactivation et activation de l’analyse
-   Liste des points de restauration disponibles
-   Lancement d’une restauration sur le système local
-   Récupération de l’état de la dernière restauration du système

La classe [**SystemRestoreConfig**](systemrestoreconfig.md) fournit des propriétés pour contrôler la fréquence de création de points de restauration planifiés et la quantité d’espace disque consommée par la restauration du système sur chaque lecteur.

Vous pouvez accéder aux deux classes à distance à l’aide des techniques WMI standard. pour obtenir une description complète de WMI, consultez [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).

 

 