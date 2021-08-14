---
title: Méthode IWMDRMLicense CreateSecureDecryptor (wmdrmsdk. h)
description: La méthode CreateSecureDecryptor crée un objet déchiffreur sécurisé. Le déchiffreur sécurisé diffère du déchiffreur normal en ce sens qu’il déchiffre le contenu, puis le chiffre à nouveau en fonction des paramètres spécifiés dans les paramètres de cette méthode.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Méthode CreateSecureDecryptor format Windows Media
- Méthode CreateSecureDecryptor format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode CreateSecureDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c562dcafd72a72ecef340688fd709ecbe5446abae53403d403c9a70bdd6f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433668"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>IWMDRMLicense :: CreateSecureDecryptor, méthode

La méthode **CreateSecureDecryptor** crée un objet déchiffreur sécurisé. Le déchiffreur sécurisé diffère du déchiffreur normal en ce sens qu’il déchiffre le contenu, puis le chiffre à nouveau en fonction des paramètres spécifiés dans les paramètres de cette méthode.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbCertificate* \[ dans\]
</dt> <dd>

Certificat de l’application appelante.

</dd> <dt>

*cbCertificate* \[ dans\]
</dt> <dd>

Taille du certificat en octets.

</dd> <dt>

*dwCertificateType* \[ dans\]
</dt> <dd>

Type du certificat. Définissez sur le \_ type de certificat WMDRM \_ \_ XML.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Type de protection de session à utiliser pour le ré-encodage. Doit être défini sur l’une des constantes dans le tableau suivant :



| Constante                     | Description                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| \_Type de protection WMDRM \_ \_ RC4 | Utilise le chiffrement RC4 pour le chiffrement de session. Il s’agit de la seule protection de session prise en charge pour cette version. |



 

</dd> <dt>

*pbInitializationVector* \[ à\]
</dt> <dd>

Reçoit le vecteur d’initialisation. Le vecteur d’initialisation est chiffré par RSA à l’aide du schéma de remplissage OAEP avec la clé publique RSA trouvée dans le certificat. Affectez la valeur **null** pour recevoir la taille de mémoire tampon requise dans *pcbInitializationVector*.

</dd> <dt>

*pcbInitializationVector* \[ in, out\]
</dt> <dd>

En entrée, taille de la mémoire tampon transmise en tant que *pbInitializationVector*. À la sortie, taille de la partie utilisée de la mémoire tampon. Si vous transmettez la valeur **null** pour *pbInitializationVector*, cette valeur est définie sur la taille de mémoire tampon requise sur la sortie.

</dd> <dt>

*ppDecryptor* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) de l’objet nouvellement créé.

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

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





