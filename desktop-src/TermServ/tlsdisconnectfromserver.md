---
title: TLSDisconnectFromServer fonction)
description: Ferme un handle ouvert sur un serveur de licences Bureau à distance.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSDisconnectFromServer
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95911536eda4bd87e45fd034626cf83d88f4d9fc768e4837316ee93abfe3c3d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869409"
---
# <a name="tlsdisconnectfromserver-function"></a>TLSDisconnectFromServer fonction)

Ferme un handle ouvert sur un serveur de licences Bureau à distance.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hHandle* \[ dans\]
</dt> <dd>

Handle vers un serveur de licences Bureau à distance qui est ouvert par un appel à la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Appelez la fonction **TLSDisconnectFromServer** dans le cadre de la routine de nettoyage de votre programme pour fermer tous les descripteurs de serveur ouverts par les appels à la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

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

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

