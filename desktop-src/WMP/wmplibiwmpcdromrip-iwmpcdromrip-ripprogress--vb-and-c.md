---
title: IWMPCdromRip propriété ripProgress
description: La propriété ripProgress obtient la progression de l’extraction de CD comme pourcentage d’achèvement.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- Lecteur Windows Media de la propriété ripProgress
- Lecteur Windows Media de la propriété ripProgress, interface IWMPCdromRip
- Lecteur Windows Media de l’interface IWMPCdromRip, propriété ripProgress
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0d80a9eeed0246c48c142177bb4611c8666ca8b4f783d51f472dada2bbdbc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246749"
---
# <a name="iwmpcdromripripprogress-property"></a>IWMPCdromRip :: ripProgress, propriété

La propriété **ripProgress** obtient la progression de l’extraction de CD comme pourcentage d’achèvement.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est la valeur de progression. Les valeurs de progression sont comprises entre 0 et 100.

## <a name="remarks"></a>Remarques

La valeur de progression représente le pourcentage terminé de l’ensemble du processus d’extraction. Pour déterminer la progression d’une piste spécifique, utilisez [IWMPMedia. getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) avec **RipProgress** comme nom d’attribut. Pour récupérer l’index de la piste actuellement extraite, appelez IWMPPlaylist. getItemInfo avec « CurrentRipTrackIndex » comme nom d’attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromRip (VB et C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Extraction d’un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





