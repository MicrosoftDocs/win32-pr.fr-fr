---
description: La fonction RKeyOpenKeyService n’est pas prise en charge.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: RKeyOpenKeyService, fonction (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529190"
---
# <a name="rkeyopenkeyservice-function"></a>RKeyOpenKeyService fonction)

La fonction **RKeyOpenKeyService** n’est pas prise en charge.

**Windows Server 2003 :** La fonction **RKeyOpenKeyService** établit une connexion à un ordinateur distant et ouvre un handle de service de clé. Le descripteur de service de clé peut ensuite être utilisé par la fonction [**RKeyPFXInstall**](rkeypfxinstall.md) . Notez que ce comportement a changé avec Windows Server 2003 avec Service Pack 1 (SP1).

## <a name="syntax"></a>Syntaxe


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszMachineName* \[ dans\]
</dt> <dd>

Pointeur long vers une chaîne terminée par le caractère null qui représente l’ordinateur sur lequel le handle de service de clé doit être ouvert.

</dd> <dt>

*OwnerType* \[ dans\]
</dt> <dd>

[**KEYSVC \_**](keysvc-type.md) Valeur de type qui représente le type de clé. La seule valeur prise en charge est **KeySvcMachine**.

</dd> <dt>

*pwszOwnerName* \[ dans\]
</dt> <dd>

Réservé. Définissez cette valeur sur **null**.

</dd> <dt>

*pAuthentication* \[ dans\]
</dt> <dd>

Pointeur vers un **void** qui représente les paramètres d’authentification. Ce pointeur peut pointer vers une valeur égale à zéro ou la valeur suivante.



| Valeur                                                                                                                                                                                                                                                           | Signification                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <dt>**RKEYSVC \_ CONNEXION \_ sécurisée \_ uniquement**</dt><dt></dt> </dl> | Le client nécessite une authentification mutuelle. Si cette valeur est spécifiée, le recours à NTLM échouera.<br/> |



 

</dd> <dt>

*conservé* \[ in, out\]
</dt> <dd>

Réservé. Définissez cette valeur sur **null**.

</dd> <dt>

*phKeySvcCli* \[ à\]
</dt> <dd>

Pointeur vers un [**\_ handle KEYSVCC**](keysvcc-handle.md) qui reçoit le handle de service de clé ouvert. Lorsque vous avez fini d’utiliser le descripteur, libérez la ressource en appelant la fonction [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est S \_ OK.

Si la fonction échoue, la valeur de retour est un **ULong** qui indique l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




