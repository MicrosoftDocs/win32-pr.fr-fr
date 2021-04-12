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
ms.openlocfilehash: ef441754fd5de09e3792d9269f05d96ecc08aa23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384688"
---
# <a name="internetgetproxyinfo-function"></a><span data-ttu-id="8e542-104">InternetGetProxyInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="8e542-104">InternetGetProxyInfo function</span></span>

> [!NOTE]
> <span data-ttu-id="8e542-105">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8e542-105">This function is deprecated.</span></span> <span data-ttu-id="8e542-106">Pour la prise en charge d’AutoProxy, utilisez les services HTTP (WinHTTP) version 5,1 à la place.</span><span class="sxs-lookup"><span data-stu-id="8e542-106">For autoproxy support, use HTTP Services (WinHTTP) version 5.1 instead.</span></span> <span data-ttu-id="8e542-107">Pour plus d’informations, consultez [prise en charge d’AutoProxy WinHTTP](../winhttp/winhttp-autoproxy-support.md).</span><span class="sxs-lookup"><span data-stu-id="8e542-107">For more information, see [WinHTTP AutoProxy Support](../winhttp/winhttp-autoproxy-support.md).</span></span>

<span data-ttu-id="8e542-108">Récupère les données du proxy pour accéder aux ressources spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8e542-108">Retrieves proxy data for accessing specified resources.</span></span> <span data-ttu-id="8e542-109">Cette fonction ne peut être appelée qu’en établissant une liaison dynamique à « JSProxy.dll ».</span><span class="sxs-lookup"><span data-stu-id="8e542-109">This function can only be called by dynamically linking to "JSProxy.dll".</span></span>

## <a name="syntax"></a><span data-ttu-id="8e542-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e542-110">Syntax</span></span>

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

## <a name="parameters"></a><span data-ttu-id="8e542-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e542-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e542-112">*lpszUrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e542-112">*lpszUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e542-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’URL de la ressource HTTP cible.</span><span class="sxs-lookup"><span data-stu-id="8e542-113">A pointer to a null-terminated string that specifies the URL of the target HTTP resource.</span></span>

</dd> <dt>

<span data-ttu-id="8e542-114">*dwUrlLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e542-114">*dwUrlLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e542-115">Taille, en octets, de l’URL vers laquelle pointe *lpszUrl*.</span><span class="sxs-lookup"><span data-stu-id="8e542-115">The size, in bytes, of the URL pointed to by *lpszUrl*.</span></span>

</dd> <dt>

<span data-ttu-id="8e542-116">*lpszUrlHostName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e542-116">*lpszUrlHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e542-117">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’hôte de l’URL cible.</span><span class="sxs-lookup"><span data-stu-id="8e542-117">A pointer to a null-terminated string that specifies the host name of the target URL.</span></span>

</dd> <dt>

<span data-ttu-id="8e542-118">*dwUrlHostNameLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e542-118">*dwUrlHostNameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e542-119">Taille, en octets, du nom d’hôte pointé par *lpszUrlHostName*.</span><span class="sxs-lookup"><span data-stu-id="8e542-119">The size, in bytes, of the host name pointed to by *lpszUrlHostName*.</span></span>

</dd> <dt>

<span data-ttu-id="8e542-120">*lplpszProxyHostName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8e542-120">*lplpszProxyHostName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e542-121">Pointeur vers l’adresse d’une mémoire tampon qui reçoit l’URL du proxy à utiliser dans une requête HTTP pour la ressource spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8e542-121">A pointer to the address of a buffer that receives the URL of the proxy to use in an HTTP request for the specified resource.</span></span> <span data-ttu-id="8e542-122">L’application est chargée de libérer cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="8e542-122">The application is responsible for freeing this string.</span></span>

</dd> <dt>

<span data-ttu-id="8e542-123">*lpdwProxyHostNameLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8e542-123">*lpdwProxyHostNameLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e542-124">Pointeur vers une variable qui reçoit la taille, en octets, de la chaîne retournée dans la mémoire tampon *lplpszProxyHostName* .</span><span class="sxs-lookup"><span data-stu-id="8e542-124">A pointer to a variable that receives the size, in bytes, of the string returned in the *lplpszProxyHostName* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e542-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e542-125">Return value</span></span>

<span data-ttu-id="8e542-126">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8e542-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="8e542-127">Pour recevoir les données d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="8e542-127">To get extended error data, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e542-128">Notes</span><span class="sxs-lookup"><span data-stu-id="8e542-128">Remarks</span></span>

<span data-ttu-id="8e542-129">Pour appeler **InternetGetProxyInfo**, vous devez le lier de manière dynamique à l’aide du type de pointeur fonction défini **pfnInternetGetProxyInfo**.</span><span class="sxs-lookup"><span data-stu-id="8e542-129">To call **InternetGetProxyInfo**, you must dynamically link to it using the defined function-pointer type **pfnInternetGetProxyInfo**.</span></span> <span data-ttu-id="8e542-130">L’extrait de code ci-dessous montre comment déclarer une instance de ce type de pointeur fonction, puis l’initialiser et l’appeler.</span><span class="sxs-lookup"><span data-stu-id="8e542-130">The code snippet below shows how to declare an instance of this function-pointer type and then initialize and call it.</span></span>

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

<span data-ttu-id="8e542-131">Comme tous les autres aspects de l’API WinINet, cette fonction ne peut pas être appelée en toute sécurité à partir de DllMain ou des constructeurs et des destructeurs d’objets globaux.</span><span class="sxs-lookup"><span data-stu-id="8e542-131">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="8e542-132">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="8e542-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="8e542-133">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="8e542-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="8e542-134">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="8e542-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e542-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e542-135">Requirements</span></span>

| <span data-ttu-id="8e542-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e542-136">Requirement</span></span> | <span data-ttu-id="8e542-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e542-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e542-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e542-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8e542-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e542-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8e542-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e542-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8e542-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e542-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8e542-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8e542-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e542-143"><dt>JSProxy.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e542-143"><dt>JSProxy.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="8e542-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e542-144">See also</span></span>

[<span data-ttu-id="8e542-145">**InternetInitializeAutoProxyDll**</span><span class="sxs-lookup"><span data-stu-id="8e542-145">**InternetInitializeAutoProxyDll**</span></span>](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

<span data-ttu-id="8e542-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8e542-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span></span>

[<span data-ttu-id="8e542-147">**DetectAutoProxyUrl**</span><span class="sxs-lookup"><span data-stu-id="8e542-147">**DetectAutoProxyUrl**</span></span>](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
