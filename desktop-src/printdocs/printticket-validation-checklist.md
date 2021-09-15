---
description: Passez en revue la liste de vérification de validation PrintTicket. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: Liste de contrôle de validation PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6154b7cabb5825a0f0edcc8f90b8294557001f1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521401"
---
# <a name="printticket-validation-checklist"></a>Liste de contrôle de validation PrintTicket

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Les fournisseurs PrintTicket doivent valider le PrintTicket avant de l’utiliser à quelque fin que ce soit. Une fois le PrintTicket validé, il peut être retourné au client, ou il peut être ignoré après utilisation. Cette liste de vérification couvre les tâches que le fournisseur doit effectuer pendant la validation. Le processus de validation modifie fréquemment le contenu du PrintTicket, bien qu’il ne modifie pas un PrintTicket précédemment validé.

La validation est toujours effectuée sur un appareil spécifique qui possède un ensemble de fonctionnalités, d’options et d’instances ParameterDef définies dans un document PrintCapabilities. Le code de validation doit avoir accès à l’ensemble des instances de fonctionnalité (et aux instances de l’option contenue) et aux instances ParameterDef pour l’appareil spécifique, et n’a pas besoin d’accéder au PrintCapabilities. Les informations des instances Feature, option et ParameterDef sont nécessaires dans certaines parties du processus de validation.

1.  Pendant les tentatives de localisation des éléments correspondants ou correspondants, Notez que les espaces de noms des éléments doivent correspondre avant qu’un nom qualifié puisse être considéré comme une correspondance. Tous les noms d’éléments, les noms d’attributs et les noms d’instance sont qualifiés par un espace de noms. Pour les éléments imbriqués, leurs emplacements doivent correspondre avant que les éléments soient considérés comme une correspondance.

2.  Vérifiez que toutes les balises d’élément se trouvent dans l’espace de noms public, sont définies par le schéma PrintTicket, contiennent les attributs XML et les valeurs d’attributs appropriés, et que l’emplacement de chaque type d’élément est conforme à l’utilisation définie par le schéma PrintTicket.

3.  Déterminez tous les espaces de noms signalés par le document PrintCapabilities. Supprimer tous les éléments (et leurs descendants) du PrintTicket dont les noms d’instance appartiennent à des espaces de noms qui ne sont pas signalés par un document PrintCapabilities. Notez la différence entre ce cas et le cas suivant, qui implique des noms d’instance non reconnus dans un espace de noms connu.

4.  En raison du fait que les schémas sont continuellement étendus avec l’ajout de nouvelles définitions d’instance d’élément, le code de validation ne doit pas être écrit en partant du principe que chaque nom d’instance dans un espace de noms donné est connu. Le code de validation ne peut pas traiter les noms d’instance non reconnus dans un espace de noms connu comme des erreurs, ni les supprimer du PrintTicket.

5.  Si une instance d’élément a un frère dupliqué qui n’est pas autorisé par le schéma PrintTicket, conservez uniquement la première occurrence et supprimez les doublons, y compris le contenu de l’élément dupliqué.

6.  Supprimez de l’PrintTicket toute fonctionnalité ou sous-fonctionnalité (et tous ses enfants) qui n’a pas de fonctionnalité correspondante dans le document PrintCapabilities.

7.  Vérifiez la propriété SelectionType définie dans le document PrintCapabilities pour chacune des instances de fonctionnalités restantes dans PrintTicket. Toute fonctionnalité dont la propriété SelectionType a la valeur PickOne doit avoir exactement une instance option présente dans PrintTicket, alors qu’une fonctionnalité dont la propriété SelectionType est PickMany peut en avoir plusieurs. Si une fonctionnalité PrintTicket n’a pas d’instance d’option, fournissez l’instance d’option par défaut. Étant donné que vous êtes le fournisseur, vous savez quelle option est l’option par défaut pour chaque fonctionnalité.

    Pour une fonctionnalité dont la propriété SelectionType est PickMany, avec plusieurs options sélectionnées dans le PrintTicket, vérifiez qu’aucune option n’est désignée comme IdentityOption. Si c’est le cas, supprimez toutes les autres options, en laissant uniquement le IdentityOption désigné.

8.  Supprimez toute instance ParameterInit dans PrintTicket qui n’a pas d’instance ParameterDef correspondante dans le document PrintCapabilities.

    Pour toute autre instance ParameterInit dans PrintTicket, vérifiez que la valeur de chaque est conforme à l’instance ParameterDef du document PrintCapabilities. Si une valeur est manquante, fournissez la valeur par défaut fournie dans le ParameterDef.

