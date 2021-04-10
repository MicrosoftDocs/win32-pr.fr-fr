---
title: Comment les serveurs implémentent des ID enfants
description: Les développeurs de serveurs peuvent assigner des ID enfants à des éléments simples et à des objets accessibles. Toutefois, l’approche recommandée consiste à prendre en charge l’interface COM (Component Object Model) standard IEnumVARIANT dans chaque objet accessible qui a des enfants.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941163"
---
# <a name="how-servers-implement-child-ids"></a>Comment les serveurs implémentent des ID enfants

Les développeurs de serveurs peuvent assigner des ID enfants à des éléments simples et à des objets accessibles. Toutefois, l’approche recommandée consiste à prendre en charge l’interface COM (Component Object Model) standard [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) dans chaque objet accessible qui a des enfants.

Si vous implémentez [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), vous devez :

-   Énumérer tous les enfants, à la fois les éléments simples et les objets accessibles. Fournissez des ID enfants pour tous les éléments simples et fournissez le [**IDispatch**](idispatch-interface.md) à chaque objet accessible.
-   Pour les objets accessibles, définissez le membre **VT** du [**Variant**](variant-structure.md) sur VT \_ Dispatch. Le membre **pdispVal** doit contenir un pointeur vers l’interface [**IDispatch**](idispatch-interface.md) . Notez que le **Variant** est alloué et libéré par le client.
-   Pour les éléments simples, l’ID enfant est un entier positif de 32 bits. Notez que les entiers nuls et négatifs sont réservés par Microsoft Active Accessibility. Définissez le membre **VT** de la structure [**Variant**](variant-structure.md) sur VT \_ I4 et le membre **lVal** sur l’ID enfant.

Si vous ne prenez pas en charge [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), vous devez assigner des ID enfants et numéroter les enfants de chaque objet de manière séquentielle à partir de 1.

Il est recommandé que les clients utilisent la fonction Microsoft Active Accessibility Function [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) au lieu d’appeler directement l’interface Server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .

 

 