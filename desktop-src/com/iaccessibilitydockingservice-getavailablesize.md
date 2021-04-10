---
title: Méthode IAccessibilityDockingService GetAvailableSize
description: Obtient les dimensions disponibles pour l’ancrage d’une fenêtre d’accessibilité sur une analyse.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- Méthode GetAvailableSize COM
- Méthode GetAvailableSize COM, interface IAccessibilityDockingService
- Interface IAccessibilityDockingService COM, méthode GetAvailableSize
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030178"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a>IAccessibilityDockingService :: GetAvailableSize, méthode

Obtient les dimensions disponibles pour l’ancrage d’une fenêtre d’accessibilité sur une analyse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMonitor* \[ dans\]
</dt> <dd>

Spécifie le moniteur pour lequel la taille d’ancrage disponible sera récupérée.

</dd> <dt>

*puMaxHeight* \[ à\]
</dt> <dd>

En cas de réussite, définissez la hauteur maximale disponible pour l’ancrage sur le *hMonitor* spécifié, en pixels.

En cas d’échec, définissez sur zéro.

</dd> <dt>

*puFixedWidth* \[ à\]
</dt> <dd>

En cas de réussite, définissez la largeur fixe disponible pour l’ancrage sur le *hMonitor* spécifié, en pixels. Toute fenêtre ancrée à ce *hMonitor* sera dimensionnée à cette largeur.

En cas d’échec, définissez sur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Code de retour                                                                                                                          | Description                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                                 | Opération réussie.<br/>                                                              |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (handle de moniteur d’erreur \_ non valide \_ \_ )**</dt> </dl> | L’analyse spécifiée par le descripteur du moniteur ne prend pas en charge l’ancrage.<br/> |



 

Si *puMaxHeight* ou *puFixedWidth* a la valeur null, une violation d’accès se produit.

## <a name="remarks"></a>Notes

Les fenêtres d’accessibilité peuvent uniquement être ancrées à une analyse qui a au moins 768 pixels d’écran verticaux. Cette API n’autorise pas l’ancrage de ces fenêtres avec une hauteur qui amènerait les applications du Windows Store à avoir moins de 768 pixels d’écran verticaux.

## <a name="examples"></a>Exemples


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAccessibilityDockingService**](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





