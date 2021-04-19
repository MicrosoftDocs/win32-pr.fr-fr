---
description: Vérifie la signature Authenticode sur le code signé.
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: SignedCode. Verify, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540064"
---
# <a name="signedcodeverify-method"></a>SignedCode. Verify, méthode

\[La méthode **verify** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

La méthode **verify** vérifie la signature Authenticode sur le code signé.

## <a name="syntax"></a>Syntaxe


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bUIAllowed* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui spécifie si une boîte de dialogue est utilisée pour vérifier la signature. Si la valeur est true, une boîte de dialogue est générée pour déterminer si le code est approuvé. La valeur par défaut est false.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
