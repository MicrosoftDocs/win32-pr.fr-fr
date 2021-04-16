---
title: Exposition de contrôles basés sur des contrôles système
description: Exposition de contrôles basés sur des contrôles système
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382418"
---
# <a name="exposing-controls-based-on-system-controls"></a>Exposition de contrôles basés sur des contrôles système

Vous devez envisager d’utiliser une forme d’annotation dynamique (directe, carte de valeur ou serveur) avant de tenter la technique décrite dans cette section. Pour plus d’informations, consultez [API d’annotation dynamique](dynamic-annotation-api.md).

Dans la plupart des cas, Microsoft Active Accessibility expose des informations sur les contrôles superclassés ou sous-classés. La superclassement et les sous-classes permettent à un développeur d’applications de créer un contrôle personnalisé avec les fonctionnalités de base d’un contrôle système et d’inclure des améliorations fournies par l’application. Un contrôle superclassé a un nom de classe de fenêtre différent du contrôle système sur lequel il est basé. Un contrôle sous-classé possède le même nom de classe de fenêtre. Pour plus d’informations sur les surclassements et les sous-classes, consultez la documentation du kit de développement logiciel (SDK) Windows.

Étant donné que Microsoft Active Accessibility expose des informations sur les contrôles fournis par le système, Microsoft Active Accessibility expose le contrôle modifié, sauf si un contrôle en surclasse ou sous-classé est très différent du contrôle de base. Pour déterminer si le contrôle modifié est accessible, les développeurs d’applications doivent utiliser des utilitaires tels que [inspecter](inspect-objects.md) et accès à l' [Observateur d’événements](accessible-event-watcher.md) pour comparer le comportement du contrôle modifié au contrôle de base.

Si, après avoir utilisé ces utilitaires, vous déterminez que le contrôle modifié n’est pas accessible, vous devez traiter le contrôle comme n’importe quel autre contrôle personnalisé. Le contrôle doit déclencher des événements, et la procédure de fenêtre de l’application doit répondre au message [**WM \_ GETOBJECT**](wm-getobject.md)en fournissant une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que les applications clientes utilisent pour obtenir des informations sur le contrôle.

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a>CreateStdAccessibleProxy et CreateStdAccessibleObject

Si la totalité ou la plupart des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour le contrôle modifié sont les mêmes que le contrôle de base, utilisez [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) ou [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) pour simplifier l’implémentation de l’interface **IAccessible** du contrôle.

> [!Note]  
> Lors de la superclassement ou de la sous-classe d’un contrôle accessible, sachez que l’objet récupéré par la fonction [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) peut implémenter plus qu’une seule interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Elle peut inclure d’autres interfaces telles que [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant). Vous devrez peut-être encapsuler ces interfaces supplémentaires pour conserver la prise en charge de l’accessibilité fournie par le implémentation d’origine du contrôle.

 

Les fonctions [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) et [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) récupèrent un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour le contrôle système spécifié. La différence dans ces fonctions est que **CreateStdAccessibleObject** utilise le nom de classe de fenêtre obtenu à partir de son paramètre *HWND* alors que **CreateStdAccessibleProxy** utilise le nom de classe de fenêtre spécifié dans son paramètre *szClassName* . Par conséquent, si vous décidez d’utiliser ces fonctions, utilisez **CreateStdAccessibleProxy** pour exposer des informations sur les contrôles superclassés, et sur l’une ou l’autre des fonctions avec des contrôles sous-classés.

Après avoir obtenu un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) vers le contrôle système, utilisez le pointeur dans votre implémentation de l’interface **IAccessible** pour le contrôle modifié. Si une propriété ou une méthode pour le contrôle modifié est identique au contrôle de base, utilisez le pointeur **IAccessible** pour retourner les informations fournies par le contrôle de base. Si une propriété du contrôle modifié est différente du contrôle de base, substituez la propriété du contrôle de base.

Dans l’exemple suivant, **CAccCustomButton** est la classe définie par l’application dérivée de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). La variable membre **m \_ pAccDefaultButton** est un pointeur vers une interface **IAccessible** qui a été récupérée à partir de [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) pendant la procédure d’initialisation du contrôle. Dans cet exemple, la propriété **role** du contrôle personnalisé est la même que la propriété **role** du contrôle système, de sorte que la propriété **role** du contrôle de base est retournée. Toutefois, la propriété **Description** est différente de celle du contrôle de base, donc cette propriété est substituée.


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



Pour plus d’informations sur les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des contrôles système, consultez [annexe A : informations de référence sur les éléments d’interface utilisateur pris en charge](appendix-a--supported-user-interface-elements-reference.md).

 

 