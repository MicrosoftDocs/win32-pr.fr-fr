---
description: Obtient un certificat pour un pilote d’affichage.
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: GetCertificate fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516591"
---
# <a name="getcertificate-function"></a><span data-ttu-id="b6f79-103">GetCertificate fonction)</span><span class="sxs-lookup"><span data-stu-id="b6f79-103">GetCertificate function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6f79-104">Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b6f79-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="b6f79-105">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="b6f79-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="b6f79-106">Obtient un certificat pour un pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b6f79-106">Gets a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f79-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6f79-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="b6f79-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6f79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6f79-109">*pstrDeviceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6f79-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f79-110">Pointeur vers une structure [**de \_ chaîne Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) qui contient le nom du périphérique d’affichage, tel que retourné par la fonction [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b6f79-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="b6f79-111">*ctPVPCertificateType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6f79-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f79-112">Type de certificat, spécifié en tant que membre de l’énumération du **\_ \_ type de certificat DXGKMDT** .</span><span class="sxs-lookup"><span data-stu-id="b6f79-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="b6f79-113">*pbCertificate* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6f79-113">*pbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f79-114">Pointeur vers une mémoire tampon qui reçoit le certificat.</span><span class="sxs-lookup"><span data-stu-id="b6f79-114">A pointer to a buffer that receives the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="b6f79-115">*ulCertificateLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6f79-115">*ulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f79-116">Taille de la mémoire tampon *pbCertificate* , en octets.</span><span class="sxs-lookup"><span data-stu-id="b6f79-116">The size of the *pbCertificate* buffer, in bytes.</span></span> <span data-ttu-id="b6f79-117">Pour connaître la taille du certificat, appelez [**GetCertificateSize**](getcertificatesize.md).</span><span class="sxs-lookup"><span data-stu-id="b6f79-117">To get the size of the certificate, call [**GetCertificateSize**](getcertificatesize.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6f79-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6f79-118">Return value</span></span>

<span data-ttu-id="b6f79-119">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="b6f79-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="b6f79-120">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="b6f79-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6f79-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b6f79-121">Remarks</span></span>

<span data-ttu-id="b6f79-122">Les applications doivent appeler la méthode [**IOPMVideoOutput :: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) au lieu de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="b6f79-122">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="b6f79-123">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="b6f79-123">This function has no associated import library.</span></span> <span data-ttu-id="b6f79-124">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="b6f79-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6f79-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6f79-125">Requirements</span></span>



| <span data-ttu-id="b6f79-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6f79-126">Requirement</span></span> | <span data-ttu-id="b6f79-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6f79-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f79-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6f79-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b6f79-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6f79-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b6f79-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6f79-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b6f79-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6f79-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6f79-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b6f79-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6f79-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6f79-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6f79-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6f79-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f79-135">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="b6f79-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="b6f79-136">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="b6f79-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
