---
description: Empêche les comportements de mouvement de bord quand une fenêtre d’application est active et en mode plein écran (ou lorsqu’une fenêtre propriétaire est active).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System. EdgeGesture. DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527244"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a>System. EdgeGesture. DisableTouchWhenFullscreen

Empêche les comportements de mouvement de bord quand une fenêtre d’application est active et en mode plein écran (ou lorsqu’une fenêtre propriétaire est active).

> [!Note]  
> En mode plein écran, la taille de la fenêtre d’application correspond à la résolution de l’écran.

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Notes

Dans Windows 8, les interactions de l’utilisateur avec les bords de l’écran affichent l’interface utilisateur du système, comme les barres de l’application, les icônes et les applications en cours d’exécution.

Pour les applications distantes plein écran, ce comportement de l’interface utilisateur sur l’ordinateur local peut remplacer et interférer avec l’interface utilisateur de la session à distance. Cette propriété permet à une application de désactiver l’interface utilisateur Edge sur l’ordinateur local.

Pour désactiver l’interface utilisateur Edge, affectez à cette propriété la \_ valeur variant true. La valeur par défaut est \_ false.

Cette propriété n’a aucun effet sur les applications du Windows Store.

L’exemple suivant montre comment définir les comportements de l’interface utilisateur Edge.


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
