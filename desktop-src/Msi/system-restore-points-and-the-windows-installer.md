---
description: La restauration du système surveille et enregistre automatiquement les modifications système principales sur l’ordinateur d’un utilisateur. Pour plus d’informations, consultez restauration du système.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Points de restauration système et Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b8de832208f2bee301a1a159da058ba0f97cf2ecbd74892cb809e1186fbb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624091"
---
# <a name="system-restore-points-and-the-windows-installer"></a>Points de restauration système et Windows Installer

La restauration du système surveille et enregistre automatiquement les modifications système principales sur l’ordinateur d’un utilisateur. Pour plus d’informations, consultez [restauration du système](../sr/system-restore-portal.md).

les points de restauration système sont créés par le système et sont également créés par Windows Installer lors de l’installation ou de la suppression d’un logiciel.

sur Windows XP, le programme d’installation peut créer des points de contrôle lors de la première installation d’une application et pendant sa suppression. Le programme d’installation crée uniquement des points de contrôle dans ce cas lorsque la modification est exécutée avec au moins une [*interface utilisateur de base*](b-gly.md). Les installations dont le [niveau d’interface utilisateur](user-interface-levels.md) est défini sur aucun sont généralement initiées par le système ou par une application qui doit gérer la création d’un point de contrôle. Pour plus d’informations, consultez [restauration du système](../sr/system-restore-portal.md).

Dans les entreprises avec de nombreuses petites applications, les administrateurs peuvent décider de désactiver les points de contrôle dans le programme d’installation pour améliorer les performances. Pour plus d’informations, consultez [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) ou [définition d’un point de restauration à partir d’une action personnalisée](setting-a-restore-point-from-a-custom-action.md).

à partir de Windows Installer 5,0, la propriété [**MSIFASTINSTALL**](msifastinstall.md) peut être définie pour empêcher une installation de générer un point de restauration système.

 

 
