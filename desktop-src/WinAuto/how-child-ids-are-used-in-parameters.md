---
title: Utilisation des ID enfants dans les paramètres
description: Cette rubrique décrit les paramètres d’entrée, les paramètres de sortie et les cas spéciaux d’interprétation des ID enfants retournés par les méthodes IAccessible.
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc0c3be970fb4a688a0a5447b72719428e78e074cbc7a17f2b6b698fcca177f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052719"
---
# <a name="how-child-ids-are-used-in-parameters"></a>Utilisation des ID enfants dans les paramètres

Cette rubrique décrit les paramètres d’entrée, les paramètres de sortie et les cas spéciaux d’interprétation des ID enfants retournés par les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

## <a name="input-parameters"></a>Paramètres d’entrée

La plupart des fonctions de Active Accessibility de Microsoft et la plupart des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) prennent une structure de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) comme paramètre d’entrée. Pour la plupart des propriétés **IAccessible** , ce paramètre permet aux développeurs clients de spécifier s’ils souhaitent des informations sur l’objet lui-même ou sur l’un des éléments simples de l’objet.

Microsoft Active Accessibility fournit la constante **CHILDID \_ Self** pour indiquer que des informations sont nécessaires sur l’objet lui-même. Pour obtenir des informations sur un élément simple, les développeurs clients spécifient son ID enfant dans le paramètre [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .

Lors de l’initialisation d’un paramètre [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , veillez à spécifier **VT \_ I4** dans le membre **VT** en plus de spécifier la valeur de l’ID enfant (ou **CHILDID \_ Self**) dans le membre **lVal** .

Par exemple, pour obtenir le nom d’un objet, et non l’un des éléments enfants de l’objet, initialisez le [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) pour le premier paramètre de [**IAccessible :: obtenir \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **CHILDID \_ Self** dans le membre **lVal** et **VT \_ I4** dans le membre **VT** ), puis appelez **IAccessible :: obtenir \_ accName**.

## <a name="output-parameters"></a>Paramètres de sortie

Plusieurs fonctions et méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ont un [](/windows/win32/api/oaidl/ns-oaidl-variant) \* paramètre de sortie variant qui contient un ID enfant ou un pointeur d’interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) vers un objet enfant. Un client doit suivre différentes étapes, selon qu’il reçoit un ID enfant **VT \_ I4** (élément simple) ou un pointeur d’interface **IDispatch** avec **CHILDID \_ Self** (objet complet). Les étapes suivantes fournissent un pointeur d’interface **IAccessible** et un ID enfant qui, ensemble, permettent aux clients d’utiliser les méthodes et propriétés **IAccessible** . Ces étapes s’appliquent aux méthodes [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest), [**\_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)et [**\_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) . Elles s’appliquent également aux fonctions du client [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)et [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

Le tableau suivant répertorie les résultats possibles retournés et les étapes de retraitement requises pour que les clients aient un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un ID enfant.



| Résultat retourné                                      | Après le traitement de la valeur de retour                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pointeur d’interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) | Il s’agit d’un objet complet. Appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour accéder au pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Utilisez le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) avec **CHILDID \_ Self** pour accéder aux méthodes et propriétés **IAccessible** .<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| \_ID enfant VT I4                                      | Appelez [**IAccessible :: obtenir \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) à l’aide de l’ID enfant pour déterminer si vous disposez d’un pointeur d’interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . Si vous recevez un pointeur d’interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , utilisez-le avec **CHILDID \_ Self** pour accéder aux méthodes et propriétés de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Si l’appel à la méthode [**obtenir \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) échoue, vous avez un élément simple. Utilisez le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’origine (celui que vous avez utilisé dans votre appel à la méthode ou la fonction mentionnée ci-dessus) avec l’ID de l’enfant **VT \_ I4** renvoyé par l’appel.<br/> |



 

Avant de pouvoir utiliser un paramètre [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , vous devez l’initialiser en appelant la fonction com (Component Object Model) [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) . Lorsque vous avez terminé avec la structure, appelez [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) pour libérer la mémoire réservée pour cette **variante**.

## <a name="special-cases"></a>Cas particuliers

Il existe des exceptions aux instructions dans le tableau ci-dessus, par exemple lorsqu’un ID enfant est retourné par la méthode [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) . Les serveurs doivent retourner une interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) si l’enfant est un objet accessible. Si un ID enfant est retourné par **IAccessible :: accHitTest**, l’enfant est un élément simple.

En outre, il existe des cas spéciaux pour [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate). Pour plus d’informations, consultez **IAccessible :: accNavigate** et [navigation spatiale et logique](spatial-and-logical-navigation.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Interface IDispatch](idispatch-interface.md)
</dt> <dt>

[Structure de variante](variant-structure.md)
</dt> </dl>

 

