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
# <a name="using-direct-annotation"></a>Utilisation de l’annotation directe

**Pour utiliser l’annotation directe pour remplacer la valeur d’une propriété**

1.  Utilisez la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ou [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) pour créer l’objet [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
2.  Appelez [**IAccPropServices :: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), en passant le **HWND**, l’ID d’objet, l’ID enfant, la propriété à substituer et un [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) contenant la nouvelle valeur de la propriété. Cette étape annote la valeur.
3.  Libérez les pointeurs d’interface et la mémoire libre.

L’exemple suivant montre comment annoter la propriété [**role**](role-property.md) d’un contrôle de texte statique.


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



## <a name="properties-supported-when-specifying-a-value"></a>Propriétés prises en charge lors de la spécification d’une valeur

Les propriétés de Active Accessibility Microsoft suivantes peuvent être annotées lors de la spécification d’une valeur (où la valeur doit être du type noté) pour l’annotation directe. Pour remplacer ou ajouter une propriété Microsoft UI Automation à un contrôle, vous pouvez spécifier l’ID de propriété UI Automation à la place de l’ID de propriété Microsoft Active Accessibility. Pour obtenir la liste des ID UI Automation, consultez [identificateurs de propriété](uiauto-entry-propids.md).



| Propriété                      | Type     |
|-------------------------------|----------|
| \_nom du compte propid \_             | VT \_ BSTR |
| \_Description du compte propid \_      | VT \_ BSTR |
| \_rôle de compte propid \_             | VT \_   |
| \_État du compte propid \_            | VT \_   |
| \_aide sur le compte propid \_             | VT \_ BSTR |
| \_KEYBOARDSHORTCUT de compte propid \_ | VT \_ BSTR |
| ID de l' \_ \_ DefaultAction ACC    | VT \_ BSTR |
| PROPID \_ compte \_ VALUEMAP         | VT \_ BSTR |
| \_ROLEMAP de compte propid \_          | VT \_ BSTR |
| \_STATEMAP de compte propid \_         | VT \_ BSTR |



 

 

 