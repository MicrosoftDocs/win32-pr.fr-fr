---
description: Supprime un objet de certificat unique de la collection.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'ICertificates2 :: Remove, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237719"
---
# <a name="icertificates2remove-method"></a>ICertificates2 :: Remove, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Remove** supprime un objet [**certificat**](certificate.md) unique de la collection. Cette méthode a été introduite dans CAPICOM 2,0.

## <a name="syntax"></a>Syntaxe


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* \[ dans\]
</dt> <dd>

Valeur d’index de l’objet de [**certificat**](certificate.md) à supprimer. Ce paramètre peut être l’un des types suivants.



| Type                                                                                                                                                                                                                                                              | Signification                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> * * * * <dt>Long * *</dt> * *<dt></dt> </dl>                                                | L’objet de [**certificat**](certificate.md) à l’index spécifié dans la collection est supprimé.<br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> * * * * <dt>Chaîne *</dt> * * * *<dt></dt> </dl>                                        | Le premier objet de [**certificat**](certificate.md) de la collection qui correspond à l’empreinte [*SHA-1*](../secgloss/s-gly.md) contenue dans la chaîne spécifiée est supprimé.<br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <dt>**[**Certificat**](certificate.md)**</dt><dt></dt> </dl> | Le premier objet de [**certificat**](certificate.md) de la collection qui correspond à l’objet de **certificat** spécifié est supprimé.<br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
