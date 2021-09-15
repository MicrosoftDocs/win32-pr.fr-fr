---
description: Ce qui est répliqué
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Ce qui est répliqué
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403663"
---
# <a name="what-gets-replicated"></a>Ce qui est répliqué

## <a name="applications"></a>Applications

Toutes les applications installées sur l’ordinateur source sont répliquées, à l’exception des suivantes :

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Éléments et dépendances non-COM + application
</dt> <dd>

L’administrateur est chargé de répliquer tout ce dont dépend une application COM+, mais qui ne fait pas correctement partie de l’application elle-même, comme les fichiers de données et les dll. COMREPL ne réplique rien en dehors des éléments de l’application COM+.

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Applications préinstallées par COM+
</dt> <dd>

Les applications qui sont utilisées en interne par COM+ et qui sont installées via le programme d’installation de COM+ ne sont pas répliquées. Leurs thèmes sont les suivants :

-   Application système
-   Utilitaires COM+
-   Écouteur de file d’attente de lettres mortes QC COM+

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applications créées par IIS
</dt> <dd>

Ces applications ne sont pas répliquées et incluent les éléments suivants :

-   Applications IIS in-process
-   Utilitaires IIS
-   Toutes les applications créées pour les racines virtuelles isolées ou regroupées

</dd> </dl>

## <a name="computer-list"></a>Liste des ordinateurs

Les ordinateurs distants nommés dans le dossier **ordinateurs** de l’outil d’administration Services de composants ne seront pas répliqués à partir de la source vers l’ordinateur cible.

## <a name="properties"></a>Propriétés

Les propriétés de collection **LocalComputer** suivantes sont répliquées :

-   TransactionTimeout
-   ResourcePoolingEnabled
-   DCOMEnabled
-   DefaultAuthenticationLevel
-   DefaultImpersonationLevel
-   SecurityTrackingEnabled
-   CISEnabled
-   SecureReferencesEnabled
-   InternetPortsListed
-   DeafultToInternetPorts
-   Ports
-   RpcProxyEnabled

Les propriétés de collection **LocalComputer** suivantes ne sont pas répliquées :

-   Description
-   ApplicationProxyRSN
-   IsRouter

Pour obtenir une description des propriétés de la collection **LocalComputer** , consultez [**LocalComputer**](localcomputer.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des fichiers](file-management.md)
</dt> <dt>

[Journalisation et rapports d’erreurs](logging-and-error-reporting.md)
</dt> <dt>

[Phases de réplication](replication-phases.md)
</dt> <dt>

[Utilisation de COMREPL](using-comrepl.md)
</dt> </dl>

 

 



