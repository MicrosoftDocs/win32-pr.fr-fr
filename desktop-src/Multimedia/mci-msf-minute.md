---
title: Macro MCI_MSF_MINUTE (Mciapi. h)
description: La \_ macro MCI MSF \_ minute récupère le composant minutes à partir d’un paramètre contenant les informations de minutes/secondes/frames (MSF) compressées.
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515482"
---
# <a name="mci_msf_minute-macro"></a>\_Macro MCI MSF \_ minute

La macro **MCI \_ MSF \_ minute** récupère le composant minutes à partir d’un paramètre contenant les informations de minutes/secondes/frames (MSF) compressées.

## <a name="syntax"></a>Syntaxe


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwMSF* 
</dt> <dd>

Heure au format MSF.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le composant « minutes » des informations MSF spécifiées.

## <a name="remarks"></a>Notes

L’heure au format MSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et le prochain octet le moins significatif contenant les frames. L’octet le plus significatif n’est pas utilisé.

La macro **MCI \_ MSF \_ minute** est définie comme suit :


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
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

 

 





