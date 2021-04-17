---
description: Sélectionne un certificat client à envoyer à un serveur HTTPs (Secure Hypertext Transfer Protocol).
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'IWinHttpRequest :: SetClientCertificate, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319858"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a><span data-ttu-id="658eb-103">IWinHttpRequest :: SetClientCertificate, méthode</span><span class="sxs-lookup"><span data-stu-id="658eb-103">IWinHttpRequest::SetClientCertificate method</span></span>

<span data-ttu-id="658eb-104">La méthode **SetClientCertificate** sélectionne un certificat client à envoyer à un serveur HTTPS (Secure Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="658eb-104">The **SetClientCertificate** method selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="658eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="658eb-105">Syntax</span></span>


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="658eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="658eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="658eb-107">*ClientCertificate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="658eb-107">*ClientCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="658eb-108">Spécifie l’emplacement, le [*magasin de certificats*](glossary.md)et l’objet d’un certificat client.</span><span class="sxs-lookup"><span data-stu-id="658eb-108">Specifies the location, [*certificate store*](glossary.md), and subject of a client certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="658eb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="658eb-109">Return value</span></span>

<span data-ttu-id="658eb-110">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="658eb-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="658eb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="658eb-111">Remarks</span></span>

<span data-ttu-id="658eb-112">La chaîne spécifiée dans le paramètre *ClientCertificate* se compose de l’emplacement du certificat, du magasin de certificats et du nom d’objet délimités par des barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="658eb-112">The string specified in the *ClientCertificate* parameter consists of the certificate location, certificate store, and subject name delimited by backslashes.</span></span> <span data-ttu-id="658eb-113">Pour plus d’informations sur les composants de la chaîne de certificat, consultez [certificats clients](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="658eb-113">For more information about the components of the certificate string, see [Client Certificates](ssl-in-winhttp.md).</span></span>

<span data-ttu-id="658eb-114">Le nom et l’emplacement du magasin de certificats sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="658eb-114">The certificate store name and location are optional.</span></span> <span data-ttu-id="658eb-115">Toutefois, si vous spécifiez un magasin de certificats, vous devez également spécifier l’emplacement de ce magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="658eb-115">However, if you specify a certificate store, you must also specify the location of that certificate store.</span></span> <span data-ttu-id="658eb-116">L’emplacement par défaut est \_ utilisateur actuel et le magasin de certificats par défaut est « My ».</span><span class="sxs-lookup"><span data-stu-id="658eb-116">The default location is CURRENT\_USER and the default certificate store is "MY".</span></span> <span data-ttu-id="658eb-117">Un objet vide indique que le premier certificat du magasin de certificats doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="658eb-117">A blank subject indicates that the first certificate in the certificate store should be used.</span></span>

<span data-ttu-id="658eb-118">Appelez **SetClientCertificate** pour sélectionner un certificat avant d’appeler [**Send**](iwinhttprequest-send.md) pour envoyer la demande.</span><span class="sxs-lookup"><span data-stu-id="658eb-118">Call **SetClientCertificate** to select a certificate before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

<span data-ttu-id="658eb-119">Les services HTTP Microsoft Windows (WinHTTP) ne fournissent pas de certificats clients aux serveurs proxy qui demandent des certificats pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="658eb-119">Microsoft Windows HTTP Services (WinHTTP) does not provide client certificates to proxy servers that request certificates for authentication.</span></span>

> [!Note]  
> <span data-ttu-id="658eb-120">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="658eb-120">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="658eb-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="658eb-121">Examples</span></span>

<span data-ttu-id="658eb-122">L’exemple de script suivant montre comment sélectionner un certificat client à envoyer avec une demande.</span><span class="sxs-lookup"><span data-stu-id="658eb-122">The following scripting example shows how to select a client certificate to send with a request.</span></span> <span data-ttu-id="658eb-123">Un certificat avec le sujet « My Middle-Tier Certificate » est choisi dans le magasin de certificats « personnel » dans le Registre sous **HKEY \_ local \_ machine**.</span><span class="sxs-lookup"><span data-stu-id="658eb-123">A certificate with the subject "My Middle-Tier Certificate" is chosen from the "Personal" certificate store in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="658eb-124">Étant donné que cet exemple de code est spécifique à Microsoft JScript, qui utilise la barre oblique inverse comme caractère d’échappement, deux barres obliques inverses contiguës sont nécessaires pour délimiter les composants de la chaîne de certificat.</span><span class="sxs-lookup"><span data-stu-id="658eb-124">Because this code example is specific to Microsoft JScript, which uses the backslash as an escape character, two adjacent backslashes are required to delimit components of the certificate string.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="658eb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="658eb-125">Requirements</span></span>



| <span data-ttu-id="658eb-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="658eb-126">Requirement</span></span> | <span data-ttu-id="658eb-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="658eb-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="658eb-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="658eb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="658eb-129">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="658eb-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="658eb-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="658eb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="658eb-131">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="658eb-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="658eb-132">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="658eb-132">Redistributable</span></span><br/>          | <span data-ttu-id="658eb-133">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="658eb-133">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="658eb-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="658eb-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="658eb-135"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="658eb-135"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="658eb-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="658eb-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="658eb-137"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="658eb-137"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="658eb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="658eb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="658eb-139"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="658eb-139"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="658eb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="658eb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658eb-141">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="658eb-141">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="658eb-142">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="658eb-142">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="658eb-143">SSL dans WinHTTP</span><span class="sxs-lookup"><span data-stu-id="658eb-143">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="658eb-144">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="658eb-144">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




