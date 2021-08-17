---
title: Propriété de serveur DevicePair (Asptlb. h)
description: Obtient le serveur pour la paire d’appareils active de base.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- API de diffusion multimédia en continu des propriétés de serveur
- API de diffusion multimédia en continu des propriétés de serveur, interface DevicePair
- API de diffusion multimédia en continu de l’interface DevicePair, propriété de serveur
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0939a27d96de8f2c8ff53ffd7b0bd766292b873450fb138d0877e916c691f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100723"
---
# <a name="devicepairserver-property"></a>DevicePair :: Server, propriété

Obtient le serveur pour la paire d’appareils active de base.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Reçoit un objet [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) qui représente le périphérique serveur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Asptlb. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

