---
title: Méthode IWMPLibraryServices getLibraryByType
description: La méthode getLibraryByType retourne une interface IWMPLibrary qui représente la bibliothèque qui a le type et l’index spécifiés.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- Lecteur Windows Media de la méthode getLibraryByType
- méthode getLibraryByType Lecteur Windows Media, interface IWMPLibraryServices
- Lecteur Windows Media de l’interface IWMPLibraryServices, méthode getLibraryByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414561"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>IWMPLibraryServices :: getLibraryByType, méthode

La méthode **getLibraryByType** retourne une interface **IWMPLibrary** qui représente la bibliothèque qui a le type et l’index spécifiés.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*wmplt* \[ dans\]
</dt> <dd>

Valeur de l’énumération **wmplib. WMPLibraryType** qui spécifie le type de bibliothèque à récupérer.

</dd> <dt>

*Lindex* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index de la bibliothèque à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Interface **wmplib. IWMPLibrary** pour la bibliothèque qui est retournée.

## <a name="remarks"></a>Notes

Il n’existe qu’une seule bibliothèque locale, et les bibliothèques de disques sont uniquement disponibles sur les CD et DVD de données contenant du contenu multimédia.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPLibrary (VB et C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Interface IWMPLibraryServices (VB et C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





