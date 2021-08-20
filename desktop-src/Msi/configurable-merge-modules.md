---
description: Les modules de fusion (fichiers. msm) peuvent être créés pour contenir des attributs qui peuvent être configurés par le consommateur du module de fusion.
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: Modules de fusion configurables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ca110b45e1ec9bd28662c24440124bb75d0dde73d6e425146e8be640ae2de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144268"
---
# <a name="configurable-merge-modules"></a>Modules de fusion configurables

Les modules de fusion (fichiers. msm) peuvent être créés pour contenir des attributs qui peuvent être configurés par le consommateur du module de fusion. Cela permet de configurer le module de fusion au moment où le package d’installation et le module sont fusionnés et installés par l’utilisateur final. les modules de fusion configurables requièrent Mergemod.dll version 2,0, mais ils peuvent s’exécuter sur n’importe quelle version du Windows Installer.

L’implémentation de modules de fusion configurables se compose de deux parties. Tout d’abord, lors de la création du module de fusion (fichier. msm), l’auteur du module de fusion ajoute des informations à la base de données du module qui spécifie les éléments qui peuvent être modifiés et la façon dont ces éléments peuvent être configurés par l’utilisateur du module. L’auteur ajoute des entrées aux [tables de base de données de module de fusion](merge-module-database-tables.md) qui sont réservées aux informations configurables ([table ModuleConfiguration](moduleconfiguration-table.md) et [table ModuleSubstitution](modulesubstitution-table.md)), met à jour la [ \_ table de validation](-validation-table.md)et ajoute des entrées pour les tables de module de fusion configurables à la [table ModuleIgnoreTable](moduleignoretable-table.md). Les ajouts à la table ModuleIgnore sont nécessaires pour rendre le module compatible avec les versions de Mergemod.dll antérieures à 2,0.

Deuxièmement, lors de la fusion du module dans un package d’installation (fichier .msi), l’utilisateur final du module utilise un outil de fusion. L’outil de fusion appelle Mergemod.dll pour exposer les informations de configuration du module à un outil de configuration du client. L’outil de configuration peut interagir avec l’utilisateur final, mais il n’est pas nécessaire pour exposer toutes les options de configuration possibles. Si l’utilisateur refuse de fournir une sélection pour un élément configurable, le module peut fournir une valeur par défaut. Une fois que l’utilisateur a effectué les sélections de l’outil de configuration, l’outil de fusion appelle Mergemod.dll pour effectuer la fusion.

Les modules de fusion configurables sont entièrement compatibles avec les outils antérieurs à la version 2,0 de Mergemod.dll. Dans ce cas, l’outil utilise les valeurs par défaut du module.

Pour plus d’informations, consultez [utilisation des modules de fusion configurables](using-configurable-merge-modules.md).

 

 



