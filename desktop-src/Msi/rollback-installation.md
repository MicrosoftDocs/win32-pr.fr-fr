---
description: lorsque le Windows Installer traite le script d’installation pour l’installation d’un produit ou d’une application, il génère simultanément un script de restauration et enregistre une copie de chaque fichier supprimé au cours de l’installation.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Restauration de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276cec7d16cf5344a778dfb894d7e03e81190be42cb10f4438f128a2c3d1fed6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039889"
---
# <a name="rollback-installation"></a>Restauration de l’installation

lorsque le Windows Installer traite le script d’installation pour l’installation d’un produit ou d’une application, il génère simultanément un script de restauration et enregistre une copie de chaque fichier supprimé au cours de l’installation. Ces fichiers sont conservés dans un répertoire système masqué et sont automatiquement supprimés une fois l’installation terminée. Toutefois, si l’installation échoue, le programme d’installation effectue automatiquement une restauration qui rétablit l’état d’origine du système.

La restauration automatique d’une installation ayant échoué est le comportement par défaut du programme d’installation. Pour désactiver la restauration au cours d’une installation, utilisez l’une des options suivantes :

-   [**Propriété DISABLEROLLBACK**](-disablerollback.md)
-   [**Propriété PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [Action DisableRollback](disablerollback-action.md)
-   [DisableRollback](disablerollback.md)
-   [EnableRollback ControlEvent,](enablerollback-controlevent.md)

Chaque fois que la restauration est désactivée, le programme d’installation définit la propriété [**RollbackDisabled**](rollbackdisabled.md) .

Si une installation utilise des [actions personnalisées](custom-actions.md), une création supplémentaire du package d’installation est nécessaire pour utiliser la fonctionnalité de restauration. Pour plus d’informations, consultez [restaurer des actions personnalisées](rollback-custom-actions.md).

 

 



