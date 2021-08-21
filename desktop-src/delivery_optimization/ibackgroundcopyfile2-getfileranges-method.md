---
title: Méthode IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization. h)
description: Récupère les plages que vous souhaitez télécharger à partir du fichier distant.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Méthode GetFileRanges
- Méthode GetFileRanges, interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, méthode GetFileRanges
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 156bb2eb1e136593bfec4310599200f2d2800e271defa0e4a3259a4a67acb648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047077"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>IBackgroundCopyFile2 :: GetFileRanges, méthode

Récupère les plages que vous souhaitez télécharger à partir du fichier distant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RangeCount* \[ in, out\]
</dt> <dd>

Nombre d’éléments dans les *plages*.

</dd> <dt>

*Plages* \[ à\]
</dt> <dd>

Tableau de structures de [**BG_FILE_RANGE**](bg-file-range.md) qui spécifient les plages à télécharger. Lorsque vous avez terminé, appelez la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer des *plages*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs de retour suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Succès<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Aucune plage n’a été spécifiée ou le travail est un travail de chargement ou de chargement-réponse. *RangeCount* a la valeur zéro et *Ranges* a la valeur **null**.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 est défini en tant que 83e81b93-0873-474d-8A8C-f2018b1a939c<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

