---
title: Méthode IWMDRMLicense GetOutputProtectionLevels
description: La méthode GetOutputProtectionLevels récupère des informations sur tous les niveaux de protection de sortie (OPLs) affectés à la licence.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Méthode GetOutputProtectionLevels format Windows Media
- Méthode GetOutputProtectionLevels format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetOutputProtectionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8d70aaae5e96b8328c091e49836ae743c0fd5ef9d5036fd5aca067f9305d7fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771319"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>IWMDRMLicense :: GetOutputProtectionLevels, méthode

La méthode **GetOutputProtectionLevels** récupère des informations sur tous les niveaux de protection de sortie (OPLs) affectés à la licence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pOPLs* \[ à\]
</dt> <dd>

Pointeur vers une structure de [**\_ niveaux de \_ protection \_ de sortie WMDRM**](wmdrm-output-protection-levels.md) qui reçoit les informations OPL.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





