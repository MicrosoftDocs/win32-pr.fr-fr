---
description: Décode une chaîne de base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Méthode Utilities. Base64Decode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127417643"
---
# <a name="utilitiesbase64decode-method"></a>Méthode Utilities. Base64Decode

\[La méthode **Base64Decode** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.\]

La méthode **Base64Decode** décode une chaîne de base64.

## <a name="syntax"></a>Syntaxe


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EncodedString* \[ dans\]
</dt> <dd>

Chaîne encodée en base64 à décoder.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Chaîne décodée.

## <a name="remarks"></a>Notes

L’encodage Base64 est le schéma utilisé pour transmettre des données binaires. Base64 traite les données en tant que groupes 24 bits, en mappant ces données à quatre caractères encodés. L’encodage Base64 est parfois appelé encodage 3 à 4. Chaque 6 bits du groupe 24 bits est utilisé comme index dans une table de mappage (l’alphabet base64) pour obtenir un caractère pour les données encodées. Les données encodées ont des longueurs de ligne limitées à 76 caractères.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Eau, gaz et électricité**](utilities.md)
</dt> </dl>

 

 




