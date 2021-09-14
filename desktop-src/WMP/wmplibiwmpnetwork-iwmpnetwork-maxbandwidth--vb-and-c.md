---
title: IWMPNetwork propriété maxBandwidth
description: La propriété maxBandwidth obtient ou définit la bande passante maximale autorisée.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- Lecteur Windows Media de la propriété maxBandwidth
- Lecteur Windows Media de la propriété maxBandwidth, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, propriété maxBandwidth
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232847"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a>IWMPNetwork :: maxBandwidth, propriété

La propriété **maxBandwidth** obtient ou définit la bande passante maximale autorisée.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond à la bande passante maximale.

## <a name="remarks"></a>Notes

Cette propriété n’a pas de valeur par défaut. la valeur peut être spécifiée pendant que Lecteur Windows Media est en cours de diffusion, mais la modification ne prend pas effet tant que l’élément multimédia actuel n’est pas libéré en ouvrant un autre élément ou en appelant **AxWindowsMediaPlayer. close**. Lecteur Windows Media tente d’obtenir la bande passante la plus élevée possible. Aucune réduction intentionnelle de la bande passante ne se produit, sauf si cette valeur est définie.

Ce paramètre est utile pour réduire la quantité de bande passante utilisée, en particulier dans le cas d’un flux de la vitesse de transmission multiple (MBR). Un flux MBR contient plusieurs flux avec différentes vitesses de transmission. Dans certains cas, il peut être souhaitable d’utiliser un flux avec une vitesse de transmission inférieure à celle requise par le client. Dans ce cas, la spécification d’une vitesse de transmission inférieure avec la propriété **IWMPNetwork. maxBandwidth** sélectionnera un flux de vitesse de transmission inférieur. Par exemple, un flux de données MBR peut inclure des flux encodés à 20 kilobits par seconde (Kbits/s), 37 Kbits/s et 200 kbit/s. L’utilisation de **IWMPNetwork. maxBandwidth** pour spécifier une vitesse de transmission de 50 000 (50 kbps) sélectionnera le flux de 37 Kbits/s au lieu du flux de 200 Kbits/s.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AxWindowsMediaPlayer. close (VB et C#)**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





