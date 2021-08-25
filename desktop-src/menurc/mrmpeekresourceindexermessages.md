---
title: MrmPeekResourceIndexerMessages, fonction (MrmResourceIndexer. h)
description: Affichez tous les messages générés par un indexeur de ressource. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 87D093AE-7444-4778-8B9E-1D0D972C90E1
keywords:
- Menus de fonction MrmPeekResourceIndexerMessages et autres ressources
topic_type:
- apiref
api_name:
- MrmPeekResourceIndexerMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f72325ab147656873af2bbf13d7ce1cfa47802c816dc9f14f0c6ee4f3c821683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847329"
---
# <a name="mrmpeekresourceindexermessages-function"></a>MrmPeekResourceIndexerMessages fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Affichez tous les messages générés par un indexeur de ressource. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmPeekResourceIndexerMessages(
  _In_  MrmResourceIndexerHandle  indexer,
  _Out_ MrmResourceIndexerMessage **messages,
  _Out_ ULONG                     *numMsgs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indexeur* \[ dans\]
</dt> <dd>

Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle identifiant l’indexeur de ressource auquel vous souhaitez afficher les messages.

</dd> <dt>

*messages* \[ à\]
</dt> <dd>

Type : **[ **MrmResourceIndexerMessage**](mrmresourceindexermessage.md)\*\***

Pointeur vers un pointeur vers un [**MrmResourceIndexerMessage**](mrmresourceindexermessage.md). La fonction alloue un tableau de **MrmResourceIndexerMessage** et retourne un pointeur vers cette mémoire dans *les messages*. Ne libérez pas le pointeur dont vous transmettez l’adresse aux *messages*.

</dd> <dt>

*numMsgs* \[ à\]
</dt> <dd>

Type : **ULong \***

Nombre de messages renvoyés dans les *messages*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="remarks"></a>Remarques

Votre application ne possède pas la mémoire allouée et retournée dans les *messages*. vous ne devez donc pas la libérer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1803 \[ uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows \[Applications de bureau serveur uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

