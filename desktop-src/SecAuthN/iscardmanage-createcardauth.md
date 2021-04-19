---
description: Crée une interface ISCardAuth.
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: 'ISCardManage :: CreateCardAuth, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: d0b81fd8211491527f39999c6873f7b047bcb32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534324"
---
# <a name="iscardmanagecreatecardauth-method"></a>ISCardManage :: CreateCardAuth, méthode

\[La méthode **CreateCardAuth** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **CreateCardAuth** crée une interface [**ISCardAuth**](iscardauth.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppISCardAuth* \[ à\]
</dt> <dd>

Retourne un pointeur vers l’interface créée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                                   | Description                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *ppISCardAuth* n’est pas valide.<br/>  |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *ppISCardAuth*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                              |



 

## <a name="remarks"></a>Notes

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
