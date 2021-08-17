---
description: Convertit l’heure locale de l’ordinateur en temps universel coordonné (heure de Greenwich).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Méthode Utilities. LocalTimeToUTCTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 03efb6cdfbea712f2fbca194073b89bcee66975481c1a7c0fdc2d7bd385eb652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971020"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Méthode Utilities. LocalTimeToUTCTime

\[La méthode **LocalTimeToUTCTime** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.\]

La méthode **LocalTimeToUTCTime** convertit l’heure locale de l’ordinateur en temps universel coordonné (heure de Greenwich).

## <a name="syntax"></a>Syntaxe


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Localtime* \[ dans\]
</dt> <dd>

Heure locale à convertir en temps universel coordonné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Temps universel coordonné qui correspond à l’heure locale spécifiée.

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

 

 




