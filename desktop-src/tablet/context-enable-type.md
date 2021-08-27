---
description: Indique si les messages de contexte doivent être envoyés à la procédure de fenêtre de la fenêtre propriétaire.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: Énumération CONTEXT_ENABLE_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 94bffba211f75416ccae5e9a55342441b7b11b41b1a9f1f4b085ec190f991645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110969"
---
# <a name="context_enable_type-enumeration"></a>\_Énumération des types d’activation de contexte \_

Indique si les messages de contexte doivent être envoyés à la procédure de fenêtre de la fenêtre propriétaire.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**activation du contexte \_**
</dt> <dd>

Le contexte de tablette doit être activé, ce qui entraîne l’envoi de messages de contexte à la procédure de fenêtre de la fenêtre propriétaire.

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**désactiver le contexte \_**
</dt> <dd>

Le contexte de tablette doit être désactivé, ce qui empêche tout autre message de contexte d’être envoyé à la procédure de fenêtre ou au récepteur d’événements de la fenêtre propriétaire.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITablet :: CreateContext, méthode**](itablet-createcontext.md)
</dt> </dl>

 

 




