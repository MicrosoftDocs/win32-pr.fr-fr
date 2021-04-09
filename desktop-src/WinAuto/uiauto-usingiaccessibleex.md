---
title: Ajout de la fonctionnalité UI Automation aux serveurs Active Accessibility
description: Les contrôles qui n’ont pas de fournisseur UI Automation de Microsoft, mais qui implémentent IAccessible peuvent facilement être mis à niveau pour fournir des fonctionnalités d’automatisation d’interface utilisateur, en implémentant l’interface IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- UI Automation, serveurs Active Accessibility
- UI Automation, serveurs Microsoft Active Accessibility
- UI Automation, IAccessible
- UI Automation, IAccessibleEx
- UI Automation, exposer IAccessibleEx
- UI Automation, implémentation de IAccessibleEx
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- exposition de IAccessibleEx
- implémentation de IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941047"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a>Ajout de la fonctionnalité UI Automation aux serveurs Active Accessibility

Les contrôles qui n’ont pas de fournisseur UI Automation de Microsoft, mais qui implémentent [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) peuvent facilement être mis à niveau pour fournir des fonctionnalités d’automatisation d’interface utilisateur, en implémentant l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Cette interface permet au contrôle d’exposer des propriétés UI Automation et des modèles de contrôle, sans avoir besoin d’une implémentation complète des interfaces du fournisseur UI Automation telles que [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Pour implémenter **IAccessibleEx**, la hiérarchie d’objets Microsoft Active Accessibility de référence ne doit pas contenir d’erreurs ou d’incohérences (par exemple, un objet enfant dont l’objet parent ne la répertorie pas comme enfant) et ne doit pas être en conflit avec les spécifications UI Automation. Si la hiérarchie d’objets Microsoft Active Accessibility répond à ces exigences, il s’agit d’un bon candidat à l’ajout de fonctionnalités à l’aide de **IAccessibleEx**. dans le cas contraire, vous devez implémenter UI Automation seul ou parallèlement à l’implémentation de Microsoft Active Accessibility.

Prenons le cas d’un contrôle personnalisé qui a une valeur de plage. Le serveur Microsoft Active Accessibility pour le contrôle définit son rôle et peut retourner sa valeur actuelle, mais n’a pas la possibilité de retourner les valeurs minimales et maximales du contrôle, car ces propriétés ne sont pas définies dans Microsoft Active Accessibility. Un client UI Automation est en mesure de récupérer le rôle du contrôle, la valeur actuelle et d’autres propriétés de Active Accessibility Microsoft, car le noyau UI Automation peut les obtenir via [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Toutefois, sans accès à une interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) sur l’objet, UI Automation ne peut pas non plus récupérer les valeurs maximale et minimale.

Le développeur de contrôle peut fournir un fournisseur UI Automation complet pour le contrôle, mais cela signifierait la duplication d’une grande partie des fonctionnalités existantes de l’implémentation de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : par exemple, la navigation et les propriétés communes. Au lieu de cela, le développeur peut continuer à s’appuyer sur **IAccessible** pour fournir cette fonctionnalité, tout en ajoutant la prise en charge des propriétés spécifiques au contrôle par le biais de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

Pour mettre à jour le contrôle personnalisé, vous devez suivre les étapes principales suivantes :

-   Implémentez [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) sur l’objet accessible afin que l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se trouve sur ce ou sur un objet distinct.
-   Implémentez [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sur l’objet accessible.
-   Créez des objets accessibles distincts pour tous les éléments enfants Microsoft Active Accessibility, qui, dans Microsoft Active Accessibility, ont pu être représentés par l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sur l’objet parent (par exemple, les éléments de liste). Implémentez [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sur ces objets.
-   Implémentez [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) sur tous les objets accessibles.
-   Implémentez les interfaces de modèle de contrôle appropriées sur les objets accessibles.

Cette rubrique contient les sections suivantes.

-   [Exposition de IAccessibleEx](#exposing-iaccessibleex)
-   [Implémentation de IAccessibleEx](#implementing-iaccessibleex)
-   [Rubriques connexes](#related-topics)

## <a name="exposing-iaccessibleex"></a>Exposition de IAccessibleEx

Étant donné que l’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour un contrôle peut résider dans un objet séparé, les applications clientes ne peuvent pas compter sur [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir cette interface. Au lieu de cela, les clients sont censés appeler [**IServiceProvider :: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)). Dans l’exemple d’implémentation suivant de cette méthode, il est supposé que **IAccessibleEx** n’est pas implémenté sur un objet distinct ; par conséquent, la méthode appelle simplement via **QueryInterface**.


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a>Implémentation de IAccessibleEx

La méthode de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) qui est la plus intéressante est [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild). Cette méthode donne à Microsoft Active Accessibility Server la possibilité de créer un objet accessible (un qui expose, au minimum, **IAccessibleEx**) pour un élément enfant. Dans Microsoft Active Accessibility, les éléments enfants ne sont généralement pas représentés en tant qu’objets accessibles, mais en tant qu’enfants d’un objet accessible. Toutefois, étant donné qu’UI Automation requiert que chaque élément soit représenté par un objet accessible distinct, **GetObjectForChild** doit créer un objet distinct pour chaque enfant à la demande.

L’exemple d’implémentation suivant retourne un objet accessible pour un élément dans un affichage de liste personnalisé.


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



Pour obtenir un exemple complet d’implémentation, consultez [rendre des contrôles personnalisés accessibles, partie 5 : utilisation de IAccessibleEx pour ajouter la prise en charge d’UI Automation à un contrôle personnalisé](/previous-versions/msdn10/cc307850(v=msdn.10)) sur MSDN.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide du programmeur du fournisseur UI Automation](uiauto-providerportal.md)
</dt> </dl>

 

 