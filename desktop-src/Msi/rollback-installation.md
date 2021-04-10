---
description: Lorsque le Windows Installer traite le script d’installation pour l’installation d’un produit ou d’une application, il génère simultanément un script de restauration et enregistre une copie de chaque fichier supprimé au cours de l’installation.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Restauration de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114550"
---
# <a name="rollback-installation"></a>Restauration de l’installation

Lorsque le Windows Installer traite le script d’installation pour l’installation d’un produit ou d’une application, il génère simultanément un script de restauration et enregistre une copie de chaque fichier supprimé au cours de l’installation. Ces fichiers sont conservés dans un répertoire système masqué et sont automatiquement supprimés une fois l’installation terminée. Toutefois, si l’installation échoue, le programme d’installation effectue automatiquement une restauration qui rétablit l’état d’origine du système.

La restauration automatique d’une installation ayant échoué est le comportement par défaut du programme d’installation. Pour désactiver la restauration au cours d’une installation, utilisez l’une des options suivantes :

-   [**Propriété DISABLEROLLBACK**](-disablerollback.md)
-   [**Propriété PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [Action DisableRollback](disablerollback-action.md)
-   [DisableRollback](disablerollback.md)
-   [EnableRollback ControlEvent,](enablerollback-controlevent.md)

Chaque fois que la restauration est désactivée, le programme d’installation définit la propriété [**RollbackDisabled**](rollbackdisabled.md) .

Si une installation utilise des [actions personnalisées](custom-actions.md), une création supplémentaire du package d’installation est nécessaire pour utiliser la fonctionnalité de restauration. Pour plus d’informations, consultez [restaurer des actions personnalisées](rollback-custom-actions.md).

 

 



