---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 35 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Type d’action personnalisé 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091805"
---
# <a name="custom-action-type-35"></a>Type d’action personnalisé 35

Cette action personnalisée définit le répertoire d’installation à partir d’une chaîne de texte mise en forme. Pour plus d’informations, consultez [modification de l’emplacement cible d’un répertoire](changing-the-target-location-for-a-directory.md) .

## <a name="source"></a>Source

Le champ source de la [table CustomAction](customaction-table.md) contient une clé dans la [table de répertoires](directory-table.md). Le répertoire désigné est défini par la chaîne mise en forme dans le champ cible à l’aide de [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha). Cela affecte au chemin d’accès cible et à la propriété associée la valeur développée de la chaîne de texte mise en forme dans le champ cible. N’essayez pas de modifier l’emplacement d’un répertoire cible lors de [l’installation](maintenance-installation.md)d’une maintenance. N’essayez pas de modifier le chemin d’accès au répertoire cible si certains composants qui utilisent ce chemin d’accès sont déjà installés pour tous les utilisateurs.

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.



| Constantes                                                              | Valeur hexadécimale | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory** | 0x023       | 35      |



 

## <a name="target"></a>Cible

La colonne cible de la [table CustomAction](customaction-table.md) contient une chaîne de texte mise en forme à l’aide de la fonctionnalité spécifiée dans [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sans les spécificateurs de champ numérique). Les paramètres à remplacer sont placés entre crochets \[ ... \] et peuvent être des propriétés, des variables d’environnement (% prefix), des chemins d’accès de fichier (préfixe \# ) ou des chemins d’accès de répertoire de composant ($ prefix). Notez que les chemins d’accès aux répertoires se terminent toujours par un séparateur de répertoire.

## <a name="return-processing-options"></a>Options de traitement des retours

L’action personnalisée n’utilise pas ces options.

## <a name="execution-scheduling-options"></a>Options de planification de l’exécution

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution. Ces options contrôlent l’exécution multiple des actions personnalisées. Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script les options d’exécution

L’action personnalisée n’utilise pas ces options.

## <a name="return-values"></a>Valeurs de retour

Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).

## <a name="remarks"></a>Notes

Si vous définissez une [propriété privée](private-properties.md) dans la séquence d’interface utilisateur en créant une action personnalisée dans l’une des tables de séquence de l’interface utilisateur, cette propriété n’est pas définie dans la séquence d’exécution. Pour définir la propriété dans la séquence d’exécution, vous devez également placer une action personnalisée dans une table de séquence d’exécution. Vous pouvez également faire de la propriété une [propriété publique](public-properties.md) et l’inclure dans la [**propriété SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> <dt>

[Actions personnalisées du texte mis en forme](formatted-text-custom-actions.md)
</dt> </dl>

 

 



