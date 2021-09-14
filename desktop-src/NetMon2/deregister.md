---
description: La fonction d’exportation de désinscription libère les ressources utilisées pour créer la base de données de propriétés de protocole. La DLL de l’analyseur doit implémenter l’annulation de l’inscription.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Annuler l’inscription de la fonction de rappel (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229704"
---
# <a name="deregister-callback-function"></a>Annuler l’inscription de la fonction de rappel

La fonction d’exportation de **désinscription** libère les ressources utilisées pour créer la [*base de données de propriétés de*](p.md)protocole. La DLL de l’analyseur doit implémenter l’annulation de l' **inscription**.

## <a name="syntax"></a>Syntaxe


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProtocol* \[ dans\]
</dt> <dd>

Handle du protocole pour une base de données spécifique.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Aucun.

## <a name="remarks"></a>Notes

Moniteur réseau appelle la **désinscription** après avoir transmis toutes les informations de capture à la dll de l’analyseur. La DLL de l’analyseur doit implémenter une fonction de **désinscription** pour chaque protocole pris en charge par l’analyseur.

Lors de l’implémentation de l’annulation de l' **inscription**, la dll de l’analyseur doit appeler la fonction [DestroyPropertyDatabase](destroypropertydatabase.md) pour libérer les ressources [*de la base de données de propriétés*](p.md) .



| Pour plus d’informations sur                                        | Consultez                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau. | [Analyseurs](parsers.md)                                 |
| Les points d’entrée inclus dans la DLL de l’analyseur.        | [Architecture des DLL de l’analyseur](parser-dll-architecture.md) |
| La procédure d’implémentation de l’annulation de l' **inscription**  comprend un exemple.     | [Implémentation de l’annulation de l’inscription](implementing-deregister.md) |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DestroyPropertyDatabase](destroypropertydatabase.md)
</dt> </dl>

 

 




