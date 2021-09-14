---
description: La fonction DestroyPropertyDatabase libère les ressources utilisées pour créer la base de données de propriétés de protocole.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: DestroyPropertyDatabase, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229679"
---
# <a name="destroypropertydatabase-function"></a>DestroyPropertyDatabase fonction)

La fonction **DestroyPropertyDatabase** libère les ressources utilisées pour créer la [*base de données de propriétés de*](p.md)protocole.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProtocol* \[ dans\]
</dt> <dd>

Handle de la base de données de propriétés à détruire. Le descripteur est passé à la DLL de l’analyseur quand Moniteur réseau appelle la fonction de [désinscription](deregister.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est un code d’erreur.



| Code de retour                                                                                              | Description                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_erreur interne \_ NMERR**</dt> </dl>    | Une erreur interne s’est produite. <br/>    |
| <dl> <dt>**NMERR \_ non valide \_ HPROTOCOL**</dt> </dl> | Handle non valide dans *hProtocol*. <br/> |



 

## <a name="remarks"></a>Notes

La fonction **DestroyPropertyDatabase** doit être appelée uniquement lors de l’implémentation de la fonction d’exportation de [désinscription](deregister.md) pour le protocole. Pour les dll de l’analyseur qui prennent en charge plusieurs protocoles, la fonction **DestroyPropertyDatabase** est appelée pour chaque implémentation de l’annulation de l' **inscription**.



| Pour plus d’informations sur                                        | Consultez                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau. | [Analyseurs](parsers.md)                                 |
| Les points d’entrée inclus dans la DLL de l’analyseur.        | [Architecture des DLL de l’analyseur](parser-dll-architecture.md) |
| La procédure d’implémentation de l’annulation de l' **inscription**  comprend un exemple.     | [Implémentation de l’annulation de l’inscription](implementing-deregister.md) |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Désinscrire](deregister.md)
</dt> </dl>

 

 




