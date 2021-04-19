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
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a><span data-ttu-id="a9ffd-103">System. EdgeGesture. DisableTouchWhenFullscreen</span><span class="sxs-lookup"><span data-stu-id="a9ffd-103">System.EdgeGesture.DisableTouchWhenFullscreen</span></span>

<span data-ttu-id="a9ffd-104">Empêche les comportements de mouvement de bord quand une fenêtre d’application est active et en mode plein écran (ou lorsqu’une fenêtre propriétaire est active).</span><span class="sxs-lookup"><span data-stu-id="a9ffd-104">Prevents edge gesture behaviors when an application window is active and in full-screen mode (or an owned window is active).</span></span>

> [!Note]  
> <span data-ttu-id="a9ffd-105">En mode plein écran, la taille de la fenêtre d’application correspond à la résolution de l’écran.</span><span class="sxs-lookup"><span data-stu-id="a9ffd-105">In full-screen mode, the size of the application window matches the screen resolution.</span></span>

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="a9ffd-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9ffd-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

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

## <a name="remarks"></a><span data-ttu-id="a9ffd-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a9ffd-107">Remarks</span></span>

<span data-ttu-id="a9ffd-108">Dans Windows 8, les interactions de l’utilisateur avec les bords de l’écran affichent l’interface utilisateur du système, comme les barres de l’application, les icônes et les applications en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a9ffd-108">In Windows 8, user interactions with the edges of the screen display system UI such as app bars, charms, and running apps.</span></span>

<span data-ttu-id="a9ffd-109">Pour les applications distantes plein écran, ce comportement de l’interface utilisateur sur l’ordinateur local peut remplacer et interférer avec l’interface utilisateur de la session à distance.</span><span class="sxs-lookup"><span data-stu-id="a9ffd-109">For full-screen, remote applications, this UI behavior on the local machine might override and interfere with the UI of the remote session.</span></span> <span data-ttu-id="a9ffd-110">Cette propriété permet à une application de désactiver l’interface utilisateur Edge sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a9ffd-110">This property enables an application to disable the edge UI on the local machine.</span></span>

<span data-ttu-id="a9ffd-111">Pour désactiver l’interface utilisateur Edge, affectez à cette propriété la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="a9ffd-111">To disable edge UI, set this property to VARIANT\_TRUE.</span></span> <span data-ttu-id="a9ffd-112">La valeur par défaut est \_ false.</span><span class="sxs-lookup"><span data-stu-id="a9ffd-112">The default value is VARIANT\_FALSE.</span></span>

<span data-ttu-id="a9ffd-113">Cette propriété n’a aucun effet sur les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a9ffd-113">This property has no effect on Windows Store apps.</span></span>

<span data-ttu-id="a9ffd-114">L’exemple suivant montre comment définir les comportements de l’interface utilisateur Edge.</span><span class="sxs-lookup"><span data-stu-id="a9ffd-114">The following example shows how to set edge UI behaviors.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a9ffd-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9ffd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9ffd-116">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a9ffd-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a9ffd-117">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a9ffd-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a9ffd-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a9ffd-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
