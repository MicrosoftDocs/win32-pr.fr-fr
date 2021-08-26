---
title: Méthode IWMDRMLicenseManagement ProcessLicenseRevocationResponse (wmdrmsdk. h)
description: La méthode ProcessLicenseRevocationResponse révoque les licences du magasin de licences local. Cette méthode utilise un objet blob de révocation de licence (LRB) reçu à partir d’un serveur de révocation de licences pour identifier les licences à révoquer.
ms.assetid: 4428ac44-c3f4-404e-9997-cbc7360faedf
keywords:
- Méthode ProcessLicenseRevocationResponse format Windows Media
- Méthode ProcessLicenseRevocationResponse format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode ProcessLicenseRevocationResponse
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseRevocationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d58c33f79db575dec37d7d2ac51e3c65b10416b9ca35a50084f36a56693854be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930309"
---
# <a name="iwmdrmlicensemanagementprocesslicenserevocationresponse-method"></a>IWMDRMLicenseManagement ::P méthode rocessLicenseRevocationResponse

La méthode **ProcessLicenseRevocationResponse** révoque les licences du magasin de licences local. Cette méthode utilise un objet blob de révocation de licence (LRB) reçu à partir d’un serveur de révocation de licences pour identifier les licences à révoquer.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ProcessLicenseRevocationResponse(
  [in]  BYTE  *pbSignedLRB,
  [in]  DWORD cbSignedLRB,
  [out] BYTE  **ppbSignedACK,
  [out] DWORD *pcbSignedACK
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbSignedLRB* \[ dans\]
</dt> <dd>

Objet blob de révocation de licence (LRB) reçu du serveur de révocation de licences en réponse à une stimulation générée en appelant la méthode [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .

</dd> <dt>

*cbSignedLRB* \[ dans\]
</dt> <dd>

Taille du LRB en octets.

</dd> <dt>

*ppbSignedACK* \[ à\]
</dt> <dd>

Adresse d’un pointeur qui reçoit l’adresse de l’accusé de réception de la révocation de licence. L’accusé de réception doit être envoyé au service de révocation de licence. Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.

</dd> <dt>

*pcbSignedACK* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit la taille de l’accusé de réception en octets.

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

 

 





