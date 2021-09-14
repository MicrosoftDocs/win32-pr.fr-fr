---
description: Génère une clé de session et chiffre les données et enveloppes.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: EnvelopedData. Encrypt, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416412"
---
# <a name="envelopeddataencrypt-method"></a>EnvelopedData. Encrypt, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **Encrypt** génère une clé de session, utilise cette clé pour chiffrer le contenu, encapsule le contenu chiffré pour chaque destinataire en chiffrant la clé de session avec la clé publique de chaque destinataire, puis retourne l' [*objet BLOB*](../secgloss/b-gly.md) qui contient le contenu chiffré et les clés de session chiffrées sous la forme d’une chaîne encodée.

## <a name="syntax"></a>Syntaxe


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EncodingType* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui indique le type d’encodage utilisé pour encoder les données enveloppées. La valeur d’encodage par défaut est CAPICOM \_ encode \_ Base64. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                  | Signification                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**\_coder \_ tout**</dt> </dl>          | Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu. Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place. Introduit dans CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_Encode \_ Base64**</dt> </dl> | Les données sont enregistrées sous la forme d’une chaîne encodée en base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt> </dl> | Les données sont enregistrées sous la forme d’une séquence binaire pure.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un objet BLOB qui contient les données enveloppées dans une chaîne encodée.

## <a name="remarks"></a>Notes

L’objet BLOB retourné contient le contenu chiffré et une clé de session chiffrée pour chaque destinataire prévu. Ces clés de session sont chiffrées à l’aide de la clé publique de chaque destinataire. Les clés de session chiffrées ne peuvent être déchiffrées qu’avec la clé privée d’un destinataire.

Si la propriété [**Recipients**](envelopeddata-recipients.md) ne contient aucune information, cette méthode recherche les destinataires potentiels dans le magasin de certificats AddressBook de l’utilisateur actuel. Si plusieurs destinataires potentiels sont trouvés, l’utilisateur est invité à sélectionner un destinataire dans une boîte de dialogue de sélection.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
