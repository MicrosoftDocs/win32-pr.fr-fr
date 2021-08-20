---
title: Annotation de serveur
description: Cette section fournit des informations sur l’utilisation des annotations de serveur.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9438184cf68d4a0f819afcd7e5497e627a0982e0f9fd9784c8a3460ab5121a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052537"
---
# <a name="server-annotation"></a>Annotation de serveur

Cette section fournit des informations sur l’utilisation des annotations de serveur.

## <a name="summary"></a>Résumé

Vous définissez une classe qui implémente [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), créez une instance de celle-ci et indiquez au système que vous souhaitez qu’elle remplace des propriétés spécifiques sur des éléments d’interface utilisateur spécifiques. Quand un client demande l’une des propriétés à partir de l’un des éléments d’interface utilisateur, votre objet est appelé et donne la possibilité de fournir une valeur. Si votre objet retourne une valeur, cette valeur est repassée au client. Si votre objet ne retourne pas de valeur, la valeur par défaut de cet élément d’interface utilisateur est retournée au client.

## <a name="when-to-use-this-technique"></a>Quand utiliser cette technique

Utilisez cette technique lorsque vous souhaitez substituer les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour un objet. Cette technique est bien plus simple que les techniques **IAccessible** précédentes. Pour plus d’informations, consultez [alternatives à l’annotation dynamique](alternatives-to-dynamic-annotation.md).

Vous ne pouvez pas utiliser l’annotation de serveur pour modifier la structure d’objets exposée. Pour modifier la structure d’un objet, vous devez implémenter un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) complet.

Pour plus d’informations sur les annotations de serveur, consultez les rubriques suivantes :

-   [Utilisation de l’annotation de serveur](using-server-annotation.md)
-   [Exemple d’annotation de serveur](server-annotation-sample.md)

 

 




