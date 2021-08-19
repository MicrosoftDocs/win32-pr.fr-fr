---
title: Méthode IWMDRMLicenseManagement ProcessLicenseDeletionMessage (wmdrmsdk. h)
description: La méthode ProcessLicenseDeletion supprime une licence importée pour le contenu initialement protégé par un autre système de protection du contenu.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Méthode ProcessLicenseDeletionMessage format Windows Media
- Méthode ProcessLicenseDeletionMessage format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode ProcessLicenseDeletionMessage
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369be95314ceaf3c4babce9dacd962fd3391d4f39f8988ef56f51fb3133aee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027587"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>IWMDRMLicenseManagement ::P méthode rocessLicenseDeletionMessage

La méthode **ProcessLicenseDeletion** supprime une licence importée pour le contenu initialement protégé par un autre système de protection du contenu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDeletionMessage* \[ dans\]
</dt> <dd>

Message identifiant la licence à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