9.  Couplez chaque instance d’option dans PrintTicket avec une option figurant dans la fonctionnalité correspondante dans le document PrintCapabilities, en fonction des résultats du processus de notation. Le score est le processus qui consiste à rechercher dans le document PrintCapabilities l’option qui correspond le mieux à l’option nommée dans PrintTicket. Pour obtenir une description de ce qui est pris en compte au cours du processus de calcul de score, consultez [définitions d’options](option-definitions.md). Remplacez chaque option de référence dans PrintTicket par l’option de document le plus approprié possible pour les informations PrintCapabilities correspondantes. Vous pouvez également classer tous les candidats par score et transmettre ces informations à l’étape de résolution au cas où un conflit de contrainte empêche l’utilisation du candidat le plus approprié. Dans ce cas, le processus de résolution peut utiliser le deuxième-meilleur candidat plutôt que de choisir un autre candidat aléatoire.

10. Pour une fonctionnalité dont la propriété SelectionType est définie sur PickMany, et qui a plusieurs options sélectionnées dans PrintTicket, vérifiez qu’aucune option n’est désignée comme IdentityOption. Si une telle option existe, supprimez toutes les autres options, en laissant uniquement la IdentityOption désignée. Cette étape doit être effectuée avant et après l’application du processus de calcul de score.

    La raison pour laquelle cette étape doit être effectuée à deux reprises est qu’il est possible que le processus de notation mappe plusieurs instances d’option de référence à la même option de candidat. Si cela se produit, supprimez toutes les instances d’option dupliquées afin que les options répertoriées pour une fonctionnalité PickMany particulière soient uniques.

11. Ajoutez à l’élément PrintTicket toute fonctionnalité présente dans le document PrintCapabilities qui n’apparaît pas dans PrintTicket. Pour une telle fonctionnalité, choisissez l’option par défaut comme option sélectionnée.

12. Déterminez s’il existe des instances ParameterDef qui répondent à tous les critères suivants :

    -   L’instance ParameterDef s’affiche dans le document PrintCapabilities, mais pas dans PrintTicket.

    -   La propriété obligatoire de l’instance ParameterDef est définie sur inconditionnelle ou conditionnel.

    -   L’instance ParameterDef est référencée par une instance ParameterRef dans le PrintTicket au sein d’une instance option.

    Pour chaque instance ParameterDef dans le document PrintCapabilities, ajoutez à l’PrintTicket une instance ParameterInit correspondante. Définissez la valeur des instances ParameterInit récemment ajoutées sur la valeur par défaut spécifiée par les instances ParameterDef correspondantes.

13. Effectuez la détection des conflits de contraintes et modifiez la configuration pour éliminer ces conflits. Cette rubrique ne définit pas un processus particulier à utiliser pour résoudre les conflits de contrainte. Vous devez décider quelle fonctionnalité ou instance ParameterInit peut être modifiée, ainsi qu’une option ou valeur appropriée, respectivement, pour sélectionner qui a le moins d’impact sur l’intention générale de la configuration spécifiée dans PrintTicket. Comme mentionné précédemment, vous souhaiterez peut-être utiliser le score de mappage de chaque option et utiliser l’option avec le deuxième score le plus élevé. Pour déterminer quelle fonctionnalité ou ParameterInit modifier, vous pouvez définir une propriété privée que le client peut ajouter à PrintTicket. Cette propriété peut définir une priorité pour les instances Feature et ParameterInit afin que le processus de résolution soit informé de la fonctionnalité ou des instances ParameterInit qui sont importantes pour le client (et doivent être conservées dans le PrintTicket) et qui sont moins importantes.

14. Si le processus de résolution de contrainte a entraîné des modifications dans PrintTicket pour toutes les instances ParameterRef pour lesquelles la propriété Mandatory est définie sur Conditional, ajoutez des instances ParameterInit avec des valeurs par défaut pour celles qui apparaissent maintenant, et supprimez toute instance ParameterInit pour une instance ParameterRef qui ne s’affiche plus.

15. Supprimez toutes les instances de propriété et leur contenu qui s’affichent dans les instances d’option dans PrintTicket. Les éléments de propriété n’ont aucun rôle dans PrintTicket. Si l’option validée pour une fonctionnalité particulière correspond parfaitement à l’option prévalidée, transférez toutes les instances de propriété de cette option à partir de la prévalidation PrintTicket vers le PrintTicket maintenant validé, sous réserve que les espaces de noms des instances de propriété soient inscrits dans le document PrintCapabilities. Notez que pour que deux instances d’option soient considérées comme une correspondance parfaite, pour chaque ScoredProperty trouvé dans une option, il doit y avoir un ScoredProperty correspondant dans l’autre option, et les valeurs des deux instances ScoredProperty doivent être identiques.

16. Si votre fournisseur PrintTicket reconnaît et prend en charge toutes les instances de propriété privées ou publiques qui ont survécu à ce point, effectuez une validation dessus. Ne supprimez pas une propriété à ce stade, car vous ne la reconnaissez pas, elle peut être destinée à une autre phase de traitement des documents.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



