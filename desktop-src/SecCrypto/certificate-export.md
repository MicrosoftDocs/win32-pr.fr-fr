---
description: Copie un certificat dans une chaîne encodée.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'ICertificate2 :: export, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f002be332097baa0ad0947367259d15f0657d276770682b709402e2f0a333290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771766"
---
# <a name="icertificate2export-method"></a>ICertificate2 :: export, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Export** copie un certificat dans une chaîne encodée. La chaîne encodée peut être écrite dans un fichier ou importée dans un nouvel objet de [**certificat**](certificate.md) .

## <a name="syntax"></a>Syntaxe


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EncodingType* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui spécifie le type d’encodage pour l’opération d’exportation. La valeur par défaut est **CAPICOM \_ encode \_ Base64**. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                  | Signification                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**\_coder \_ tout**</dt> </dl>          | Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu. Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place. Introduit dans CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_Encode \_ Base64**</dt> </dl> | Les données sont enregistrées sous la forme d’une chaîne encodée en base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt> </dl> | Les données sont enregistrées sous la forme d’une séquence binaire pure.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Chaîne qui contient le certificat exporté dans le formulaire d’encodage spécifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets de chiffrement](cryptography-objects.md)
</dt> <dt>

[**Certificate**](certificate.md)
</dt> </dl>

 

 
