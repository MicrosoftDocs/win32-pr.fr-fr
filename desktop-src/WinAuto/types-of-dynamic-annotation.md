---
title: Types d’annotation dynamique
description: Il existe trois types d’annotations dynamiques pris en charge dans Microsoft Active Accessibility l’annotation directe, l’annotation mappée sur la valeur et l’annotation de serveur. Chaque type offre des avantages spécifiques. il est donc important de comprendre les différences.
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0453d3b5d05e2713d1a57fb0f475d4ec2a481b02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010595"
---
# <a name="types-of-dynamic-annotation"></a>Types d’annotation dynamique

Trois types d’annotation dynamique sont pris en charge dans Microsoft Active Accessibility : l' *annotation directe*, l' *annotation mappée sur la valeur* et l' *annotation de serveur*. Chaque type offre des avantages spécifiques. il est donc important de comprendre les différences.

## <a name="direct-annotation"></a>Annotation directe

L’annotation directe est la forme la plus simple d’annotation dynamique. Il s’applique aux éléments accessibles dont la propriété annotée n’est pas dépendante de l’état du contrôle et ne requiert pas la prise en charge supplémentaire fournie par l’annotation de mappage de valeur et l’annotation de serveur. L’annotation directe est utilisée pour substituer la valeur d’une ou de plusieurs propriétés Microsoft Active Accessibility d’un élément accessible, et pour remplacer ou ajouter une propriété Microsoft UI Automation au contrôle. Toutes les annotations effectuées dans une propriété de Active Accessibility Microsoft sont reflétées dans la traduction UI Automation, ainsi que dans le proxy Automation Microsoft Active Accessibility à interface utilisateur. Pour plus d’informations, consultez [annotation directe](direct-annotation.md).

## <a name="value-map-annotation"></a>Annotation de la carte des valeurs

En plus d’annoter directement les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , il est souvent nécessaire de convertir une valeur spécifique au contrôle en une chaîne compréhensible par un utilisateur final. par exemple, le contrôle de curseur résolution d’écran sous l’onglet **Paramètres** de la fenêtre **propriétés d’affichage** (à partir du **panneau de configuration**). Alors que chaque position de curseur correspond à une résolution différente (par exemple, 640 x 480, 1024 x 768), le contrôle n’a aucune connaissance de cette relation et ne peut pas transmettre ces informations à Microsoft Active Accessibility.

Une annotation de valeur mappée facilite cette tâche. À l’aide de cette forme d’annotation, vous pouvez spécifier des chaînes pour les valeurs de curseur et spécifier des rôles, des États et des descriptions pour les icônes dans les vues de liste et d’arborescence. Pour plus d’informations, consultez annotation de la [carte des valeurs](value-map-annotation.md).

## <a name="server-annotation"></a>Annotation de serveur

L’annotation de serveur permet aux développeurs d’inscrire un objet de rappel aux demandes du client de service pour la propriété annotée d’un élément. Cet objet de rappel doit implémenter l’interface [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) et être inscrit auprès de Microsoft Active Accessibility Annotation Services. Une fois inscrit, il est demandé de traiter toutes les demandes du client pour la valeur de la propriété de cet élément accessible.

Une fonctionnalité particulièrement utile de l’annotation de serveur est qu’un serveur peut être inscrit une seule fois pour traiter les demandes pour un conteneur et tous ses enfants. Par exemple, un serveur unique peut être configuré une seule fois pour traiter les requêtes de tous les éléments est une zone de liste. Pour plus d’informations, consultez [annotation de serveur](server-annotation.md).

 

 




