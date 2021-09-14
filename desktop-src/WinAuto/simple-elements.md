---
title: Éléments simples
description: Un élément simple est un élément d’interface utilisateur qui partage un objet IAccessible avec d’autres éléments et s’appuie sur cet objet IAccessible (généralement son parent) pour exposer ses propriétés.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010622"
---
# <a name="simple-elements"></a>Éléments simples

Un *élément simple* est un élément d’interface utilisateur qui partage un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) avec d’autres éléments et s’appuie sur cet objet **IAccessible** (généralement son parent) pour exposer ses propriétés. Pour faire la différence entre les éléments qui partagent un objet **IAccessible** , le serveur affecte un identificateur enfant positif unique à chaque élément simple. Cette affectation est effectuée par instance d’interface, de sorte que les ID doivent être uniques dans ce contexte. De nombreuses implémentations assignent ces ID de manière séquentielle, en commençant par 1. Ce schéma n’autorise pas les éléments simples à avoir leurs propres enfants. Les éléments simples sont également appelés *enfants*.

Pour être identifié et exposé de manière unique, un élément simple requiert un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un ID enfant. Par conséquent, lors de la communication avec un objet **IAccessible** , les clients doivent fournir l’ID enfant approprié. Un identificateur spécial, **CHILDID \_ Self**, peut être utilisé pour faire référence à l’objet accessible lui-même, au lieu de l’un de ses enfants.

L’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) partagé entre les éléments simples correspond souvent à un objet parent commun dans l’interface utilisateur. Par exemple, les zones de liste système exposent un objet accessible pour la zone de liste globale et des éléments simples pour chaque élément de zone de liste. Dans ce cas, l’objet **IAccessible** pour la zone de liste est également le parent ou le conteneur des éléments de liste.

Pour plus d’informations sur les objets accessibles, consultez [objets accessibles](accessible-objects.md).

 

 




