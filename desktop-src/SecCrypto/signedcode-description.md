---
description: Définit ou récupère la description du fichier exécutable signé.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: Propriété SignedCode. Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5783dd5e662aed33722a1c587bfcdc3cab76c78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123066"
---
# <a name="signedcodedescription-property"></a>Propriété SignedCode. Description

\[La propriété **Description** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

La propriété **Description** définit ou récupère la description du fichier exécutable signé.

## <a name="syntax"></a>Syntaxe


```VB
SignedCode.Description As String
```



## <a name="property-value"></a>Valeur de la propriété

Description du fichier exécutable signé.

## <a name="remarks"></a>Notes

La description est le texte qui apparaît dans la boîte de dialogue vérification Authenticode. Le texte doit décrire le fichier exécutable signé. Si cette propriété a la **valeur null**, la boîte de dialogue affiche le nom du fichier exécutable.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
