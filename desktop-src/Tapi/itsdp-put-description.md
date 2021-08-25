---
description: La \_ méthode put Description définit la description de la session.
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: ITSdp ::p ut_Description, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe47e55b41de2c656f04872846c8be9352c53a0f6265a27e0eefbb1ceb1d5d7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873689"
---
# <a name="itsdpput_description-method"></a>ITSdp ::p ut ( \_ méthode de Description)

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **put \_ Description** définit la description de la session.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDescription* \[ dans\]
</dt> <dd>

Pointeur vers un **BSTR** contenant la description de session.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pDescription* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Remarques

L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PDescription* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.

Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données. Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp :: obtient la \_ Description**](itsdp-get-description.md)
</dt> </dl>

 

