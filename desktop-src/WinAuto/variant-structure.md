---
title: Structure de variante
description: La plupart des fonctions de Active Accessibility Microsoft et les propriétés et méthodes IAccessible prennent une structure de variante comme paramètre. Fondamentalement, la structure VARIANT est un conteneur pour une grande Union qui transporte de nombreux types de données.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530220"
---
# <a name="variant-structure"></a>Structure de variante

La plupart des fonctions de Active Accessibility Microsoft et les propriétés et méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) prennent une structure de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) comme paramètre. Fondamentalement, la structure **Variant** est un conteneur pour une grande Union qui transporte de nombreux types de données.

La valeur du premier membre de la structure, **VT**, décrit les membres de l’Union qui sont valides. Bien que la structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) prenne en charge de nombreux types de données différents, Microsoft Active Accessibility utilise uniquement les types suivants.



| Valeur VT     | Nom du membre de valeur correspondant |
|--------------|---------------------------------|
| VT \_       | **lVal**                        |
| \_distribution vt | **pdispVal**                    |
| VT \_ BSTR     | **bstrVal**                     |
| VT \_ vide    | Aucun                            |



 

Lorsque vous recevez des informations dans une structure de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) , vérifiez le membre **VT** pour savoir quel membre contient des données valides. De même, lorsque vous envoyez des informations à l’aide d’une structure **Variant** , définissez toujours **VT** pour refléter le membre d’Union qui contient les informations.

Avant d’utiliser la structure, initialisez-la en appelant la fonction COM (Component Object Model) [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) . Lorsque vous avez terminé avec la structure, effacez-la avant de libérer la mémoire qui contient la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) en appelant [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).

 

 