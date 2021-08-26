---
description: La \_ méthode d’authentification ICC permet à une application d’authentifier la carte à puce.
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: 'ISCardAuth :: ICC_Auth, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b96d40d6c35250b55b6aa2bb37733492fda874df0346b24c859431d749a3e4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015379"
---
# <a name="iscardauthicc_auth-method"></a>ISCardAuth :: ICC, \_ méthode d’authentification

\[La méthode d' **\_ authentification ICC** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode d' **\_ authentification ICC** permet à une application d’authentifier la carte à puce.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lAlgoID* \[ dans\]
</dt> <dd>

Algorithme à utiliser dans le processus d’authentification.

</dd> <dt>

*pParam* \[ dans\]
</dt> <dd>

Objet [**IByteBuffer**](ibytebuffer.md) contenant les paramètres spécifiques au fournisseur du processus d’authentification.

</dd> <dt>

*pbuffer* \[ in, out\]
</dt> <dd>

En entrée, contient les données à utiliser dans le processus d’authentification.

Lors de la sortie, contient le résultat du processus d’authentification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Remarques

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardAuth**](iscardauth.md).

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

[**ISCardAuth**](iscardauth.md)
</dt> </dl>

 

 
