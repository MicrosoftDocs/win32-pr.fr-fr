---
title: Objets accessibles
description: Avec Microsoft Active Accessibility, les éléments d’interface utilisateur sont exposés aux clients sous la forme d’objets COM (Component Object Model).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9591c4884826ba9d85192e5702d0528f25087797faf83d83314d5c00f172459b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994379"
---
# <a name="accessible-objects"></a>Objets accessibles

Avec Microsoft Active Accessibility, les éléments d’interface utilisateur sont exposés aux clients sous la forme d’objets COM (Component Object Model). Ces *objets accessibles* maintiennent des informations, appelées *Propriétés*, qui décrivent le nom de l’objet, l’emplacement de l’écran et d’autres informations requises par les aides à l’accessibilité. Les objets accessibles fournissent également des *méthodes* que les clients appellent pour faire en sorte que l’objet effectue une action. Les objets accessibles qui ont des éléments simples qui leur sont associés sont également appelés *parents*, ou *conteneurs*.

Les objets accessibles sont implémentés à l’aide de l’interface [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com de Microsoft Active Accessibility. Les méthodes et propriétés **IAccessible** permettent aux applications clientes d’obtenir des informations sur les éléments d’interface utilisateur requis par les utilisateurs. Par exemple, [**IAccessible :: obtenir \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) retourne un pointeur d’interface vers le parent d’un objet accessible, et [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) permet aux clients d’obtenir des informations sur d’autres objets au sein d’un conteneur.

Pour plus d’informations sur la façon dont les objets accessibles et les éléments simples sont liés, consultez [éléments simples](simple-elements.md).

 

 




