---
description: Crée une signature d’horodatage Authenticode sur le fichier exécutable signé spécifié dans la propriété SignedCode. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: SignedCode. Timestamp, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541331"
---
# <a name="signedcodetimestamp-method"></a>SignedCode. Timestamp, méthode

\[La méthode d' **horodatage** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

La méthode **timestamp** crée une signature d’horodatage Authenticode sur le fichier exécutable signé spécifié dans la propriété **SignedCode. FileName** . Cet horodatage est une signature de compteur sur le fichier exécutable signé qui est exécuté par une autorité d’horodatage.

## <a name="syntax"></a>Syntaxe


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*URL* \[ dans\]
</dt> <dd>

Chaîne qui contient l’URL du serveur d’horodatage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Un horodatage étend la validité d’un certificat en vérifiant que le fichier exécutable a été signé au moment où il a été horodaté.

Avant que cette méthode puisse être appelée, le fichier exécutable signé doit être spécifié dans la propriété **SignedCode. FileName** , et la méthode [**SignedCode. Sign**](signedcode-sign.md) doit être appelée pour signer le fichier exécutable.

Si le fichier exécutable signé est déjà horodaté, cette méthode remplace l’heure d’horodatage existante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
