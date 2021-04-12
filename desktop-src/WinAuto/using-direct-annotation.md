---
title: Utilisation de l’annotation directe
description: Utilisation de l’annotation directe
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f0bdea5af896329b6836d21ca1dcee25bc2739
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315660"
---
# <a name="using-direct-annotation"></a><span data-ttu-id="0ec25-103">Utilisation de l’annotation directe</span><span class="sxs-lookup"><span data-stu-id="0ec25-103">Using Direct Annotation</span></span>

<span data-ttu-id="0ec25-104">**Pour utiliser l’annotation directe pour remplacer la valeur d’une propriété**</span><span class="sxs-lookup"><span data-stu-id="0ec25-104">**To use direct annotation to override the value of a property**</span></span>

1.  <span data-ttu-id="0ec25-105">Utilisez la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ou [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) pour créer l’objet [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="0ec25-105">Use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) function to create the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) object.</span></span>
2.  <span data-ttu-id="0ec25-106">Appelez [**IAccPropServices :: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), en passant le **HWND**, l’ID d’objet, l’ID enfant, la propriété à substituer et un [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) contenant la nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0ec25-106">Call [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passing the **HWND**, object ID, child ID, the property to be overridden, and a [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) containing the new value of the property.</span></span> <span data-ttu-id="0ec25-107">Cette étape annote la valeur.</span><span class="sxs-lookup"><span data-stu-id="0ec25-107">This step annotates the value.</span></span>
3.  <span data-ttu-id="0ec25-108">Libérez les pointeurs d’interface et la mémoire libre.</span><span class="sxs-lookup"><span data-stu-id="0ec25-108">Release the interface pointers and free memory.</span></span>

<span data-ttu-id="0ec25-109">L’exemple suivant montre comment annoter la propriété [**role**](role-property.md) d’un contrôle de texte statique.</span><span class="sxs-lookup"><span data-stu-id="0ec25-109">The following example shows how to annotate the [**Role**](role-property.md) property of a static text control.</span></span>


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a><span data-ttu-id="0ec25-110">Propriétés prises en charge lors de la spécification d’une valeur</span><span class="sxs-lookup"><span data-stu-id="0ec25-110">Properties Supported When Specifying a Value</span></span>

<span data-ttu-id="0ec25-111">Les propriétés de Active Accessibility Microsoft suivantes peuvent être annotées lors de la spécification d’une valeur (où la valeur doit être du type noté) pour l’annotation directe.</span><span class="sxs-lookup"><span data-stu-id="0ec25-111">The following Microsoft Active Accessibility properties can be annotated when specifying a value (where the value must be of the noted type) for direct annotation.</span></span> <span data-ttu-id="0ec25-112">Pour remplacer ou ajouter une propriété Microsoft UI Automation à un contrôle, vous pouvez spécifier l’ID de propriété UI Automation à la place de l’ID de propriété Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="0ec25-112">To override or add a Microsoft UI Automation property to a control, you can specify the UI Automation property ID instead of the Microsoft Active Accessibility property ID.</span></span> <span data-ttu-id="0ec25-113">Pour obtenir la liste des ID UI Automation, consultez [identificateurs de propriété](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="0ec25-113">For a list of UI Automation IDs, see [Property Identifiers](uiauto-entry-propids.md).</span></span>



| <span data-ttu-id="0ec25-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ec25-114">Property</span></span>                      | <span data-ttu-id="0ec25-115">Type</span><span class="sxs-lookup"><span data-stu-id="0ec25-115">Type</span></span>     |
|-------------------------------|----------|
| <span data-ttu-id="0ec25-116">\_nom du compte propid \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-116">PROPID\_ACC\_NAME</span></span>             | <span data-ttu-id="0ec25-117">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="0ec25-117">VT\_BSTR</span></span> |
| <span data-ttu-id="0ec25-118">\_Description du compte propid \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-118">PROPID\_ACC\_DESCRIPTION</span></span>      | <span data-ttu-id="0ec25-119">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="0ec25-119">VT\_BSTR</span></span> |
| <span data-ttu-id="0ec25-120">\_rôle de compte propid \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-120">PROPID\_ACC\_ROLE</span></span>             | <span data-ttu-id="0ec25-121">VT \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-121">VT\_I4</span></span>   |
| <span data-ttu-id="0ec25-122">\_État du compte propid \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-122">PROPID\_ACC\_STATE</span></span>            | <span data-ttu-id="0ec25-123">VT \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-123">VT\_I4</span></span>   |
| <span data-ttu-id="0ec25-124">\_aide sur le compte propid \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-124">PROPID\_ACC\_HELP</span></span>             | <span data-ttu-id="0ec25-125">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="0ec25-125">VT\_BSTR</span></span> |
| <span data-ttu-id="0ec25-126">\_KEYBOARDSHORTCUT de compte propid \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-126">PROPID\_ACC\_KEYBOARDSHORTCUT</span></span> | <span data-ttu-id="0ec25-127">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="0ec25-127">VT\_BSTR</span></span> |
| <span data-ttu-id="0ec25-128">ID de l' \_ \_ DefaultAction ACC</span><span class="sxs-lookup"><span data-stu-id="0ec25-128">PROPID\_ACC\_DEFAULTACTION</span></span>    | <span data-ttu-id="0ec25-129">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="0ec25-129">VT\_BSTR</span></span> |
| <span data-ttu-id="0ec25-130">PROPID \_ compte \_ VALUEMAP</span><span class="sxs-lookup"><span data-stu-id="0ec25-130">PROPID\_ACC\_VALUEMAP</span></span>         | <span data-ttu-id="0ec25-131">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="0ec25-131">VT\_BSTR</span></span> |
| <span data-ttu-id="0ec25-132">\_ROLEMAP de compte propid \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-132">PROPID\_ACC\_ROLEMAP</span></span>          | <span data-ttu-id="0ec25-133">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="0ec25-133">VT\_BSTR</span></span> |
| <span data-ttu-id="0ec25-134">\_STATEMAP de compte propid \_</span><span class="sxs-lookup"><span data-stu-id="0ec25-134">PROPID\_ACC\_STATEMAP</span></span>         | <span data-ttu-id="0ec25-135">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="0ec25-135">VT\_BSTR</span></span> |



 

 

 