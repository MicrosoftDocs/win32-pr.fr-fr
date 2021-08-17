---
title: Méthode IWMDRMSecurity GetMachineCertificate (wmdrmsdk. h)
description: La méthode GetMachineCertificate récupère le certificat de l’ordinateur du sous-système DRM sur l’ordinateur client.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Méthode GetMachineCertificate format Windows Media
- Méthode GetMachineCertificate format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetMachineCertificate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd85a3b74ee28e5faa8df5fc264d50366803f4073ec97a36920577d417e4f97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084696"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>IWMDRMSecurity :: GetMachineCertificate, méthode

La méthode **GetMachineCertificate** récupère le certificat de l’ordinateur du sous-système DRM sur l’ordinateur client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwCertificateType* \[ dans\]
</dt> <dd>

Type de certificat à récupérer. Définissez l’une des valeurs du tableau suivant.



| Valeur                        | Description                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| \_Type de certificat WMDRM \_ \_ v1 | Le certificat sera récupéré dans le format utilisé par les composants hérités.            |
| \_Type de certificat WMDRM \_ \_ v2 | le certificat sera récupéré dans le format utilisé par les composants Windows Vista. |



 

</dd> <dt>

*rgbVersion \[ 4 \]* \[ out\]
</dt> <dd>

Tableau de quatre octets spécifiant la version du sous-système DRM sur l’ordinateur client.

</dd> <dt>

*ppbCertificate* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers les données du certificat. Affectez la valeur **null** pour que la méthode fournisse la taille de mémoire tampon nécessaire pour contenir le certificat dans *pcbCertificate*.

</dd> <dt>

*pcbCertificate* \[ in, out\]
</dt> <dd>

Taille du certificat en octets. Si *ppbCertificate* a la valeur **null**, cette valeur sera définie sur la taille du certificat. Si *ppbCertificate* n’a pas la valeur **null**, cette valeur doit être définie sur la taille de la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





