---
description: Libère l’utilisation exclusive de la carte à puce connectée.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'ISCardManage :: SCardUnlock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1c100d1607cceea95264e9af24ba29b23824dee833c14e492cfb0a1dd7ad396f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013889"
---
# <a name="iscardmanagescardunlock-method"></a>ISCardManage :: SCardUnlock, méthode

\[La méthode **SCardUnlock** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **SCardUnlock** libère l’utilisation exclusive de la [*carte à puce*](../secgloss/s-gly.md)connectée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Disposition* \[ dans\]
</dt> <dd>

État dans lequel la carte à puce doit être laissée lorsque le verrou est libéré.

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

**CONGÉ**
</dt><span id="RESET"></span><span id="reset"></span><dt>

**RESET**
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

**Hors tension**
</dt><span id="EJECT"></span><span id="eject"></span><dt>

**ÉMISSION**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                  | Description                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération exécutée avec succès.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *disposition* n’est pas valide.<br/> |



 

## <a name="remarks"></a>Remarques

Pour verrouiller la carte à puce connectée, appelez [**SCardLock**](iscardmanage-scardlock.md).

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**SCardLock**](iscardmanage-scardlock.md)
</dt> </dl>

 

 
