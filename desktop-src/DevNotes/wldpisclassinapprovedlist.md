---
description: Appelle la bibliothèque pour valider si un CLSID particulier peut être appelé en toute sécurité.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: WldpIsClassInApprovedList, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: ef4f6a719a1fe5146badbe59239dc16f9031f553ee8bba189c838dddcb641d8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642039"
---
# <a name="wldpisclassinapprovedlist-function"></a>WldpIsClassInApprovedList fonction)

Appelle la bibliothèque pour valider si un **CLSID** particulier peut être appelé en toute sécurité. La fonction n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions LoadLibrary et GetProcAddress pour établir une liaison dynamique à wldp.dll.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*classID* 
</dt> <dd>

ID de classe COM pour lequel vérifier l’approbation.

</dd> <dt>

*hostInformation* \[ dans\]
</dt> <dd>

Structure [**d' \_ \_ informations de l’hôte WLDP**](wldp-host-information.md) identifiant l’hôte à évaluer.

</dd> <dt>

*IsApproved* \[ à\]
</dt> <dd>

En cas de réussite de l’opération, contient la **valeur true** si l’ID de classe est approuvé ; Sinon, **false**.

</dd> <dt>

*optionalFlags* 
</dt> <dd>

Ce paramètre est réservé et doit avoir la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




