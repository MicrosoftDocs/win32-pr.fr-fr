---
description: La propriété FileName définit ou récupère le chemin d’accès au fichier exécutable. Il s’agit de la propriété par défaut.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: SignedCode. FileName, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 981ff6e1343f836ef145d1dac8c66b93d7a89c885a04cb2fe024740d7e35a53d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900379"
---
# <a name="signedcodefilename-property"></a>SignedCode. FileName, propriété

\[La propriété **nom de fichier** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

La propriété **filename** définit ou récupère le chemin d’accès au fichier exécutable. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a>Valeur de la propriété

Chemin du fichier exécutable.

## <a name="remarks"></a>Remarques

Si la valeur de la propriété **filename** est modifiée, l’état de la totalité de l’objet [**SignedCode**](signedcode.md) est réinitialisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
