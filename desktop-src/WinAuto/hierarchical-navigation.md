---
title: Navigation hiérarchique
description: Les clients doivent souvent se déplacer entre des objets en fonction de leurs relations parent-enfant. Par exemple, un client a peut-être déjà des informations sur un contrôle de barre d’outils, mais pas d’informations sur les boutons qu’il contient.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe1ab794dbf73c7da522d481030c417d968c1be509c9b24b1dd3108860845f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122179"
---
# <a name="hierarchical-navigation"></a>Navigation hiérarchique

Les clients doivent souvent se déplacer entre des objets en fonction de leurs relations parent-enfant. Par exemple, un client a peut-être déjà des informations sur un contrôle de barre d’outils, mais pas d’informations sur les boutons qu’il contient.

L’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expose les relations hiérarchiques entre les objets. Les clients peuvent naviguer d’un objet parent à ses enfants ou d’un objet enfant vers son parent en appelant [**IAccessible :: obtenir \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) ou [**IAccessible :: obtenir \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).

 

 




