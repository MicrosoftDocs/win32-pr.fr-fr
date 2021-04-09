---
description: Définit les différents États prêts de l’extension de source de média.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: Énumération MF_MSE_READY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865585"
---
# <a name="mf_mse_ready-enumeration"></a>\_ \_ Énumération compatible MF MSE

Définit les différents États prêts de l’extension de source de média.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF \_ MSE \_ prêt \_ fermé**
</dt> <dd>

La source du média est fermée.

</dd> <dt>

<span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**\_ouverture de MSE MF \_ \_ ouverte**
</dt> <dd>

La source du média est ouverte.

</dd> <dt>

<span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**fin de la fermeture de \_ MSE MF \_ \_**
</dt> <dd>

La source du média est terminée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




