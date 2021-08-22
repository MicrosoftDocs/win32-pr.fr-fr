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
ms.openlocfilehash: c1ad7236564fff2f9a3814beda9bedacbf96fbc9ca2678546304ee108891bea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005147"
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

## <a name="remarks"></a>Remarques

Alors que le système utilise le temps universel coordonné en interne, les applications affichent généralement l’heure locale, qui correspond à la date et à l’heure du fuseau horaire local de l’ordinateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Outils**](utilities.md)
</dt> </dl>

 

 




