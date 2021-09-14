---
description: L’objectif d’une action personnalisée d’exécution différée est de retarder l’exécution d’une modification du système au moment de l’exécution du script d’installation.
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: Actions personnalisées d’exécution différée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09b91793f5d5bbc7be7099c92f8d8f212012d12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091650"
---
# <a name="deferred-execution-custom-actions"></a>Actions personnalisées d’exécution différée

L’objectif d’une action personnalisée d’exécution différée est de retarder l’exécution d’une modification du système au moment de l’exécution du script d’installation. Cela diffère d’une action personnalisée normale, ou d’une action standard, dans laquelle le programme d’installation exécute l’action immédiatement lorsqu’il le rencontre dans une table de séquence ou dans un appel à [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). Une action personnalisée d’exécution différée permet à l’auteur d’un package de spécifier des opérations système à un point particulier au sein de l’exécution du script d’installation.

Le programme d’installation n’exécute pas d’action personnalisée d’exécution différée au moment du traitement de la séquence d’installation. Au lieu de cela, le programme d’installation écrit l’action personnalisée dans le script d’installation. Le seul paramètre de mode défini par le programme d’installation dans ce cas est MSIRUNMODE \_ planifié. Pour obtenir une description des paramètres du mode d’exécution, consultez [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .

Une action personnalisée d’exécution différée doit être planifiée dans la table des séquences d’exécution de la section qui effectue la génération de scripts. Les actions personnalisées d’exécution différée doivent être postérieures à [InstallInitialize](installinitialize-action.md) et précéder [InstallFinalize](installfinalize-action.md) dans la séquence d’action.

Les actions personnalisées qui définissent les propriétés, les États des fonctionnalités, les États des composants ou les répertoires cibles, ou qui planifient les opérations système en insérant des lignes dans des tables de séquence, peuvent, dans de nombreux cas, utiliser l’exécution immédiate en toute sécurité. Toutefois, les actions personnalisées qui modifient directement le système ou appellent un autre service système doivent être différées à l’heure d’exécution du script d’installation. Consultez [actions personnalisées synchrones et asynchrones](synchronous-and-asynchronous-custom-actions.md) pour plus d’informations sur les conflits potentiels entre leurs actions personnalisées et le thread d’installation principal.

Étant donné que le script d’installation peut être exécuté en dehors de la session d’installation dans laquelle il a été écrit, la session n’existe peut-être plus pendant l’exécution du script d’installation. Cela signifie que le handle de session d’origine et le jeu de données de propriété pendant la séquence d’installation ne sont pas disponibles pour une action personnalisée d’exécution différée. Les actions personnalisées différées qui appellent des bibliothèques de liens dynamiques (dll) passent un handle qui ne peut être utilisé que pour obtenir une quantité très limitée d’informations, comme décrit dans [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).

Notez que les actions personnalisées différées, y compris les actions personnalisées de [restauration](rollback-custom-actions.md) et de [validation des actions personnalisées](commit-custom-actions.md), sont les seuls types d’actions qui peuvent s’exécuter en dehors du contexte de sécurité des utilisateurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Options d’exécution d’une action personnalisée In-Script](custom-action-in-script-execution-options.md)
</dt> <dt>

[Référence des actions personnalisées](custom-action-reference.md)
</dt> </dl>

 

 



