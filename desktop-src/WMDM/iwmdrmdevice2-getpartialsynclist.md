---
title: Méthode IWMDRMDevice2 GetPartialSyncList
description: La méthode GetPartialSyncList obtient une liste de synchronisation partielle.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Méthode GetPartialSyncList Gestionnaire de périphériques Windows Media
- Méthode GetPartialSyncList Gestionnaire de périphériques Windows Media, interface IWMDRMDevice2
- Interface IWMDRMDevice2 Windows Media Gestionnaire de périphériques, méthode GetPartialSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0bcff91d41ce77003219336431433ee511ff144dfcb8be7880526994689a929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055657"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>IWMDRMDevice2 :: GetPartialSyncList, méthode

La méthode **GetPartialSyncList** obtient une liste de synchronisation partielle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cMinCountThreshold* \[ dans\]
</dt> <dd>

Seuil de nombre minimal.

</dd> <dt>

*cMinHoursThreshold* \[ dans\]
</dt> <dd>

Seuil d’heures minimum.

</dd> <dt>

*dwStartingIndex* \[ dans\]
</dt> <dd>

Position de départ pour l’indexation.

</dd> <dt>

*CItems* \[ dans\]
</dt> <dd>

Nombre d’éléments à indexer.

</dd> <dt>

*ppbSyncList* \[ à\]
</dt> <dd>

Liste de synchronisation de la licence récupérée.

</dd> <dt>

*pcbSyncList* \[ à\]
</dt> <dd>

Taille de la liste de synchronisation de licence, en octets.

</dd> <dt>

*pdwNextStartingIndex* \[ à\]
</dt> <dd>

Position de début suivante pour l’indexation.

</dd> <dt>

*pcItemsProcessed* \[ à\]
</dt> <dd>

Nombre d’éléments en cours de traitement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. toutes les méthodes d’interface dans Windows Media Gestionnaire de périphériques peuvent retourner l’une des classes suivantes de codes d’erreur :

-   Codes d’erreur COM standard
-   Windows les codes d’erreur convertis en valeurs HRESULT
-   Windows Codes d’erreur du Gestionnaire de périphériques de média

Pour obtenir une liste complète des codes d’erreur possibles, consultez [codes d’erreur](error-codes.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMDRMDevice::GetSyncList**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**Interface IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





