---
description: Convertit le temps universel coordonné (heure de Greenwich) en heure locale de l’ordinateur.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Méthode Utilities. UTCTimeToLocalTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545321"
---
# <a name="utilitiesutctimetolocaltime-method"></a>Méthode Utilities. UTCTimeToLocalTime

\[La méthode **UTCTimeToLocalTime** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.\]

La méthode **UTCTimeToLocalTime** convertit le temps universel coordonné (heure de Greenwich) en heure locale de l’ordinateur.

## <a name="syntax"></a>Syntaxe


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UTCTime* \[ dans\]
</dt> <dd>

Temps universel coordonné à convertir en heure locale de l’ordinateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Heure locale qui correspond au temps universel coordonné spécifié.

## <a name="remarks"></a>Notes

Alors que le système utilise le temps universel coordonné en interne, les applications affichent généralement l’heure locale, qui correspond à la date et à l’heure du fuseau horaire local de l’ordinateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Services**](utilities.md)
</dt> </dl>

 

 




