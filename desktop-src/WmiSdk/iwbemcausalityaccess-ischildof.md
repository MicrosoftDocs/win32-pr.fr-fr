---
description: La méthode IsChildOf détermine si une demande est un enfant d’une demande spécifiée (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess :: IsChildOf, méthode (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203957"
---
# <a name="iwbemcausalityaccessischildof-method"></a>IWbemCausalityAccess :: IsChildOf, méthode

La méthode **IsChildOf** détermine si une demande est un enfant d’une demande spécifiée (PID). Une requête parent peut avoir plusieurs demandes enfants. Chaque requête est identifiée par un identificateur global unique (GUID) et peut avoir une requête parente ou peut être une requête principale. Un GUID est un nombre 128 bits unique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PID* \[ dans\]
</dt> <dd>

Valeur GUID qui identifie de façon unique une demande. Par exemple, 5b2fc63a-8AF4-44cb-960C-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur Successful si la requête spécifiée est un enfant de la demande appelant la méthode **IsChildOf** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWbemCausalityAccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




