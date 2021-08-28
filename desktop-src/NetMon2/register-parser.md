---
description: La fonction d’exportation de registre doit être implémentée dans toutes les dll de l’analyseur. L’implémentation d’un registre crée et remplit une base de données de propriétés pour un protocole. Moniteur réseau utilise la base de données pour déterminer les propriétés prises en charge par le protocole.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Enregistrer la fonction de rappel de l’analyseur (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 4c24f719018f155fab26df4673b7dc3be18546675532657cb8fb3a0271763af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128919"
---
# <a name="register-parser-callback-function"></a>Enregistrer la fonction de rappel de l’analyseur

La fonction d’exportation de **Registre** doit être implémentée dans toutes les dll de l’analyseur. L’implémentation d’un **Registre** crée et remplit une [*base de données de propriétés*](p.md) pour un protocole. Moniteur réseau utilise la base de données pour déterminer les propriétés prises en charge par le protocole.

## <a name="syntax"></a>Syntaxe


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProtocol* \[ dans\]
</dt> <dd>

Handle du protocole que Moniteur réseau fournit lors de l’appel de **Register**. Le descripteur *hProtocol* est nécessaire lors de l’appel des fonctions d’assistance d’exportation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Aucun.

## <a name="remarks"></a>Notes

Moniteur réseau démarre l’appel de la fonction **Register** dès qu’une capture est chargée. Moniteur réseau appelle la fonction **Register** pour chaque protocole qu’il peut identifier. La fonction [CreateProtocol](createprotocol.md) passe un pointeur vers la fonction **Register** .

L’implémentation de **Register** comprend des appels aux fonctions suivantes.

-   Un appel aux fonctions [CreatePropertyDatabase](createpropertydatabase.md) et [AddProperty](/previous-versions/bb251873(v=msdn.10)) pour créer une base de données de toutes les propriétés prises en charge par le protocole.
-   Un appel à la fonction [CreateHandoffTable](createhandofftable.md) est requis si le protocole utilise un [*jeu de remise*](h.md).

Si la DLL de l’analyseur contient plusieurs analyseurs et que l’analyseur peut détecter plusieurs protocoles, vous devez implémenter une fonction d' **inscription** pour chaque protocole.



| Pour plus d’informations sur                                        | Consultez                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau. | [Analyseurs](parsers.md)                                 |
| Les points d’entrée inclus dans la DLL de l’analyseur.        | [Architecture des DLL de l’analyseur](parser-dll-architecture.md) |
| La procédure d’implémentation de **Register**  comprend un exemple.       | [Implémentation du Registre](implementing-register.md)     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> <dt>

[CreatePropertyDatabase](createpropertydatabase.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> </dl>

 

