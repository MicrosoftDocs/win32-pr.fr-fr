---
title: InternetGetProxyInfo, fonction
description: Récupère les données du proxy pour accéder aux ressources spécifiées.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- InternetGetProxyInfo fonction WinINet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76965f63afb751e810daa6feffe76774f03daaaf7278996b4c6800f0efa42dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113683"
---
# <a name="internetgetproxyinfo-function"></a>InternetGetProxyInfo, fonction

> [!NOTE]
> Cette fonction est déconseillée. Pour la prise en charge d’AutoProxy, utilisez les services HTTP (WinHTTP) version 5,1 à la place. Pour plus d’informations, consultez [prise en charge d’AutoProxy WinHTTP](../winhttp/winhttp-autoproxy-support.md).

Récupère les données du proxy pour accéder aux ressources spécifiées. Cette fonction ne peut être appelée qu’en établissant une liaison dynamique à « JSProxy.dll ».

## <a name="syntax"></a>Syntaxe

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszUrl* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’URL de la ressource HTTP cible.

</dd> <dt>

*dwUrlLength* \[ dans\]
</dt> <dd>

Taille, en octets, de l’URL vers laquelle pointe *lpszUrl*.

</dd> <dt>

*lpszUrlHostName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’hôte de l’URL cible.

</dd> <dt>

*dwUrlHostNameLength* \[ dans\]
</dt> <dd>

Taille, en octets, du nom d’hôte pointé par *lpszUrlHostName*.

</dd> <dt>

*lplpszProxyHostName* \[ à\]
</dt> <dd>

Pointeur vers l’adresse d’une mémoire tampon qui reçoit l’URL du proxy à utiliser dans une requête HTTP pour la ressource spécifiée. L’application est chargée de libérer cette chaîne.

</dd> <dt>

*lpdwProxyHostNameLength* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille, en octets, de la chaîne retournée dans la mémoire tampon *lplpszProxyHostName* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire. Pour recevoir les données d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Pour appeler **InternetGetProxyInfo**, vous devez le lier de manière dynamique à l’aide du type de pointeur fonction défini **pfnInternetGetProxyInfo**. L’extrait de code ci-dessous montre comment déclarer une instance de ce type de pointeur fonction, puis l’initialiser et l’appeler.

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

Comme tous les autres aspects de l’API WinINet, cette fonction ne peut pas être appelée en toute sécurité à partir de DllMain ou des constructeurs et des destructeurs d’objets globaux.

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>JSProxy.dll</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[**InternetInitializeAutoProxyDll**](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))

[**DetectAutoProxyUrl**](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
