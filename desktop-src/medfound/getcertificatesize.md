---
description: Obtient la taille d’un certificat pour un pilote d’affichage.
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: GetCertificateSize fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateSize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bcd1f49ce65978c6a89c89cee1fda38e41434065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317958"
---
# <a name="getcertificatesize-function"></a><span data-ttu-id="cab5d-103">GetCertificateSize fonction)</span><span class="sxs-lookup"><span data-stu-id="cab5d-103">GetCertificateSize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cab5d-104">Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cab5d-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="cab5d-105">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cab5d-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="cab5d-106">Obtient la taille d’un certificat pour un pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cab5d-106">Gets the size of a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="cab5d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cab5d-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificateSize(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ ULONG                    *pulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="cab5d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cab5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cab5d-109">*pstrDeviceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cab5d-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cab5d-110">Pointeur vers une structure [**de \_ chaîne Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) qui contient le nom du périphérique d’affichage, tel que retourné par la fonction [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="cab5d-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="cab5d-111">*ctPVPCertificateType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cab5d-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cab5d-112">Type de certificat, spécifié en tant que membre de l’énumération du **\_ \_ type de certificat DXGKMDT** .</span><span class="sxs-lookup"><span data-stu-id="cab5d-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="cab5d-113">*pulCertificateLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cab5d-113">*pulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cab5d-114">Reçoit la taille du certificat, en octets.</span><span class="sxs-lookup"><span data-stu-id="cab5d-114">Receives the size of the certificate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cab5d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cab5d-115">Return value</span></span>

<span data-ttu-id="cab5d-116">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="cab5d-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="cab5d-117">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="cab5d-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cab5d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="cab5d-118">Remarks</span></span>

<span data-ttu-id="cab5d-119">Les applications doivent appeler la méthode [**IOPMVideoOutput :: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) au lieu de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cab5d-119">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="cab5d-120">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="cab5d-120">This function has no associated import library.</span></span> <span data-ttu-id="cab5d-121">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="cab5d-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="cab5d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cab5d-122">Requirements</span></span>



| <span data-ttu-id="cab5d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cab5d-123">Requirement</span></span> | <span data-ttu-id="cab5d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cab5d-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cab5d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cab5d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cab5d-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cab5d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cab5d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cab5d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cab5d-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cab5d-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cab5d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cab5d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cab5d-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cab5d-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab5d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cab5d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab5d-132">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="cab5d-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="cab5d-133">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="cab5d-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
