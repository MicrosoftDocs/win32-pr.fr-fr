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
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384864"
---
# <a name="tlsconnecttolsserver-function"></a><span data-ttu-id="2f092-104">TLSConnectToLsServer fonction)</span><span class="sxs-lookup"><span data-stu-id="2f092-104">TLSConnectToLsServer function</span></span>

<span data-ttu-id="2f092-105">Ouvre un handle vers le serveur de licences de Bureau à distance spécifié.</span><span class="sxs-lookup"><span data-stu-id="2f092-105">Opens a handle to the specified Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="2f092-106">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="2f092-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="2f092-107">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="2f092-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2f092-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f092-108">Syntax</span></span>


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a><span data-ttu-id="2f092-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f092-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f092-110">*pszLsServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f092-110">*pszLsServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f092-111">Pointeur vers une chaîne se terminant par un caractère **null** qui spécifie le nom NetBIOS du serveur de licences bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2f092-111">Pointer to a **null**-terminated string that specifies the NetBIOS name of the Remote Desktop license server.</span></span> <span data-ttu-id="2f092-112">Si la valeur de ce paramètre est **null**, le serveur spécifié est l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2f092-112">If the value of this parameter is **NULL**, the specified server is the local computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f092-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f092-113">Return value</span></span>

<span data-ttu-id="2f092-114">Si la fonction est réussie, la valeur de retour est un handle vers le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="2f092-114">If the function succeeds, the return value is a handle to the specified server.</span></span>

<span data-ttu-id="2f092-115">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="2f092-115">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="2f092-116">Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="2f092-116">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f092-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2f092-117">Remarks</span></span>

<span data-ttu-id="2f092-118">Lorsque vous avez terminé d’utiliser le handle retourné par la fonction **TLSConnectToLsServer** , libérez-le en appelant la fonction [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) .</span><span class="sxs-lookup"><span data-stu-id="2f092-118">When you have finished using the handle that is returned by the **TLSConnectToLsServer** function, release it by calling the [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f092-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f092-119">Requirements</span></span>



| <span data-ttu-id="2f092-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f092-120">Requirement</span></span> | <span data-ttu-id="2f092-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f092-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f092-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f092-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2f092-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f092-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f092-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f092-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2f092-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f092-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f092-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2f092-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f092-127"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f092-127"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f092-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f092-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f092-129">**\_handle TLS**</span><span class="sxs-lookup"><span data-stu-id="2f092-129">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="2f092-130">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="2f092-130">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

