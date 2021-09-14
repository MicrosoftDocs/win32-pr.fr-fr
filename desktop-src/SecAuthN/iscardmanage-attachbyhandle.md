---
description: Crée un lien de communication vers une carte à puce (ICC) à l’aide d’un handle retourné par le gestionnaire de ressources de carte à puce.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'ISCardManage :: AttachByHandle, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193907"
---
# <a name="iscardmanageattachbyhandle-method"></a>ISCardManage :: AttachByHandle, méthode

\[La méthode **AttachByHandle** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **AttachByHandle** crée un lien de communication vers une [*carte à puce*](../secgloss/s-gly.md) (ICC) à l’aide d’un handle renvoyé par le gestionnaire de [*ressources*](../secgloss/r-gly.md)de carte à puce.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hICC* \[ dans\]
</dt> <dd>

Handle d’une carte à puce.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                                   | Description                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *hICC* n’est pas valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                     |



 

## <a name="remarks"></a>Notes

Pour joindre un appel de [*lecteur*](../secgloss/r-gly.md) [**AttachByIFD**](iscardmanage-attachbyifd.md).

Pour libérer le [**détachement**](iscardmanage-detach.md)d’un appel de pièce jointe.

Pour vous reconnecter à la carte à puce sans appeler [**Detach**](iscardmanage-detach.md) et **AttachByHandle**, appelez [**reconnect**](iscardmanage-reconnect.md).

Pour obtenir la liste de toutes les méthodes définies par l’interface [**ISCardManage**](iscardmanage.md) , consultez [**ISCardManage**](iscardmanage.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations sur les codes d’erreur de carte à puce, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Detach**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Reconnexion**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
