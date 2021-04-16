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
# <a name="exposing-controls-based-on-system-controls"></a><span data-ttu-id="c8cd9-103">Exposition de contrôles basés sur des contrôles système</span><span class="sxs-lookup"><span data-stu-id="c8cd9-103">Exposing Controls Based on System Controls</span></span>

<span data-ttu-id="c8cd9-104">Vous devez envisager d’utiliser une forme d’annotation dynamique (directe, carte de valeur ou serveur) avant de tenter la technique décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-104">You should consider using some form of Dynamic Annotation—Direct, Value Map, or Server—before attempting the technique described in this section.</span></span> <span data-ttu-id="c8cd9-105">Pour plus d’informations, consultez [API d’annotation dynamique](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="c8cd9-105">For more information, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

<span data-ttu-id="c8cd9-106">Dans la plupart des cas, Microsoft Active Accessibility expose des informations sur les contrôles superclassés ou sous-classés.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-106">In most cases, Microsoft Active Accessibility exposes information about superclassed or subclassed controls.</span></span> <span data-ttu-id="c8cd9-107">La superclassement et les sous-classes permettent à un développeur d’applications de créer un contrôle personnalisé avec les fonctionnalités de base d’un contrôle système et d’inclure des améliorations fournies par l’application.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-107">Superclassing and subclassing allow an application developer to create a custom control with the basic functionality of a system control and include enhancements provided by the application.</span></span> <span data-ttu-id="c8cd9-108">Un contrôle superclassé a un nom de classe de fenêtre différent du contrôle système sur lequel il est basé.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-108">A superclassed control has a different window class name than the system control on which it is based.</span></span> <span data-ttu-id="c8cd9-109">Un contrôle sous-classé possède le même nom de classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-109">A subclassed control has the same window class name.</span></span> <span data-ttu-id="c8cd9-110">Pour plus d’informations sur les surclassements et les sous-classes, consultez la documentation du kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-110">For more information about superclassing and subclassing, see the Windows Software Development Kit (SDK) documentation.</span></span>

<span data-ttu-id="c8cd9-111">Étant donné que Microsoft Active Accessibility expose des informations sur les contrôles fournis par le système, Microsoft Active Accessibility expose le contrôle modifié, sauf si un contrôle en surclasse ou sous-classé est très différent du contrôle de base.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-111">Because Microsoft Active Accessibility exposes information about system-provided controls, Microsoft Active Accessibility exposes the modified control unless a superclassed or subclassed control is significantly different from the base control.</span></span> <span data-ttu-id="c8cd9-112">Pour déterminer si le contrôle modifié est accessible, les développeurs d’applications doivent utiliser des utilitaires tels que [inspecter](inspect-objects.md) et accès à l' [Observateur d’événements](accessible-event-watcher.md) pour comparer le comportement du contrôle modifié au contrôle de base.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-112">To determine if the modified control is accessible, application developers should use utilities such as [Inspect](inspect-objects.md) and [Accessible Event Watcher](accessible-event-watcher.md) to compare the behavior of the modified control with the base control.</span></span>

<span data-ttu-id="c8cd9-113">Si, après avoir utilisé ces utilitaires, vous déterminez que le contrôle modifié n’est pas accessible, vous devez traiter le contrôle comme n’importe quel autre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-113">If after using these utilities you determine that the modified control is not accessible, you must treat the control as any other custom control.</span></span> <span data-ttu-id="c8cd9-114">Le contrôle doit déclencher des événements, et la procédure de fenêtre de l’application doit répondre au message [**WM \_ GETOBJECT**](wm-getobject.md)en fournissant une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que les applications clientes utilisent pour obtenir des informations sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-114">The control must trigger events, and the application's window procedure must respond to the [**WM\_GETOBJECT**](wm-getobject.md)message by supplying an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface that client applications use to obtain information about the control.</span></span>

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a><span data-ttu-id="c8cd9-115">CreateStdAccessibleProxy et CreateStdAccessibleObject</span><span class="sxs-lookup"><span data-stu-id="c8cd9-115">CreateStdAccessibleProxy and CreateStdAccessibleObject</span></span>

<span data-ttu-id="c8cd9-116">Si la totalité ou la plupart des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour le contrôle modifié sont les mêmes que le contrôle de base, utilisez [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) ou [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) pour simplifier l’implémentation de l’interface **IAccessible** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-116">If all or most of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for the modified control are the same as the base control, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) or [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) to simplify the implementation of the control's **IAccessible** interface.</span></span>

