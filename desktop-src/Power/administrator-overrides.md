---
description: Remplacements de l’administrateur
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Remplacements de l’administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531943"
---
# <a name="administrator-overrides"></a>Remplacements de l’administrateur

Windows dispose d’une seule liste de contrôle d’accès (ACL) par défaut sur tous les objets de stratégie d’alimentation. La liste de contrôle d’accès accorde des autorisations de lecture, d’écriture et de modification aux membres du groupe utilisateurs authentifiés. L’autorisation lecture seule est accordée à tous les autres utilisateurs. Les applications qui appellent des fonctions de stratégie d’alimentation peuvent déterminer si un utilisateur dispose d’autorisations pour un paramètre d’alimentation spécifié à l’aide de la fonction [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .

Les paramètres d’alimentation peuvent être remplacés via stratégie de groupe. Les remplacements peuvent être définis via la stratégie de groupe de domaine ou la stratégie de groupe locale. [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) indique si un paramètre d’alimentation spécifié a une substitution de stratégie de groupe.

L’outil de ligne de commande **PowerCfg.exe** affiche un message d’erreur lorsqu’une commande ne peut pas être exécutée soit parce que l’utilisateur n’a pas les autorisations nécessaires pour modifier le paramètre d’alimentation, soit parce que le paramètre d’alimentation a une substitution de stratégie de groupe.

L’application options d’alimentation du panneau de configuration ne prend pas en charge la configuration des autorisations d’accès à la stratégie d’alimentation. La modification des autorisations doit être effectuée via **PowerCfg.exe**.

 

 



