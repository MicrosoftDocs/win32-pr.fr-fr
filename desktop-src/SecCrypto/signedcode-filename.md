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
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535411"
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

## <a name="remarks"></a>Notes

Si la valeur de la propriété **filename** est modifiée, l’état de la totalité de l’objet [**SignedCode**](signedcode.md) est réinitialisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
