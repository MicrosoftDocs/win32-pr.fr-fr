---
description: La méthode SetExternalT120Address est appelée par une application pour configurer une adresse T. 120 externe pour l’échange de données.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'IH323LineEx :: SetExternalT120Address, méthode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541049"
---
# <a name="ih323lineexsetexternalt120address-method"></a>IH323LineEx :: SetExternalT120Address, méthode

\[**SetExternalT120Address** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **SetExternalT120Address** est appelée par une application pour configurer une adresse T. 120 externe pour l’échange de données. La fonctionnalité T. 120 sera publiée au cours de la négociation H. 245, et l’adresse sera utilisée dans l’accusé de réception du canal logique ouvert afin que l’autre point de terminaison puisse configurer T. 120 sessions avec le service à l’écoute sur cette adresse. Si cette fonction n’est pas appelée, le fournisseur de services H. 323 ne publiera pas la fonctionnalité T. 120.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fEnable* \[ dans\]
</dt> <dd>

**True** pour activer la fonctionnalité T. 120 ; **False** pour désactiver la fonctionnalité T. 120.

</dd> <dt>

*dwIP* \[ dans\]
</dt> <dd>

**Valeur DWORD** contenant l’adresse IP dans l’ordre d’octet de l’hôte du service T. 120 externe.

</dd> <dt>

*wPort* \[ dans\]
</dt> <dd>

**Mot** contenant le port du service T. 120 externe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                          | Description                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




