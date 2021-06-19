---
description: En savoir plus sur la création d’un PrintTicket spécifique à l’appareil, qui cible un appareil particulier et qui est portable sur plusieurs appareils.
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: Création d’un Device-Specific PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b825bd875ada534c8c467cd18d90f2db9a2a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409544"
---
# <a name="creating-a-device-specific-printticket"></a>Création d’un Device-Specific PrintTicket

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un PrintTicket spécifique à l’appareil cible un appareil particulier et n’est donc généralement pas portable sur plusieurs appareils.

Les étapes décrites dans la liste suivante doivent être utilisées lorsque vous créez un PrintTicket spécifique à l’appareil.

1.  Obtenez un document PrintCapabilities contenant uniquement les instances de fonctionnalités pertinentes pour l’appareil. Demandez un document PrintCapabilities par défaut. Cela ne vous oblige pas à spécifier un PrintTicket d’entrée, car les attributs d’appareil (instances et paramètres de fonctionnalité et d’option) utilisés pour construire le PrintTicket sont indépendants de la configuration.

2.  Créez un document XML vide contenant la racine PrintTicket. Assignez un préfixe d’espace de noms à l’espace de noms du schéma d’impression et assignez des préfixes pour tous les autres espaces de noms qui seront utilisés par le PrintTicket. Spécifiez la version du schéma PrintTicket.

3.  Vous pouvez définir des paramètres dans le PrintTicket pour chaque fonctionnalité et instance ParameterDef rapportée dans le document PrintCapabilities, ou uniquement celles qui vous intéressent. Si un PrintTicket partiel est présenté à l’interface PrintTicket, les valeurs par défaut sont automatiquement fournies pour les instances Feature et ParameterDef omises pendant la validation de PrintTicket.

4.  Examinez le document PrintCapabilities pour les instances de fonctionnalités et déterminez celles que vous souhaitez définir dans le PrintTicket. Ajoutez ces instances de fonctionnalités au PrintTicket, mais ne transférez pas le contenu des instances de fonctionnalité vers votre PrintTicket. Si vous transférez une sous-fonctionnalité, la fonctionnalité parente doit également être transférée, et la relation parent-enfant doit être conservée dans PrintTicket.

    Pour chaque fonctionnalité que vous transférez, déterminez les instances d’option applicables à votre PrintTicket. Transférez la totalité de l’option telle qu’elle est définie dans le document PrintCapabilities, puis supprimez toutes les instances de propriété présentes. Les instances de propriété sont utilisées dans les documents PrintCapabilities, mais n’ont aucun effet dans PrintTicket. Conservez toutes les instances ScoredProperty, en veillant à conserver leur emplacement. ils constituent une partie intrinsèque de la définition de l’option.

5.  Vous pouvez également ajouter des instances de propriété à toute instance ScoredProperty. Les instances de propriété sont utilisées uniquement si le fournisseur PrintTicket prend explicitement en charge leur utilisation. Chaque fournisseur doit documenter l’objectif et l’utilisation de toutes les instances de propriété prises en charge. Notez que pendant la validation, toutes les instances de propriété contenues dans une instance option sont supprimées, sauf si l’espace de noms de la propriété est reconnu par le fournisseur PrintCapabilities ou PrintTicket cible, et si une option candidat est trouvée dans le document PrintCapabilities dont les instances ScoredProperty correspondent parfaitement à celles définies dans l’option de référence.

6.  Si les mots clés du schéma d’impression définissent la propriété SelectionType sur PickMany pour une fonctionnalité particulière, vous pouvez sélectionner plusieurs options pour cette fonctionnalité, à condition que l’option désignée comme IdentityOption ne soit pas l’une de celles sélectionnées. IdentityOption dans le schéma d’impression a le même effet que l’option None des fichiers PPD PostScript et des fichiers Unidrv GPD. Il sert de non-opération.

7.  Examinez le document PrintCapabilities pour les instances ParameterDef qui doivent être définies dans votre PrintTicket. Pour chaque instance ParameterDef, sélectionnez une valeur à utiliser dans l’instance ParameterInit dans PrintTicket. Cette valeur doit être du type de données correct et doit être comprise dans la plage définie dans l’instance ParameterDef et doit satisfaire à toutes les autres exigences spécifiées dans l’instance ParameterDef. Utilisez une instance ParameterInit pour initialiser le paramètre avec la valeur que vous avez sélectionnée.

8.  Examinez le contenu de chaque instance d’option qui apparaît dans PrintTicket pour les occurrences d’instances ParameterRef. Si une instance ParameterInit correspondante n’apparaît pas déjà dans PrintTicket, suivez l’étape précédente pour créer une instance ParameterInit dans PrintTicket. L’objectif de cette instance ParameterInit est d’initialiser le paramètre référencé par l’instance ParameterRef.

9.  Gardez à l’esprit que les conflits de contrainte peuvent empêcher l’appareil d’appliquer la configuration que vous avez spécifiée dans PrintTicket. Si nécessaire, le processus de validation modifie la configuration définie dans PrintTicket à une valeur qui est exempte de conflits.

10. Examinez les mots clés du schéma d’impression pour les instances de propriété qui doivent être présentes dans PrintTicket. Ajoutez une instance de propriété à votre PrintTicket pour chaque requis et fournissez une valeur appropriée pour celle-ci à l’aide du type d’élément de valeur. Assurez-vous que les instances de propriété se trouvent correctement dans PrintTicket.

11. Examinez les instances de propriété facultatives dans le schéma PrintTicket. S’il existe des instances de propriété de ce type qui doivent se trouver dans PrintTicket, créez-les dans votre PrintTicket.

12. Vous pouvez également ajouter des instances de propriété définies en privé au niveau de la racine, ou à n’importe quelle fonctionnalité, option ou instance de propriété. Notez toutefois que ces instances de propriété définies de manière privée sont supprimées pendant la validation, à moins que l’espace de noms auquel elles appartiennent soient reconnus par le fournisseur PrintCapabilities ou PrintTicket cible. En outre, les instances de propriété qui apparaissent n’importe où dans une instance option sont supprimées lors de la validation, sauf si le document PrintCapabilities contient une option qui correspond à une correspondance parfaite. Deux instances d’option sont une correspondance parfaite si chaque ScoredProperty dans une instance d’option a un ScoredProperty correspondant dans l’autre, et les valeurs des instances ScoredProperty sont les mêmes. Consultez le schéma privé du fournisseur PrintTicket pour obtenir la liste des instances de propriété privées reconnues et leurs utilisations.

13. Les enfants du même type d’élément ne peuvent pas s’imbriquer jusqu’à une profondeur de plus de 10 éléments. Cette règle s’applique indépendamment à chaque type d’élément qui peut être défini.

> [!Note]  
> Le contenu XML PrintTicket doit être encodé à l’aide de UTF-8 ou UTF-16.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



