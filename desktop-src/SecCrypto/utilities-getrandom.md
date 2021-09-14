---
description: Génère un nombre aléatoire sécurisé à l’aide du fournisseur de services de chiffrement (CSP) par défaut.
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Méthode Utilities. GetRandom
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127417635"
---
# <a name="utilitiesgetrandom-method"></a>Méthode Utilities. GetRandom

\[La méthode **GetRandom** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.\]

La méthode **GetRandom** génère un nombre aléatoire sécurisé à l’aide du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) par défaut.

## <a name="syntax"></a>Syntaxe


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Longueur* \[ dans, facultatif\]
</dt> <dd>

Longueur, en octets, du nombre aléatoire à créer. La valeur par défaut est de 8 octets.

</dd> <dt>

*EncodingType* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui indique le type d’encodage à utiliser pour le nombre aléatoire généré. La valeur par défaut est l' \_ encodage d’un \_ binaire CAPICOM. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                  | Signification                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**\_coder \_ tout**</dt> </dl>          | Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu. Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place. Introduit dans CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_Encode \_ Base64**</dt> </dl> | Les données sont enregistrées sous la forme d’une chaîne encodée en base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt> </dl> | Les données sont enregistrées sous la forme d’une séquence binaire pure.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Nombre d’octets de *longueur* numérique généré de manière aléatoire, avec l’encodage spécifié.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Eau, gaz et électricité**](utilities.md)
</dt> </dl>

 

 
