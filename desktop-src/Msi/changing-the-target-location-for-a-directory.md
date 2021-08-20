---
description: Si possible, la meilleure façon de spécifier l’emplacement cible d’un répertoire consiste à créer la table de répertoires dans votre package d’installation afin de fournir l’emplacement correct. Pour plus d’informations, consultez Utilisation de la table des répertoires.
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: Modification de l’emplacement cible d’un répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27adf952faeb4d37d5edb08a04bf25cc640d41e5d87732b30c80d25bba729705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145682"
---
# <a name="changing-the-target-location-for-a-directory"></a>Modification de l’emplacement cible d’un répertoire

Si possible, la meilleure façon de spécifier l’emplacement cible d’un répertoire consiste à créer la [table de répertoires](directory-table.md) dans votre package d’installation afin de fournir l’emplacement correct. Pour plus d’informations, consultez [utilisation de la table des répertoires](using-the-directory-table.md).

Si vous avez besoin de modifier l’emplacement du répertoire au moment de l’installation, vous disposez des options suivantes :

-   Spécifiez l’emplacement d’un répertoire en définissant la valeur d’une [propriété publique](public-properties.md) sur la ligne de commande. Au cours de l' [action CostFinalize](costfinalize-action.md), les chemins d’accès de répertoire internes utilisés par le programme d’installation sont mis à jour avec la valeur des propriétés répertoriées en tant que clés dans la [table de répertoire](directory-table.md). Pour plus d’informations, consultez [utilisation des propriétés](using-properties.md) et [définition des valeurs de propriété publiques sur la ligne de commande](setting-public-property-values-on-the-command-line.md).
-   Spécifiez l’emplacement d’un répertoire à l’aide d’une action personnalisée. Si l’action personnalisée doit être exécutée avant l' [action CostFinalize](costfinalize-action.md), vous pouvez utiliser un [type d’action personnalisé 51](custom-action-type-51.md) pour définir la valeur d’une propriété à partir d’une chaîne de texte mise en forme. Si l’action personnalisée s’exécute après l' [action CostFinalize](costfinalize-action.md), vous pouvez utiliser un [type d’action personnalisé 35](custom-action-type-35.md) pour définir la valeur du chemin d’accès du répertoire à partir d’une chaîne de texte mise en forme. Les actions personnalisées qui modifient l’une des [Propriétés du dossier système](property-reference.md) doivent être incluses dans les tables de séquence d’exécution (table [InstallExecuteSequence](installexecutesequence-table.md) ou [AdminExecuteSequence](adminexecutesequence-table.md)) et les tables de séquences de l’interface utilisateur (table [InstallUISequence](installuisequence-table.md) et [table AdminUISequence](adminuisequence-table.md)) afin que le dossier soit modifié au cours de l’installation [*complète*](f-gly.md) de l’interface utilisateur et de l’interface utilisateur de [*base*](b-gly.md) .
-   Si l’installation exécute une [*interface utilisateur complète*](f-gly.md), vous pouvez utiliser [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) ou [SetTargetPath ControlEvent,](settargetpath-controlevent.md) pour définir le chemin d’accès du répertoire. Vérifiez la propriété [**ProductState**](productstate.md) pour déterminer si le produit qui contient ce composant est déjà installé avant d’appeler **MsiSetTargetPath** ou SetTargetPath ControlEvent,. N’essayez pas de modifier le chemin d’accès au répertoire cible si certains composants qui utilisent ce chemin d’accès sont déjà installés pour l’utilisateur actuel ou un autre utilisateur.

Les restrictions suivantes s’appliquent à toutes les options ci-dessus :

-   N’essayez pas de modifier le chemin d’accès au répertoire cible si certains composants qui utilisent le chemin d’accès sont déjà installés pour l’utilisateur actuel ou pour un autre utilisateur.
-   N’essayez pas de modifier le chemin d’accès au répertoire cible pendant une [installation de maintenance](maintenance-installation.md).

 

 



