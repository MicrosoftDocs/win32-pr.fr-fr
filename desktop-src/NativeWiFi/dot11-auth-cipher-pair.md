---
description: Définit une paire d’algorithmes d’authentification et de chiffrement 802,11 qui peuvent être activés en même temps sur la station 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: Structure DOT11_AUTH_CIPHER_PAIR (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011617"
---
# <a name="dot11_auth_cipher_pair-structure"></a>\_Structure de \_ paire de chiffrement d’authentification DOT11 \_

La structure de **\_ \_ \_ paire de chiffrement** d’authentification DOT11 définit une paire d’algorithmes d’authentification et de chiffrement de 802,11 qui peut être activée en même temps sur la station 802,11.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a>Membres

<dl> <dt>

**AuthAlgoId**
</dt> <dd>

Algorithme d’authentification qui utilise un type énuméré d' [**\_ \_ algorithme**](dot11-auth-algorithm.md) d’authentification DOT11.

</dd> <dt>

**CipherAlgoId**
</dt> <dd>

Algorithme de chiffrement qui utilise un type énuméré de l' [**\_ \_ algorithme de chiffrement DOT11**](dot11-cipher-algorithm.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

La \_ structure de \_ paire de chiffrement d’authentification DOT11 \_ définit un algorithme d’authentification et de chiffrement qui peut être activé ensemble pour les connexions réseau BSS (Basic Service Set).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                        |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Wlantypes. h (inclure Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Algorithme d’authentification DOT11 \_**](dot11-auth-algorithm.md)
</dt> <dt>

[**\_Algorithme de chiffrement DOT11 \_**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




