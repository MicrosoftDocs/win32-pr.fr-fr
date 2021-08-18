---
title: Structure MPCLEAN_PRECHECK_DATA (MpClient. h)
description: Données de notification transmises à la fonction de rappel de prévérification propre.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPCLEAN_PRECHECK_DATA
- PMPCLEAN_PRECHECK_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc272ed230a67811497f0eebb99624d74369c8c55419fba970f326fba502e8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747925"
---
# <a name="mpclean_precheck_data-structure"></a>\_Structure de données de PRÉVÉRIFICATION MPCLEAN \_

Données de notification transmises à la fonction de rappel de prévérification propre.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**BlockedResourceInfo**
</dt> <dd>

Type : **PMPRESOURCE \_ info**

</dd> <dd>

Informations sur les ressources relatives à la ressource bloquée. Par exemple, lorsque la progression est **MPNOTIFY \_ prévérifier la ressource est \_ \_ bloquée**. Consultez [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> <dt>

**\_informations PMPRESOURCE**
</dt> <dd>

Type : **BlockingResourceInfo**

</dd> <dd>

Informations de ressource sur la ressource qui bloque. Par exemple, lorsque la progression est **MPNOTIFY \_ prévérifier la ressource est \_ \_ bloquée**. Consultez [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations MPRESOURCE**](mpresource-info.md)
</dt> </dl>

 

 





