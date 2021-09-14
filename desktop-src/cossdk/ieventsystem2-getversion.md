---
description: Récupère le numéro de version du système d’événements.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'IEventSystem2 :: GetVersion, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916811"
---
# <a name="ieventsystem2getversion-method"></a>IEventSystem2 :: GetVersion, méthode

Récupère le numéro de version du système d’événements.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pnVersion* \[ à\]
</dt> <dd>

Numéro de version du système d’événements.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




