---
title: Obtention des ID enfants par les clients
description: Obtention des ID enfants par les clients
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727724"
---
# <a name="how-clients-obtain-child-ids"></a>Obtention des ID enfants par les clients

Les développeurs clients peuvent récupérer l’ID enfant d’un objet de l’une des manières suivantes :

-   Appelez [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren). Cette fonction récupère un tableau de structures de [**type Variant**](variant-structure.md) .
-   Interrogez l’objet pour voir s’il prend en charge l’interface [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) . S’il est présent, utilisez [**IEnumVARIANT :: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtenir les ID enfants.
-   Collectez les ID enfants en appelant la méthode [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) de l’objet parent.

> [!Note]  
> Il incombe au client de libérer la mémoire utilisée pour les structures de [**variantes**](variant-structure.md) . Les clients doivent également appeler [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur toute interface [**IDispatch**](idispatch-interface.md) qui est retournée.

 

 

 