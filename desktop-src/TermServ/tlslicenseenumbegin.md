---
title: TLSLicenseEnumBegin fonction)
description: Commence l’énumération des licences émises par le serveur de licences Bureau à distance en fonction des critères de recherche.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSLicenseEnumBegin
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743605"
---
# <a name="tlslicenseenumbegin-function"></a>TLSLicenseEnumBegin fonction)

Commence l’énumération des licences émises par le serveur de licences Bureau à distance en fonction des critères de recherche.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
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

Spécifie les critères de recherche. Le paramètre peut être une ou une combinaison des valeurs qui sont décrites dans la liste suivante. Le paramètre spécifie le type de jeu de clés et le Pack de clés à rechercher.

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ Rechercher \_ LICENSEID** (0x00000001)


</dt> <dd>

Recherchez par ID de licence.

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ Rechercher \_ KEYPACKID** (0x00000002)


</dt> <dd>

Rechercher par ID de jeu de clés.

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ Rechercher \_ MachineName** (0x00000008)


</dt> <dd>

Rechercher par nom d’ordinateur.

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ \_Nom d’utilisateur de recherche** (0x00000010)


</dt> <dd>

Rechercher par nom d’utilisateur.

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ \_Publication** de la recherche (0x00000080)


</dt> <dd>

Rechercher par date d’émission.

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ \_Expiration** de la recherche (0x00000100)


</dt> <dd>

Rechercher par date d’expiration.

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ Rechercher \_ NUMLICENSES** (0x00000200)


</dt> <dd>

Recherche par nombre de licences.

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ \_ \_ État** de l’entrée de recherche (0x20000000)


</dt> <dd>

Rechercher par État de l’entrée.

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ Exsearch \_ LICENSESTATUS** (0x00100000)


</dt> <dd>

Rechercher par État de licence.

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ Rechercher \_ tout** (0xFFFFFFFF)


</dt> <dd>

Recherchez toutes les licences.

</dd> </dl> </dd> <dt>

*bMatchAll* \[ dans\]
</dt> <dd>

Spécifie si toutes les valeurs de recherche doivent être mises en correspondance.

</dd> <dt>

*lpSearchParm* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**LSLicense**](lslicense.md) qui spécifie les paramètres de recherche à rechercher.

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

[**LSLicense**](lslicense.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

