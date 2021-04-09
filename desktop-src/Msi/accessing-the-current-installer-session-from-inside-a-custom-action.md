---
description: Les actions personnalisées non différées qui appellent des bibliothèques de liens dynamiques ou des scripts peuvent accéder à une installation en cours d’exécution pour interroger ou modifier les attributs de la session d’installation actuelle.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Accès à la session de programme d’installation actuelle à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951803"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>Accès à la session de programme d’installation actuelle à partir d’une action personnalisée

Les actions personnalisées non différées qui appellent des [bibliothèques de liens dynamiques](dynamic-link-libraries.md) ou des [scripts](scripts.md) peuvent accéder à une installation en cours d’exécution pour interroger ou modifier les attributs de la session d’installation actuelle. Un seul objet de **session** peut exister pour chaque processus, et les scripts d’action personnalisés ne doivent pas essayer de créer une autre session.

Les actions personnalisées peuvent uniquement ajouter, modifier ou supprimer des lignes, des colonnes ou des tables temporaires dans une base de données. Les actions personnalisées ne peuvent pas modifier les données persistantes dans une base de données, par exemple les données qui font partie de la base de données stockée sur le disque.

[Bibliothèques de liens dynamiques](dynamic-link-libraries.md)

Pour accéder à une installation en cours d’exécution, les actions personnalisées qui appellent des bibliothèques de liens dynamiques (DLL) sont passées à un handle du type MSIHANDLE pour la session active en tant que seul argument du point d’entrée de la DLL nommé dans la colonne cible de la [table CustomAction](customaction-table.md). Étant donné que le programme d’installation fournit ce handle, l’action personnalisée ne doit pas la fermer, par exemple pour recevoir le handle *hInstall* du programme d’installation, la fonction d’action personnalisée est déclarée comme suit.


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Pour un accès en lecture seule à la base de données actuelle, obtenez le handle de base de données en appelant [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase). Pour plus d’informations, consultez [obtention d’un descripteur de base de données](obtaining-a-database-handle.md).

[Scripts](scripts.md)

Les actions personnalisées écrites en VBScript ou JScript peuvent accéder à la session d’installation actuelle à l’aide de l' [**objet session**](session-object.md). Le programme d’installation crée un objet de **session** nommé « session » qui fait référence à l’installation actuelle. Pour un accès en lecture seule à la base de données actuelle, utilisez la propriété [**Database**](session-database.md) de l’objet **session** .

Étant donné qu’un script est exécuté à partir du contexte de l’objet [**session**](session-object.md) , il n’est pas toujours nécessaire de qualifier entièrement les propriétés et les méthodes. Dans l’exemple suivant, quand vous utilisez VBScript, la référence me peut remplacer l’objet de **session** , par exemple, les trois lignes suivantes sont équivalentes.


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[Fichiers exécutables](executable-files.md)

Vous ne pouvez pas accéder à la session de programme d’installation actuelle à partir d’actions personnalisées qui appellent des fichiers exécutables lancés avec une ligne de commande, par exemple, [type d’action personnalisée 2](custom-action-type-2.md) et [type d’action personnalisé 18](custom-action-type-18.md).

[Actions personnalisées d’exécution différée](deferred-execution-custom-actions.md)

Vous ne pouvez pas accéder à la session du programme d’installation en cours ou à toutes les données de propriété à partir d’une action personnalisée d’exécution différée. Pour plus d’informations, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès à une base de données ou à une session à partir d’une action personnalisée](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



