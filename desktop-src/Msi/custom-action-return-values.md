---
description: Si l’option de traitement de retour msidbCustomActionTypeContinue n’est pas définie, l’action personnalisée doit retourner un code d’État entier comme indiqué dans le tableau suivant.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valeurs de retour de l’action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530918"
---
# <a name="custom-action-return-values"></a>Valeurs de retour de l’action personnalisée

Si l’option de traitement de retour **msidbCustomActionTypeContinue** n’est pas définie, l’action personnalisée doit retourner un code d’État entier comme indiqué dans le tableau suivant.



| Valeur retournée                 | Description                           |
|------------------------------|---------------------------------------|
| fonction d’erreur \_ \_ non \_ appelée | Action non exécutée.                  |
| ERREUR de \_ réussite               | Actions terminées avec succès.       |
| ERREUR lors de l' \_ installation de \_ USEREXIT     | L’utilisateur s’est arrêté prématurément.          |
| ERREUR d' \_ installation \_      | Une erreur irrécupérable s’est produite.         |
| ERREUR \_ aucun \_ autre \_ élément       | Ignorer les actions restantes, et non pas une erreur. |



 

Notez que les actions personnalisées qui sont des [fichiers exécutables](executable-files.md) doivent retourner la valeur 0 en cas de réussite. Le programme d’installation interprète toute autre valeur de retour comme un échec. Pour ignorer les valeurs de retour, définissez l’indicateur de bit **msidbCustomActionTypeContinue** dans le champ type de la [table CustomAction](customaction-table.md).

Pour plus d’informations sur l’option **msidbCustomActionTypeContinue** et d’autres options de traitement des retours, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).

Notez que Windows Installer traduit les valeurs de retour de toutes les actions lorsqu’il écrit la valeur de retour dans le fichier journal. Par exemple, si la valeur de retour de l’action apparaît comme 1 dans le fichier journal, cela signifie que l’action a retourné une erreur de \_ réussite. Pour plus d’informations sur cette traduction, consultez [journalisation des valeurs de retour d’action](logging-of-action-return-values.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codes d’erreur](error-codes.md)
</dt> <dt>

[Journalisation des valeurs de retour d’action](logging-of-action-return-values.md)
</dt> </dl>

 

 



