---
description: Crée une signature numérique Authenticode et signe le fichier exécutable spécifié dans la propriété SignedCode. FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: SignedCode. Sign, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541435"
---
# <a name="signedcodesign-method"></a>SignedCode. Sign, méthode

\[La méthode **Sign** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

La méthode **Sign** crée une signature numérique Authenticode et signe le fichier exécutable spécifié dans la propriété [**SignedCode. FileName**](signedcode-filename.md) .

## <a name="syntax"></a>Syntaxe


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Signataire* \[ dans, facultatif\]
</dt> <dd>

Objet [**signataire**](signer.md) qui a accès à la clé privée du certificat utilisé pour signer le code. La valeur par défaut est **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Avant l’appel de la méthode **Sign** , le fichier qui contient le code doit être spécifié dans la propriété [**filename**](signedcode-filename.md) .

Si le fichier exécutable est déjà signé, cette méthode remplace la signature existante.

Les résultats suivants s’appliquent à la valeur du paramètre de *signataire* :

-   Si le paramètre de *signataire* n’a pas la **valeur null**, cette méthode utilise la clé privée désignée par le certificat associé pour chiffrer la signature. Si la clé privée vers laquelle pointe le certificat n’est pas disponible, la méthode échoue.
-   Si le paramètre de *signataire* a la **valeur null** et qu’il y a exactement un certificat dans l' \_ utilisateur actuel mon magasin qui a accès à une clé privée avec la fonctionnalité de signature de code, ce certificat est utilisé pour créer la signature.
-   Si le paramètre de *signataire* est **null**, la valeur de la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) est true et il existe plusieurs certificats dans le magasin de l' \_ utilisateur actuel mon magasin avec une clé privée disponible avec la fonctionnalité de signature de code, une boîte de dialogue s’affiche et permet à l’utilisateur de sélectionner le certificat à utiliser.
-   Si le paramètre de *signataire* a la **valeur null** et que la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) a la valeur false, la méthode échoue.
-   Si le paramètre de *signataire* a la **valeur null** et qu’il n’existe aucun certificat dans le magasin de l' \_ utilisateur actuel avec une clé privée disponible avec la fonction de signature de code, la méthode échoue.

Cette méthode utilise l’algorithme de hachage SHA-1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
