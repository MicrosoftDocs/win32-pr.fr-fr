---
title: Macro MCI_MAKE_MSF (Mciapi. h)
description: La \_ macro MCI make \_ crée une valeur d’heure en minutes compactées/secondes/images (MSF) à partir des valeurs de minutes, de secondes et de frames données.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942821"
---
# <a name="mci_make_msf-macro"></a>\_Créer une \_ macro pour MCI

La macro **MCI make crée une \_ \_** valeur d’heure en minutes compactées/secondes/images (MSF) à partir des valeurs de minutes, de secondes et de frames données.

## <a name="syntax"></a>Syntaxe


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*minutes* 
</dt> <dd>

Nombre de minutes.

</dd> <dt>

*secondes* 
</dt> <dd>

Nombre de secondes.

</dd> <dt>

*cadres* 
</dt> <dd>

Nombre de frames.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’heure au format MSF compressé.

## <a name="remarks"></a>Notes

L’heure au format MSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et le prochain octet le moins significatif contenant les frames. L’octet le plus significatif n’est pas utilisé.

La **macro \_ MCI \_ Make** do est définie comme suit :


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Macros MCI](mci-macros.md)
</dt> </dl>

 

 





