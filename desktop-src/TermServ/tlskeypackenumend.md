---
title: TLSKeyPackEnumEnd fonction)
description: Continue à partir d’un appel précédent à la fonction TLSKeyPackEnumBegin et met fin à l’énumération.
ms.assetid: 3434e18d-54c9-46ed-b6a5-bc174b63a152
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSKeyPackEnumEnd
topic_type:
- apiref
api_name:
- TLSKeyPackEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04723318b29adff7a647fe2cab39fb0b16f3f5a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741276"
---
# <a name="tlskeypackenumend-function"></a><span data-ttu-id="89b6c-104">TLSKeyPackEnumEnd fonction)</span><span class="sxs-lookup"><span data-stu-id="89b6c-104">TLSKeyPackEnumEnd function</span></span>

<span data-ttu-id="89b6c-105">Continue à partir d’un appel précédent à la fonction [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) et met fin à l’énumération.</span><span class="sxs-lookup"><span data-stu-id="89b6c-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="89b6c-106">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="89b6c-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="89b6c-107">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="89b6c-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="89b6c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89b6c-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="89b6c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89b6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89b6c-110">*hHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89b6c-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89b6c-111">Handle vers un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="89b6c-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="89b6c-112">Spécifiez un descripteur ouvert par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="89b6c-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="89b6c-113">*pdwErrCode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="89b6c-113">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89b6c-114">Pointeur vers une variable qui reçoit l’un des codes d’erreur suivants au retour.</span><span class="sxs-lookup"><span data-stu-id="89b6c-114">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="89b6c-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ \_Réussite S** (0)</span><span class="sxs-lookup"><span data-stu-id="89b6c-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89b6c-116">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="89b6c-116">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span data-ttu-id="89b6c-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**Lserver \_ \_ \_ Pointeur E non valide** (5005)</span><span class="sxs-lookup"><span data-stu-id="89b6c-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER\_E\_INVALID\_HANDLE** (5005)</span></span>


</dt> <dd>

<span data-ttu-id="89b6c-118">Le descripteur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="89b6c-118">The handle is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89b6c-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89b6c-119">Return value</span></span>

<span data-ttu-id="89b6c-120">Cette fonction retourne les valeurs de retour possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="89b6c-120">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="89b6c-121">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="89b6c-121">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="89b6c-122">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="89b6c-122">The call succeeded.</span></span> <span data-ttu-id="89b6c-123">Vérifiez la valeur du paramètre *pdwErrCode* pour obtenir le code de retour de l’appel.</span><span class="sxs-lookup"><span data-stu-id="89b6c-123">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="89b6c-124">**\_argument RPC \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="89b6c-124">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="89b6c-125">L’argument n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="89b6c-125">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89b6c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89b6c-126">Requirements</span></span>



| <span data-ttu-id="89b6c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89b6c-127">Requirement</span></span> | <span data-ttu-id="89b6c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="89b6c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89b6c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89b6c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="89b6c-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89b6c-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89b6c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89b6c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="89b6c-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89b6c-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89b6c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="89b6c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89b6c-134"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89b6c-134"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b6c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89b6c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b6c-136">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="89b6c-136">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="89b6c-137">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="89b6c-137">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="89b6c-138">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="89b6c-138">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="89b6c-139">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="89b6c-139">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> </dl>

 

