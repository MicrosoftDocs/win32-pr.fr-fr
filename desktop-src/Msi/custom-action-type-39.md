---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 39 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Type d’action personnalisé 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091793"
---
# <a name="custom-action-type-39"></a>Type d’action personnalisé 39

Le type d’action personnalisé 39 est utilisé avec les installations simultanées. Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public. Pour plus d’informations sur les installations simultanées, consultez [installations simultanées](concurrent-installations.md).

Tapez 39 action personnalisée pour installer une application publiée ou déjà installée. Ce type d’action personnalisé peut être utilisé pour réinstaller ou supprimer un produit qui a été installé en tant qu’installation simultanée par le package d’installation du produit actuel. L’action personnalisée de type 39 ne peut pas être utilisée pour réinstaller ou supprimer un produit précédemment installé par d’autres moyens. Par exemple, si le produit secondaire est installé à l’aide d’un type 39, de type 23 ou de l’action personnalisée de type 7 lors de l’installation du produit principal, une action personnalisée de type 39 peut être utilisée pour supprimer le produit secondaire lors de la désinstallation du produit principal.

## <a name="source"></a>Source

Le champ source de la [table CustomAction](customaction-table.md) contient le code de produit de l’application.

## <a name="numeric-type"></a>Type numérique



| Nom de type                                                     | Valeur |
|---------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory | 39    |



 

## <a name="target"></a>Cible

Le champ cible de la [table CustomAction](customaction-table.md) contient les paramètres de propriété qui doivent être passés à l’installation simultanée. Ces paramètres de propriété peuvent spécifier des fonctionnalités.

## <a name="return-processing-options"></a>Options de traitement des retours

Le type d’action personnalisé 39 échoue si l’application n’est pas publiée ou installée. Pour éviter ce problème, vous devez définir **msidbCustomActionTypeContinueflag**.

Une installation simultanée ne peut pas s’exécuter de façon asynchrone.

Consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Options de planification de l’exécution

Des indicateurs d’options sont disponibles pour contrôler l’exécution multiple potentielle des actions personnalisées. Consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script les options d’exécution

L’action personnalisée n’utilise pas cette option.

## <a name="return-values"></a>Valeurs de retour

L’état de retour de la sortie de l’utilisateur, de l’échec, de l’interruption ou de la réussite d’une installation simultanée est traité de la même façon que toute autre action. notez toutefois que Windows Installer traduit les valeurs de retour de toutes les actions quand il écrit la valeur de retour dans le fichier journal. Par exemple, si la valeur de retour de l’action apparaît comme 1 dans le fichier journal, cela signifie que l’action a retourné une erreur de \_ réussite. Pour plus d’informations, consultez [journalisation des valeurs de retour d’action](logging-of-action-return-values.md).

Notez que, si une installation simultanée a une **msidbCustomActionTypeContinue** définie, un retour de l’erreur d’installation de USEREXIT, une erreur d’installation de \_ \_ \_ \_ redémarrage, une erreur d' \_ installation de \_ redémarrage \_ maintenant ou une erreur de \_ redémarrage de la réussite \_ \_ requise est traitée comme une erreur de \_ réussite. Cela signifie que si vous définissez **msidbCustomActionTypeContinue** et que votre installation simultanée requiert un redémarrage, la nécessité du redémarrage sera ignorée. En outre, le code d’erreur de l’action personnalisée d’installation simultanée est ignoré.

Si **msidbCustomActionTypeContinue** n’est pas défini, les codes de retour suivants plus la réussite de l’erreur \_ sont traités comme des succès et ont les significations suivantes. Les autres codes de retour sont traités comme des échecs.



| Message                          | Signification                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| ERREUR d' \_ installation de \_ redémarrage           | L’indicateur de redémarrage sera configuré pour redémarrer à la fin de l’installation.                                  |
| ERREUR d' \_ installation de \_ redémarrage \_ maintenant      | Un redémarrage est nécessaire avant de terminer l’installation. Le redémarrage sera traité immédiatement. |
| ERREUR \_ de \_ redémarrage de la réussite \_ obligatoire | Un redémarrage était nécessaire, mais a été supprimé.                                                          |



 

## <a name="remarks"></a>Notes

Une expression conditionnelle est requise pour activer l’installation simultanée au niveau de l’installation ou de la suppression du composant ou de la fonctionnalité associé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Installations simultanées](concurrent-installations.md)
</dt> <dt>

[Référence des actions personnalisées](custom-action-reference.md)
</dt> <dt>

[À propos des actions personnalisées](about-custom-actions.md)
</dt> <dt>

[Utilisation d’actions personnalisées](using-custom-actions.md)
</dt> </dl>

 

 



