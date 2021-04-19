---
title: Méthode IWMDRMLicenseManagement CreateLicenseRevocationChallenge (wmdrmsdk. h)
description: La méthode CreateLicenseRevocationChallenge génère une demande de révocation de licence.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Méthode CreateLicenseRevocationChallenge format Windows Media
- Méthode CreateLicenseRevocationChallenge format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode CreateLicenseRevocationChallenge
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528523"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>IWMDRMLicenseManagement :: CreateLicenseRevocationChallenge, méthode

La méthode **CreateLicenseRevocationChallenge** génère une demande de révocation de licence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbMachineID* \[ dans\]
</dt> <dd>

Identificateur de l’ordinateur spécifié par l’utilisateur. Cette valeur est utilisée pour interroger une licence sur le serveur et doit être conforme au format utilisé par le serveur de licences.

</dd> <dt>

*cbMachineID* \[ dans\]
</dt> <dd>

Taille, en octets, de l’identificateur de l’ordinateur.

</dd> <dt>

*pbChallenge* \[ dans\]
</dt> <dd>

Données de stimulation spécifiées par l’utilisateur. Ces données, en plus de l’identificateur de l’ordinateur, sont utilisées pour interroger le serveur de licences afin d’identifier les licences à révoquer.

</dd> <dt>

*cbChallenge* \[ dans\]
</dt> <dd>

Taille, en octets, des données de stimulation.

</dd> <dt>

*ppbChallengeOutput* \[ à\]
</dt> <dd>

Adresse d’un pointeur qui reçoit l’adresse de la sortie de la stimulation. Cette mémoire tampon est celle qui est envoyée au service de révocation de licence. Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.

</dd> <dt>

*pcbChallengeOutput* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit la taille des données de sortie de la stimulation allouée, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



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

 

 





