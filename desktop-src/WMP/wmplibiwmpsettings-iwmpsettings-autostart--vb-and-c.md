---
title: IWMPSettings propriété AutoStart
description: La propriété AutoStart obtient ou définit une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- propriété de démarrage automatique lecteur Windows Media
- propriété de démarrage automatique lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété AutoStart
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526571"
---
# <a name="iwmpsettingsautostart-property"></a>IWMPSettings :: AutoStart, propriété

La propriété **AutoStart** obtient ou définit une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Valeur de la propriété

Valeur **System. Boolean** qui indique si l’élément multimédia actuel commence à être lu automatiquement. La valeur par défaut est **true**.

## <a name="remarks"></a>Notes

Si **AutoStart** est défini sur **true**, l’élément multimédia commence à s’exécuter quand **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentPlaylist** ou **AxWindowsMediaPlayer. currentMedia** est défini. Dans le cas contraire, l’élément multimédia ne démarre pas tant que la méthode **IWMPControls. Play** n’est pas appelée.

À moins que vous n’ayez défini **AutoStart** sur **true** juste avant de spécifier un élément multimédia, vous ne devez pas compter sur ce paramètre en remplacement de l’utilisation de la méthode **IWMPControls. Play** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB et C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. currentPlaylist (VB et C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB et C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





