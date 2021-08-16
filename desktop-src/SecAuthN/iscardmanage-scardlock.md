---
description: Verrouille une carte à puce connectée pour une utilisation exclusive.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'ISCardManage :: SCardLock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e610b914f1185eb2a1f4f7becdc8ba12c8aea4823630ecf3c5b9abe0f1ea3f97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013939"
---
# <a name="iscardmanagescardlock-method"></a>ISCardManage :: SCardLock, méthode

\[La méthode **SCardLock** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **SCardLock** verrouille une [*carte à puce*](../secgloss/s-gly.md) connectée pour une utilisation exclusive.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                            | Description                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl> | L’opération n’a pas pu se terminer.<br/>     |



 

## <a name="remarks"></a>Remarques

Pour libérer l’utilisation exclusive de la carte à puce connectée, appelez [**SCardUnlock**](iscardmanage-scardunlock.md).

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

[**SCardUnlock**](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
