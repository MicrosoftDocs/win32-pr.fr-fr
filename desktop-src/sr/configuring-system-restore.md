---
title: Configuration de la restauration du système
description: La restauration du système utilise Windows Management Instrumentation (WMI) pour fournir un moyen scriptable de configurer et d’utiliser ses fonctionnalités. Il expose deux classes, SystemRestore et SystemRestoreConfig, dans l' \\ espace de noms racine par défaut.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382195"
---
# <a name="configuring-system-restore"></a>Configuration de la restauration du système

La restauration du système utilise [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) pour fournir un moyen scriptable de configurer et d’utiliser ses fonctionnalités. Il expose deux classes, [**SystemRestore**](systemrestore.md) et [**SystemRestoreConfig**](systemrestoreconfig.md), dans l' \\ espace de noms racine par défaut.

La classe [**SystemRestore**](systemrestore.md) fournit des méthodes pour les tâches suivantes :

-   Désactivation et activation de l’analyse
-   Liste des points de restauration disponibles
-   Lancement d’une restauration sur le système local
-   Récupération de l’état de la dernière restauration du système

La classe [**SystemRestoreConfig**](systemrestoreconfig.md) fournit des propriétés pour contrôler la fréquence de création de points de restauration planifiés et la quantité d’espace disque consommée par la restauration du système sur chaque lecteur.

Vous pouvez accéder aux deux classes à distance à l’aide des techniques WMI standard. Pour obtenir une description complète de WMI, consultez [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).

 

 