> [!Note]  
> <span data-ttu-id="c8cd9-117">Lors de la superclassement ou de la sous-classe d’un contrôle accessible, sachez que l’objet récupéré par la fonction [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) peut implémenter plus qu’une seule interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="c8cd9-117">When superclassing or subclassing an accessible control, be aware that the object retrieved by the [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) function may implement more than just the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="c8cd9-118">Elle peut inclure d’autres interfaces telles que [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span><span class="sxs-lookup"><span data-stu-id="c8cd9-118">It may include other interfaces such as [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span></span> <span data-ttu-id="c8cd9-119">Vous devrez peut-être encapsuler ces interfaces supplémentaires pour conserver la prise en charge de l’accessibilité fournie par le implémentation d’origine du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-119">You might need to wrap these additional interfaces to retain the accessibility support provided by the original implemenation of the control.</span></span>

 

<span data-ttu-id="c8cd9-120">Les fonctions [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) et [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) récupèrent un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour le contrôle système spécifié.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-120">The [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) and [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) functions retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the specified system control.</span></span> <span data-ttu-id="c8cd9-121">La différence dans ces fonctions est que **CreateStdAccessibleObject** utilise le nom de classe de fenêtre obtenu à partir de son paramètre *HWND* alors que **CreateStdAccessibleProxy** utilise le nom de classe de fenêtre spécifié dans son paramètre *szClassName* .</span><span class="sxs-lookup"><span data-stu-id="c8cd9-121">The difference in these functions is that **CreateStdAccessibleObject** uses the window class name obtained from its *hwnd* parameter whereas **CreateStdAccessibleProxy** uses the window class name specified in its *szClassName* parameter.</span></span> <span data-ttu-id="c8cd9-122">Par conséquent, si vous décidez d’utiliser ces fonctions, utilisez **CreateStdAccessibleProxy** pour exposer des informations sur les contrôles superclassés, et sur l’une ou l’autre des fonctions avec des contrôles sous-classés.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-122">Therefore, if you decide to use these functions, use **CreateStdAccessibleProxy** to expose information about superclassed controls, and either function with subclassed controls.</span></span>

<span data-ttu-id="c8cd9-123">Après avoir obtenu un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) vers le contrôle système, utilisez le pointeur dans votre implémentation de l’interface **IAccessible** pour le contrôle modifié.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-123">After obtaining an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to the system control, use the pointer in your implementation of the **IAccessible** interface for the modified control.</span></span> <span data-ttu-id="c8cd9-124">Si une propriété ou une méthode pour le contrôle modifié est identique au contrôle de base, utilisez le pointeur **IAccessible** pour retourner les informations fournies par le contrôle de base.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-124">If a property or method for the modified control is the same as the base control, use the **IAccessible** pointer to return the information provided by the base control.</span></span> <span data-ttu-id="c8cd9-125">Si une propriété du contrôle modifié est différente du contrôle de base, substituez la propriété du contrôle de base.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-125">If a property for the modified control is different from the base control, override the base control's property.</span></span>

<span data-ttu-id="c8cd9-126">Dans l’exemple suivant, **CAccCustomButton** est la classe définie par l’application dérivée de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="c8cd9-126">In the following example, **CAccCustomButton** is the application-defined class derived from [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="c8cd9-127">La variable membre **m \_ pAccDefaultButton** est un pointeur vers une interface **IAccessible** qui a été récupérée à partir de [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) pendant la procédure d’initialisation du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-127">The member variable **m\_pAccDefaultButton** is a pointer to an **IAccessible** interface that was retrieved from [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) during the initialization procedure for the control.</span></span> <span data-ttu-id="c8cd9-128">Dans cet exemple, la propriété **role** du contrôle personnalisé est la même que la propriété **role** du contrôle système, de sorte que la propriété **role** du contrôle de base est retournée.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-128">In this example, the **Role** property for the custom control is the same as the **Role** property of the system control, so the **Role** property of the base control is returned.</span></span> <span data-ttu-id="c8cd9-129">Toutefois, la propriété **Description** est différente de celle du contrôle de base, donc cette propriété est substituée.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-129">However, the **Description** property is different from that of the base control, so this property is overridden.</span></span>


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



<span data-ttu-id="c8cd9-130">Pour plus d’informations sur les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des contrôles système, consultez [annexe A : informations de référence sur les éléments d’interface utilisateur pris en charge](appendix-a--supported-user-interface-elements-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c8cd9-130">For more information about the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of system controls, see [Appendix A: Supported User Interface Elements Reference](appendix-a--supported-user-interface-elements-reference.md).</span></span>

 

 