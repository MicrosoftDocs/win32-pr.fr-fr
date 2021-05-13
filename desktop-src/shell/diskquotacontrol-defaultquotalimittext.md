---
description: Obtient la limite de quota par défaut sous la forme d’une chaîne de texte.
title: DiskQuotaControl. DefaultQuotaLimitText, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 14a5b5a0cc42bda17f922020a8485430797875e1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841540"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a>DiskQuotaControl. DefaultQuotaLimitText, propriété

Obtient la limite de quota par défaut sous la forme d’une chaîne de texte.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de chaîne qui contient la limite de quota par défaut pour les nouveaux utilisateurs du volume. Par exemple, si le quota par défaut est de 10,5 Mo, la valeur de la propriété est « 10,5 Mo ». Si le volume n’a pas de quota par défaut, la propriété a la valeur « aucune limite » ou l’équivalent localisé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




