---
description: Réinitialise le contexte de sécurité actuel de la carte à puce.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: 'ISCardVerify :: ResetSecurityState, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6cf1d27298e5bc37288b209547e82f29cfba1393dc3c654563977fbd3f0bf0ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141062"
---
# <a name="iscardverifyresetsecuritystate-method"></a>ISCardVerify :: ResetSecurityState, méthode

\[La méthode **ResetSecurityState** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **ResetSecurityState** réinitialise le contexte de [*sécurité*](../secgloss/s-gly.md) actuel de la [*carte à puce*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Remarques

Pour réactiver le [*contexte de sécurité*](../secgloss/s-gly.md) sans réinitialiser, appelez [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardVerify**](iscardverify.md).

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

[**ISCardVerify**](iscardverify.md)
</dt> <dt>

[**Verrouillage**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))
</dt> </dl>

 

 
