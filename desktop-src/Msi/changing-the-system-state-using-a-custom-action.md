---
description: Les actions personnalisées destinées à changer l’état du système doivent être des actions personnalisées d’exécution différée.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Modification de l’état du système à l’aide d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529796"
---
# <a name="changing-the-system-state-using-a-custom-action"></a>Modification de l’état du système à l’aide d’une action personnalisée

Les actions personnalisées destinées à changer l’état du système doivent être des actions personnalisées d’exécution différée. Les actions personnalisées qui définissent les propriétés, les États des fonctionnalités, les États des composants ou les répertoires cibles, ou planifient les opérations système en insérant des lignes dans des tables de séquence peuvent utiliser l’exécution immédiate en toute sécurité. Toutefois, les actions personnalisées qui modifient directement le système ou appellent un autre service système doivent être différées à l’heure d’exécution du script d’installation. Pour plus d’informations, consultez [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md).

Vous ne devez pas essayer d’utiliser une action personnalisée d’exécution immédiate pour modifier l’état du système, car chaque action personnalisée qui modifie l’État doit avoir une action personnalisée de restauration correspondante pour annuler la modification de l’état du système lors d’une restauration de l’installation. Toutes les actions personnalisées de restauration sont également des actions personnalisées différées et doivent précéder l’action qu’elles annulent. Pour plus d’informations, consultez [restaurer des actions personnalisées](rollback-custom-actions.md).

 

 



