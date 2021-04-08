---
title: RPC_MGR_EPV (rpcdce. h)
description: Le type de données \_ EPV redirecteur RPC \_ définit un vecteur de point d’entrée de gestionnaire.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740213"
---
# <a name="rpc_mgr_epv"></a>\_EPV du gestionnaire RPC \_

Le type de **données \_ \_ EPV redirecteur RPC** définit un vecteur de point d’entrée de gestionnaire.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Membres

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**If-Name**
</dt> <dd>

Spécifie le nom de l’interface

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**type de retour**
</dt> <dd>

Spécifie le type retourné par la fonction **nomfonction** indiquée dans le fichier IDL.

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**
</dt> <dd>

Spécifie le nom de la fonction indiquée dans le fichier IDL.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**Param-liste**
</dt> <dd>

Spécifie les paramètres indiqués pour la fonction **nomfonction** dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

Le vecteur de point d’entrée du gestionnaire (EPV) est un tableau de pointeurs de fonction. Le tableau contient des pointeurs vers les implémentations des fonctions spécifiées dans le fichier IDL. Le nombre d’éléments dans le tableau est défini sur le nombre de fonctions spécifiées dans le fichier IDL. Une application peut également avoir plusieurs EPVs, représentant plusieurs implémentations des fonctions spécifiées dans l’interface.

Le compilateur MIDL génère un type de données **EPV** par défaut nommé * if-name ***\_ Server \_ EPV**, où *-Name* spécifie l’identificateur d’interface dans le fichier IDL. Le compilateur MIDL Initialise ce **EPV** par défaut pour contenir des pointeurs fonction pour chacune des procédures spécifiées dans le fichier IDL.

Lorsque le serveur offre plusieurs implémentations de la même interface, l’application serveur doit déclarer et initialiser une variable de type *If-name * * * \_ Server \_ EPV** pour chaque implémentation de l’interface. Chaque **EPV** doit contenir un point d’entrée (pointeur de fonction) pour chaque procédure définie dans le fichier IDL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Rpcdce. h (inclure RPC. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





