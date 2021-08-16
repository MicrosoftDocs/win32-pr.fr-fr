---
title: Méthode IWMDRMLicense GetInclusionList (wmdrmsdk. h)
description: La méthode GetInclusionList récupère la liste d’inclusion entière pour la licence ou la chaîne de licences actuelle.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Méthode GetInclusionList format Windows Media
- Méthode GetInclusionList format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetInclusionList
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6389ac30d5bffeb6ad354ec6c7e83f2834921fe8fb83c1abe2bca2d0c2f43bfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705239"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a>IWMDRMLicense :: GetInclusionList, méthode

La méthode **GetInclusionList** récupère la liste d’inclusion entière pour la licence ou la chaîne de licences actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppGuids* \[ à\]
</dt> <dd>

Reçoit un tableau de GUID identifiant les technologies incluses.

</dd> <dt>

*pcGuids* \[ à\]
</dt> <dd>

Reçoit le nombre d’éléments dans le tableau *ppGuids* . Le tableau est alloué à l’aide de **CoTaskMemAlloc**. Lorsque vous avez terminé avec la liste, libérez de la mémoire en appelant **CoTaskMemFree**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

L’émetteur de licence peut spécifier d’autres systèmes de protection sur lesquels le contenu chiffré peut être converti. La liste des GUID récupérés par cette méthode identifie les systèmes de protection autorisés. Lorsque vous entrez dans un contrat de licence avec Microsoft pour obtenir la bibliothèque stub, vous recevrez une liste des systèmes de protection actuellement pris en charge et les GUID utilisés pour les identifier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Listes d’autorisations et d’inclusion explicites**](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





