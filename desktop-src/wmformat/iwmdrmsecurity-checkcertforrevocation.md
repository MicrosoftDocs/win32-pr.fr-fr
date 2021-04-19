---
title: Méthode IWMDRMSecurity CheckCertForRevocation (wmdrmsdk. h)
description: La méthode CheckCertForRevocation détermine si un certificat a été révoqué.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Méthode CheckCertForRevocation format Windows Media
- Méthode CheckCertForRevocation format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode CheckCertForRevocation
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528427"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>IWMDRMSecurity :: CheckCertForRevocation, méthode

La méthode **CheckCertForRevocation** détermine si un certificat a été révoqué.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rguidRevocationList* \[ dans\]
</dt> <dd>

GUID identifiant la liste de révocation à utiliser. Définissez l’une des valeurs du tableau suivant.



| GUID, constante                 | Description                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| \_application REVOCATIONTYPE \_ WMDRM    | Spécifie la liste de révocation des certificats d’application.                                     |
| \_appareil REVOCATIONTYPE \_ WMDRM | Spécifie la liste de révocation de certificats de l’appareil.                                          |
| \_REVOCATIONTYPE WMDRM \_ CARDEA | Spécifie la liste de révocation de certificats de Microsoft Windows Media DRM pour les périphériques réseau. |



 

</dd> <dt>

*pbCert* \[ dans\]
</dt> <dd>

Mémoire tampon contenant le certificat à rechercher.

</dd> <dt>

*cbCert* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *pbCert*, en octets.

</dd> <dt>

*fRevoked* \[ à\]
</dt> <dd>

Lors de la sortie, indique si le certificat est présent dans la liste de révocation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



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

 

 





