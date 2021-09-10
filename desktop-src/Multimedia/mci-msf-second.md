---
title: Macro MCI_MSF_SECOND (Mciapi. h)
description: La \_ macro MCI MSF \_ second récupère le composant seconds à partir d’un paramètre contenant les informations de minutes/secondes/frames (MSF) compressées.
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND macro Windows multimédia
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363971"
---
# <a name="mci_msf_second-macro"></a>\_Macro MCI MSF \_ second

La macro **MCI \_ MSF \_ second** récupère le composant seconds à partir d’un paramètre contenant les informations de minutes/secondes/frames (MSF) compressées.

## <a name="syntax"></a>Syntaxe


```C++
BYTE MCI_MSF_SECOND(
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

Retourne le composant « secondes » des informations MSF spécifiées.

## <a name="remarks"></a>Remarques

L’heure au format MSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et le prochain octet le moins significatif contenant les frames. L’octet le plus significatif n’est pas utilisé.

La **\_ \_ deuxième macro MCI MSF** est définie comme suit :


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
```



## <a name="requirements"></a>Spécifications



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

 

 





