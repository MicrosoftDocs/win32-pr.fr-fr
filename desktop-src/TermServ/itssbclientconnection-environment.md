---
title: Propriété d’environnement ITsSbClientConnection
description: Récupère un objet qui contient des informations sur l’environnement qui héberge l’ordinateur cible.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété d’environnement
- Services Bureau à distance de propriété d’environnement, interface ITsSbClientConnection
- Services Bureau à distance de l’interface ITsSbClientConnection, propriété d’environnement
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118585"
---
# <a name="itssbclientconnectionenvironment-property"></a>ITsSbClientConnection :: Environment, propriété

Récupère un objet qui contient des informations sur l’environnement qui héberge l’ordinateur cible. Par exemple, dans un scénario de bureau virtuel, cet objet contient des informations sur l’ordinateur qui héberge l’ordinateur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers un pointeur vers un objet d’environnement [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne une valeur **HRESULT** qui indique l’erreur. Les valeurs possibles incluent, mais ne sont pas limitées à, celles figurant dans la liste suivante.

<dl> <dt>

\_pointeur E
</dt> <dd>

L’environnement est introuvable.

</dd> </dl>

## <a name="remarks"></a>Notes

Un plug-in d’orchestration peut appeler cette méthode pour récupérer des informations d’environnement sur une machine virtuelle cible.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                       |
| MIDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





