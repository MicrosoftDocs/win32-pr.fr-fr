---
description: Vérifie l’existence de tous les abonnés temporaires dans le magasin de données. En appelant cette méthode, vous pouvez vous assurer que tous les abonnés temporaires répertoriés dans le magasin de données sont actifs.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'IEventSystem2 :: VerifyTransientSubscribers, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950568"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a>IEventSystem2 :: VerifyTransientSubscribers, méthode

Vérifie l’existence de tous les abonnés temporaires dans le magasin de données. En appelant cette méthode, vous pouvez vous assurer que tous les abonnés temporaires répertoriés dans le magasin de données sont actifs.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




