---
description: Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse sa limite de quota affectée.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: DiskQuotaControl. LogQuotaLimit, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971958"
---
# <a name="diskquotacontrollogquotalimit-property"></a>DiskQuotaControl. LogQuotaLimit, propriété

Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse sa limite de quota affectée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété a la valeur **true** si une entrée du journal des événements système est effectuée lorsque l’utilisateur dépasse sa limite de quota, ou **false** dans le cas contraire.

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

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




