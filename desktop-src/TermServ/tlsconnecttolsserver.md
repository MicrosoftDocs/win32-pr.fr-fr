---
title: TLSConnectToLsServer fonction)
description: Ouvre un handle vers le serveur de licences de Bureau à distance spécifié.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSConnectToLsServer
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbfc3c1e365a97b8199df34c2e55a8362f48b7f6a2a43e524e3c6e937de5cb0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986969"
---
# <a name="tlsconnecttolsserver-function"></a>TLSConnectToLsServer fonction)

Ouvre un handle vers le serveur de licences de Bureau à distance spécifié.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszLsServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère **null** qui spécifie le nom NetBIOS du serveur de licences bureau à distance. Si la valeur de ce paramètre est **null**, le serveur spécifié est l’ordinateur local.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est un handle vers le serveur spécifié.

Si la fonction échoue, la valeur de retour est **null**. Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Remarques

Lorsque vous avez terminé d’utiliser le handle retourné par la fonction **TLSConnectToLsServer** , libérez-le en appelant la fonction [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_handle TLS**](tls-handle.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

