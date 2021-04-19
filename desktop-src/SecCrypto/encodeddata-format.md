---
description: Retourne une représentation sous forme de chaîne des données encodées.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: EncodedData. format, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523441"
---
# <a name="encodeddataformat-method"></a>EncodedData. format, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **format** retourne une représentation sous forme de chaîne des données encodées.

## <a name="syntax"></a>Syntaxe


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bMultiLines* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si la chaîne retournée contient plusieurs lignes. Si la **valeur est true**, la chaîne retournée peut contenir plusieurs lignes séparées par **vbCrLf**. La valeur par défaut est **False**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Chaîne explicite qui représente les données encodées. Si CAPICOM ne comprend pas les données encodées, une représentation hexadécimale des données est retournée.

## <a name="remarks"></a>Notes

Le format de la chaîne retournée peut changer entre les différentes versions de CAPICOM. Ne vous fiez pas à un format particulier dans votre application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EncodedData**](encodeddata.md)
</dt> </dl>

 

 
