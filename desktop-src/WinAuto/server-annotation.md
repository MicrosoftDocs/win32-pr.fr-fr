---
title: Annotation de serveur
description: Cette section fournit des informations sur l’utilisation des annotations de serveur.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518225"
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

 

 




