---
description: Définit la stratégie d’ouverture de session automatique actuelle.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'IWinHttpRequest :: SetAutoLogonPolicy, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526196"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a><span data-ttu-id="92627-103">IWinHttpRequest :: SetAutoLogonPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="92627-103">IWinHttpRequest::SetAutoLogonPolicy method</span></span>

<span data-ttu-id="92627-104">La méthode **SetAutoLogonPolicy** définit la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md)actuelle.</span><span class="sxs-lookup"><span data-stu-id="92627-104">The **SetAutoLogonPolicy** method sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="92627-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92627-105">Syntax</span></span>


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="92627-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92627-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92627-107">*AutoLogonPolicy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92627-107">*AutoLogonPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92627-108">Spécifie la stratégie d’ouverture de session automatique actuelle.</span><span class="sxs-lookup"><span data-stu-id="92627-108">Specifies the current automatic logon policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92627-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92627-109">Return value</span></span>

<span data-ttu-id="92627-110">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="92627-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="92627-111">Notes</span><span class="sxs-lookup"><span data-stu-id="92627-111">Remarks</span></span>

<span data-ttu-id="92627-112">La stratégie par défaut est [**AutoLogonPolicy \_ OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="92627-112">The default policy is [**AutoLogonPolicy\_OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span></span>

<span data-ttu-id="92627-113">Appelez **SetAutoLogonPolicy** pour définir la stratégie d’ouverture de session automatique avant d’appeler [**Send**](iwinhttprequest-send.md) pour envoyer la demande.</span><span class="sxs-lookup"><span data-stu-id="92627-113">Call **SetAutoLogonPolicy** to set the automatic logon policy before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

> [!Note]  
> <span data-ttu-id="92627-114">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="92627-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="92627-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="92627-115">Examples</span></span>

<span data-ttu-id="92627-116">L’exemple de script suivant montre comment définir la stratégie d’ouverture de session automatique pour ne jamais utiliser l’authentification NTLM ou Negotiate automatiquement.</span><span class="sxs-lookup"><span data-stu-id="92627-116">The following scripting example shows how to set the automatic logon policy to never use NTLM or Negotiate authentication automatically.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="92627-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92627-117">Requirements</span></span>



| <span data-ttu-id="92627-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92627-118">Requirement</span></span> | <span data-ttu-id="92627-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="92627-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="92627-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92627-120">Minimum supported client</span></span><br/> | <span data-ttu-id="92627-121">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92627-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="92627-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92627-122">Minimum supported server</span></span><br/> | <span data-ttu-id="92627-123">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92627-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="92627-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="92627-124">Redistributable</span></span><br/>          | <span data-ttu-id="92627-125">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="92627-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="92627-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="92627-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92627-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="92627-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="92627-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="92627-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="92627-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92627-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="92627-130">DLL</span><span class="sxs-lookup"><span data-stu-id="92627-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92627-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92627-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="92627-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92627-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92627-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="92627-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="92627-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="92627-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="92627-135">Authentification dans WinHTTP</span><span class="sxs-lookup"><span data-stu-id="92627-135">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="92627-136">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="92627-136">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




