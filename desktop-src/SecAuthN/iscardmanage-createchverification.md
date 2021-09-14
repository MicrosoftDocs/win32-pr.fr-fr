---
description: Crée une interface ISCardVerify.
ms.assetid: 6338e672-83cd-46fe-8f94-f4ba6e2581ea
title: 'ISCardManage :: CreateCHVerification, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCHVerification
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a5909a8782571f9bd01a1c31e5ccd04c3d029df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193895"
---
# <a name="iscardmanagecreatechverification-method"></a>ISCardManage :: CreateCHVerification, méthode

\[La méthode **CreateCHVerification** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **CreateCHVerification** crée une interface [**ISCardVerify**](iscardverify.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateCHVerification(
  [out] ISCardVerify **ppISCardVerify
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppISCardVerify* \[ à\]
</dt> <dd>

Renvoi d’un pointeur vers l’interface [**ISCardVerify**](iscardverify.md) créée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                                   | Description                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *ppISCardVerify* n’est pas valide.<br/>  |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *ppISCardVerify*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                                |



 

## <a name="remarks"></a>Notes

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Spécifications



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

[**ISCardVerify**](iscardverify.md)
</dt> </dl>

 

 
