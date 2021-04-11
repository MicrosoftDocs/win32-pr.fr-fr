---
title: TLSKeyPackEnumBegin fonction)
description: Commence l’énumération par le biais de tous les jeux de clés installés sur un serveur de licences Bureau à distance en fonction des critères de recherche.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSKeyPackEnumBegin
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f61197e3c08f5608be954a9288ea54cad5586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317478"
---
# <a name="tlskeypackenumbegin-function"></a>TLSKeyPackEnumBegin fonction)

Commence l’énumération par le biais de tous les jeux de clés installés sur un serveur de licences Bureau à distance en fonction des critères de recherche.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hHandle* \[ dans\]
</dt> <dd>

Handle vers un serveur de licences Bureau à distance. Spécifiez un descripteur ouvert par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*dwSearchParm* \[ dans\]
</dt> <dd>

Spécifie les critères de recherche. Ce paramètre est réservé pour une utilisation ultérieure et doit contenir 0xFFFFFFFF.

</dd> <dt>

*bMatchAll* \[ dans\]
</dt> <dd>

Spécifie si toutes les valeurs de recherche doivent être mises en correspondance.

</dd> <dt>

*lpSearchParm* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**LSKeyPack**](lskeypack.md) qui spécifie les paramètres de recherche à rechercher.

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

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ \_ \_ Erreur interne E** (5001)


</dt> <dd>

Erreur interne dans le serveur de licences.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ \_ \_ Séquence E non valide** (5006)


</dt> <dd>

La séquence d’appel n’était pas valide. Probablement, une énumération précédente ne s’est pas terminée.

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

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**Lserver \_ E \_ \_ données non valides** (5009)


</dt> <dd>

Les données du paramètre de recherche ne sont pas valides.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

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

## <a name="requirements"></a>Configuration requise



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

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

