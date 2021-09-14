---
title: Navigation hiérarchique
description: Les clients doivent souvent se déplacer entre des objets en fonction de leurs relations parent-enfant. Par exemple, un client a peut-être déjà des informations sur un contrôle de barre d’outils, mais pas d’informations sur les boutons qu’il contient.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095546"
---
# <a name="hierarchical-navigation"></a>Navigation hiérarchique

Les clients doivent souvent se déplacer entre des objets en fonction de leurs relations parent-enfant. Par exemple, un client a peut-être déjà des informations sur un contrôle de barre d’outils, mais pas d’informations sur les boutons qu’il contient.

L’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expose les relations hiérarchiques entre les objets. Les clients peuvent naviguer d’un objet parent à ses enfants ou d’un objet enfant vers son parent en appelant [**IAccessible :: obtenir \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) ou [**IAccessible :: obtenir \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).

 

 




