---
title: TLSKeyPackEnumNext fonction)
description: Continue à partir d’un appel précédent à la fonction TLSKeyPackEnumBegin et retourne le prochain Pack de clés installé sur un serveur de licences Bureau à distance qui correspond aux critères de recherche.
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSKeyPackEnumNext
topic_type:
- apiref
api_name:
- TLSKeyPackEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897874f333ed7933ea1616f7f5ba5f1686736d0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217428"
---
# <a name="tlskeypackenumnext-function"></a>TLSKeyPackEnumNext fonction)

Continue à partir d’un appel précédent à la fonction [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) et retourne le prochain Pack de clés installé sur un serveur de licences bureau à distance qui correspond aux critères de recherche.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hHandle* \[ dans\]
</dt> <dd>

Handle vers un serveur de licences Bureau à distance. Spécifiez un descripteur ouvert par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*lpKeyPack* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**LSKeyPack**](lskeypack.md) qui reçoit le prochain Pack de clés qui correspond aux critères de recherche.

</dd> <dt>

*pdwErrCode* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit l’un des codes d’erreur suivants au retour.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ \_Réussite S** (0)


</dt> <dd>

L’appel a réussi.

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**Lserver \_ Je \_ n’ai \_ plus de \_ données** (4001)


</dt> <dd>

Aucun autre pack de clés ne correspond aux critères de recherche.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ \_ \_ Erreur interne E** (5001)


</dt> <dd>

Erreur interne dans le serveur de licences.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ \_ \_ Séquence E non valide** (5006)


</dt> <dd>

La séquence d’appel n’était pas valide. Vous devez appeler la fonction [**TLSKeyPackEnumBegin ()**](tlskeypackenumbegin.md) avant cela.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Lserver \_ E \_ serveur \_ occupé** (5007)


</dt> <dd>

Le serveur de licences est trop occupé pour traiter la demande.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Lserver \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

Impossible de traiter la requête en raison d’une mémoire insuffisante.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette fonction retourne les valeurs de retour possibles suivantes.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

L’appel a réussi. Vérifiez la valeur du paramètre *pdwErrCode* pour obtenir le code de retour de l’appel.

</dd> <dt>

**\_argument RPC \_ non valide \_**
</dt> <dd>

L’argument n’est pas valide.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

