---
title: Obtention des ID enfants par les clients
description: Obtention des ID enfants par les clients
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a12dc3f40c2aaa776c1fa8e61713c52ffbdcde554c9f6a1cbca7093998780c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388599"
---
# <a name="how-clients-obtain-child-ids"></a>Obtention des ID enfants par les clients

Les développeurs clients peuvent récupérer l’ID enfant d’un objet de l’une des manières suivantes :

-   Appelez [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren). Cette fonction récupère un tableau de structures de [**type Variant**](variant-structure.md) .
-   Interrogez l’objet pour voir s’il prend en charge l’interface [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) . S’il est présent, utilisez [**IEnumVARIANT :: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtenir les ID enfants.
-   Collectez les ID enfants en appelant la méthode [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) de l’objet parent.

> [!Note]  
> Il incombe au client de libérer la mémoire utilisée pour les structures de [**variantes**](variant-structure.md) . Les clients doivent également appeler [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur toute interface [**IDispatch**](idispatch-interface.md) qui est retournée.

 

 

 