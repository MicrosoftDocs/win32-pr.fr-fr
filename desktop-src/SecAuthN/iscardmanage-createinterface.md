---
description: Crée l’interface spécifiée.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'ISCardManage :: CreateInterface, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8c9b231ec7930b78c1693e38268638e7a24b26dfa32d8f25acb5a429dbcdedc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922658"
---
# <a name="iscardmanagecreateinterface-method"></a>ISCardManage :: CreateInterface, méthode

\[La méthode **CreateInterface** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **CreateInterface** crée l’interface spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pguidInterface* \[ dans\]
</dt> <dd>

Valeur GUID de l’interface à créer.

</dd> <dt>

*bstrName* \[ dans\]
</dt> <dd>

Nom de l’interface à créer si le GUID n’est pas disponible. Les valeurs standard sont « CryptoProvider ».

</dd> <dt>

*pUserData* \[ dans\]
</dt> <dd>

Pointeur vers des données spécifiques à l’utilisateur à utiliser dans la création d’une interface.

</dd> <dt>

*ppInterface* \[ à\]
</dt> <dd>

Pointeur vers l’interface retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Les valeurs de retour possibles sont les suivantes :



| Code de retour                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | L’un des paramètres fournis n’est pas valide.<br/>                                         |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans le paramètre *pguidInterface* ou *pUserData* .<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                                                                        |



 

## <a name="remarks"></a>Remarques

Pour obtenir la liste de toutes les méthodes définies par l’interface [**ISCardManage**](iscardmanage.md) , consultez **ISCardManage**.

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations sur les codes d’erreur de carte à puce, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

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
</dt> </dl>

 

 
