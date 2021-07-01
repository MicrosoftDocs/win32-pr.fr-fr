---
description: Passez en revue une discussion sur le comportement de l’interface utilisateur en ce qui concerne les fonctionnalités et les options de documents et d’impression.
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: Comportement de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81d007c653ed3f019892e944d9fa4203dc6de11
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119434"
---
# <a name="user-interface-behavior"></a>Comportement de l’interface utilisateur

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Supposons que vous créez un client PrintCapabilities qui lit un document PrintCapabilities et sélectionne une ou plusieurs options de chaque fonctionnalité et qui utilise celles-ci pour construire un PrintTicket qui spécifie la configuration à utiliser pour traiter le travail. Pour chaque fonctionnalité qui vous intéresse, le client doit examiner chaque option et déterminer si cette option est appropriée pour la tâche en cours. Pour une option qui n’est pas paramétrable, elle peut être évaluée en accédant à la valeur de chaque ScoredProperty. Dans le cas d’une option de taille de média non paramétrable, le client détermine si les dimensions de largeur et de hauteur des médias signalées dans chaque option correspondent aux dimensions requises.

Dans le cas de l’option paramétrable, le client doit accéder à l’instance ParameterDef indiquée dans l’instance ParameterRef contenue dans l’une des instances ScoredProperty. Le ParameterDef définit généralement la plage de valeurs autorisées pour le paramètre, ainsi que les unités (pouces, mm, etc.) représentées par la valeur. Si les dimensions requises se trouvent dans la plage de valeurs autorisées pour chacun des paramètres, le client a la tâche supplémentaire d’initialiser les paramètres (au moyen d’une instance de ParameterInit) dans PrintTicket. Il s’agit d’une tâche particulièrement importante. Par exemple, un PrintTicket ne doit pas spécifier de taille de média personnalisée sans spécifier les dimensions du média, car le PrintTicket résultant sera ambigu et mal défini.

Un ensemble similaire de circonstances doit être géré si le client est une interface utilisateur. L’interface utilisateur affiche généralement les valeurs des instances ScoredProperty définies pour chaque option. Par souci de clarté, il est essentiel d’afficher la plage et les unités autorisées pour les paramètres dans une option paramétrée. En outre, si l’utilisateur sélectionne l’option paramétrable, l’interface utilisateur (IU) doit inviter l’utilisateur à entrer la valeur à utiliser pour initialiser chaque paramètre. Enfin, l’interface utilisateur doit composer un PrintTicket qui reflète toutes les sélections de l’utilisateur.

Pour plus d’informations sur la construction et la spécification de l’initialisation des paramètres, consultez [création d’un Device-Specific PrintTicket](creating-a-device-specific-printticket.md). Pour plus d’informations sur le déréférencement des instances ParameterRef et l’interprétation des instances ParameterDef, consultez [Using Parameters](using-parameters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



