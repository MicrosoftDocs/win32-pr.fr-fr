---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Création d’un PrintTicket générique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34281eda82a48ea0ac4077248547522ddc305ea
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523115"
---
# <a name="creating-a-generic-printticket"></a>Création d’un PrintTicket générique

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Si le document PrintCapabilities pour l’appareil n’est pas disponible, ou si l’appareil cible est inconnu, vous devez construire un PrintTicket générique. Étant donné qu’il n’existe aucun document PrintCapabilities fournissant un ensemble d’éléments de fonctionnalité et d’option, ou paramètres, les instances prises en charge de ces types d’éléments doivent être obtenues directement à partir des mots clés du schéma d’impression.

Les étapes décrites dans la liste suivante doivent être utilisées lorsque vous créez un PrintTicket générique.

1.  Créez un document XML vide qui contient la racine PrintTicket. Attribuez un préfixe d’espace de noms à l’espace de noms du schéma d’impression. Spécifiez la version du schéma.

2.  Examinez les instances de fonctionnalités dans les mots clés du schéma d’impression et déterminez celles que vous souhaitez définir dans le PrintTicket. Ajoutez ces instances de fonctionnalités à votre PrintTicket. Lorsque vous transférez une sous-fonctionnalité, vous devez transférer la fonctionnalité parente et conserver la relation parent-enfant entre la fonctionnalité et la sous-fonctionnalité dans PrintTicket.

    Pour chaque instance de fonctionnalité que vous transférez, déterminez les instances d’option applicables à votre PrintTicket. À partir de cet ensemble d’instances d’option, transférez chaque instance d’option complète telle qu’elle apparaît dans le schéma d’impression, puis supprimez toutes les instances de propriété présentes, à l’exception possible de celles qui ont une signification pour votre PrintTicket. Conservez toutes les instances ScoredProperty, en veillant à conserver leur emplacement. ils constituent une partie intrinsèque de la définition de l’option.

3.  Vous pouvez également ajouter des instances de propriété à n’importe quel ScoredProperty. Les éléments de propriété sont applicables uniquement si le fournisseur PrintTicket prend explicitement en charge leur utilisation. Chaque fournisseur doit documenter l’objectif et l’utilisation de toutes les instances de propriété prises en charge. Étant donné que vous n’avez aucune idée du fournisseur qui traitera le PrintTicket, vous souhaiterez peut-être ajouter uniquement les instances de propriété qui sont explicitement prises en charge par le fournisseur PrintTicket du système.

4.  Si les mots clés du schéma d’impression définissent la propriété SelectionType sur PickMany pour une fonctionnalité particulière, vous pouvez sélectionner plusieurs options pour cette fonctionnalité, à condition que l’option désignée comme IdentityOption ne soit pas l’une de celles sélectionnées. IdentityOption dans le schéma d’impression a le même effet que l’option None des fichiers PPD PostScript et des fichiers Unidrv GPD. Il sert de non-opération.

5.  Examinez les mots clés du schéma d’impression pour les instances ParameterDef qui doivent être initialisées dans votre PrintTicket. Pour chaque instance ParameterDef, sélectionnez la valeur à utiliser dans l’instance ParameterInit dans PrintTicket. Cette valeur doit être du type de données correct, doit être comprise dans la plage définie dans l’instance ParameterDef et doit satisfaire à toutes les autres exigences spécifiées dans l’instance ParameterDef. Utilisez une instance ParameterInit pour initialiser le paramètre avec la valeur que vous avez sélectionnée.

    Si vous développez un composant d’interface utilisateur (IU), concevez vos méthodes de génération PrintTicket afin que les utilisateurs puissent entrer la valeur de l’élément ParameterInit. En outre, la méthode d’entrée d’interface utilisateur doit observer et se conformer aux restrictions d’entrée spécifiées par l’élément ParameterDef associé.

6.  Examinez le contenu de chaque instance d’option qui apparaît dans PrintTicket pour les occurrences de ParameterRef. Si une instance ParameterInit correspondante n’apparaît pas déjà dans PrintTicket, suivez l’étape précédente pour créer une instance ParameterInit dans PrintTicket. L’objectif de cette instance ParameterInit est d’initialiser le paramètre référencé par l’instance ParameterRef.

7.  Gardez à l’esprit que l’appareil qui traite le travail peut ne pas prendre en charge toutes les fonctionnalités spécifiées dans PrintTicket. Gardez également à l’esprit qu’une fonctionnalité nommée peut être prise en charge, mais qu’il est possible qu’il ne s’agit pas d’une option spécifiée de cette fonctionnalité. Les mêmes avertissements s’appliquent aux paramètres. Même si un appareil prend en charge un paramètre nommé, la valeur spécifiée dans l’instance ParameterInit peut ne pas être comprise dans la plage valide pour l’appareil.

8.  Examinez les mots clés du schéma d’impression pour les instances de propriété qui doivent être présentes dans PrintTicket. Ajoutez une instance de propriété pour chacun d’entre eux à votre PrintTicket et fournissez une valeur appropriée pour celle-ci à l’aide du type d’élément de valeur. Assurez-vous que les instances de propriété se trouvent correctement dans PrintTicket. Veillez à consulter le schéma PrintTicket plutôt que le schéma PrintCapabilities.

9.  Examinez les instances de propriété facultatives définies dans le schéma PrintTicket. S’il existe des instances de propriété de ce type qui doivent se trouver dans PrintTicket, créez-les dans votre PrintTicket.

10. Les enfants du même type d’élément ne peuvent pas s’imbriquer jusqu’à une profondeur de plus de 10 éléments. Cette règle s’applique indépendamment à chaque type d’élément qui peut être défini.

> [!Note]  
> Le contenu XML PrintTicket doit être encodé à l’aide de UTF-8 ou UTF-16.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



