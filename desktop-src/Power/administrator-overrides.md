---
description: Remplacements de l’administrateur
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Remplacements de l’administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af73f6d6fe3fe7d4edb8272c4d39c385a84973e4a3263c448505f5235adec855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033019"
---
# <a name="administrator-overrides"></a>Remplacements de l’administrateur

Windows possède une seule liste de contrôle d’accès (ACL) par défaut sur tous les objets de stratégie d’alimentation. La liste de contrôle d’accès accorde des autorisations de lecture, d’écriture et de modification aux membres du groupe utilisateurs authentifiés. L’autorisation lecture seule est accordée à tous les autres utilisateurs. Les applications qui appellent des fonctions de stratégie d’alimentation peuvent déterminer si un utilisateur dispose d’autorisations pour un paramètre d’alimentation spécifié à l’aide de la fonction [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .

Les paramètres d’alimentation peuvent être remplacés via stratégie de groupe. Les remplacements peuvent être définis via la stratégie de groupe de domaine ou la stratégie de groupe locale. [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) indique si un paramètre d’alimentation spécifié a une substitution de stratégie de groupe.

L’outil de ligne de commande **PowerCfg.exe** affiche un message d’erreur lorsqu’une commande ne peut pas être exécutée soit parce que l’utilisateur n’a pas les autorisations nécessaires pour modifier le paramètre d’alimentation, soit parce que le paramètre d’alimentation a une substitution de stratégie de groupe.

L’application options d’alimentation du panneau de configuration ne prend pas en charge la configuration des autorisations d’accès à la stratégie d’alimentation. La modification des autorisations doit être effectuée via **PowerCfg.exe**.

 

 



