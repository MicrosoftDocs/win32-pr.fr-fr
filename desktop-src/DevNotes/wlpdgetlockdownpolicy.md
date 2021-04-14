---
description: Appelle la bibliothèque pour récupérer l’état de sécurité relatif à l’hôte, et script ou MSI à utiliser.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: WldpGetLockdownPolicy, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523463"
---
# <a name="wldpgetlockdownpolicy-function"></a>WldpGetLockdownPolicy fonction)

Appelle la bibliothèque pour récupérer l’état de sécurité relatif à l’hôte, et script ou MSI à utiliser. La fonction n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions LoadLibrary et GetProcAddress pour établir une liaison dynamique à wldp.dll.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hostInformation* \[ dans, facultatif\]
</dt> <dd>

Structure [**d' \_ \_ informations de l’hôte WLDP**](wldp-host-information.md) identifiant l’hôte et le fichier source à évaluer.

</dd> <dt>

*lockdownState* \[ à\]
</dt> <dd>

Fournit la valeur sécurisée de la stratégie obtenue. Que! WLDP_LOCKDOWN_IS_OFF, UMCI est activé. Vous pouvez également vérifier WLDP_LOCKDOWN_IS_AUDIT et WLDP_LOCKDOWN_IS_ENFORCE pour déterminer si une stratégie est en mode d’audit ou d’application.
</dd> <dt>

*lockdownFlags* \[ dans\]
</dt> <dd>

Les valeurs d’indicateur suivantes sont définies WLDP \_ Flags \_ SKIPSIGNATUREVALIDATION 0x00000100 – When set, ignorent la validation SaferIdentifyLevel, qui ignore si un script est signé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne S \_ OK en cas de réussite ou un code d’échec dans le cas contraire.

## <a name="remarks"></a>Notes

En cas d’appel \_ avec \_ les informations de l’hôte WLDP. SZSOURCE = null, la stratégie générique pour l’hôte est retournée.

En cas d’appel avec les informations de l' \_ hôte WLDP \_ . dwHostId = \_ ID d’hôte WLDP \_ \_ global, \_ informations sur l’hôte WLDP \_ . szSource doit avoir la valeur null et la fonction renverra la stratégie système globale.

Le SKIPSIGNATUREVALIDATION dwFlag WLDP \_ Flags \_ peut être utilisé pour ignorer la validation de SaferIdentifyLevel (), qui ignore si un script est signé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




