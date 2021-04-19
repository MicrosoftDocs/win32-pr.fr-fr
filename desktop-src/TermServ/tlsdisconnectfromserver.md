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
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106514257"
---
# <a name="tlsdisconnectfromserver-function"></a><span data-ttu-id="70d95-104">TLSDisconnectFromServer fonction)</span><span class="sxs-lookup"><span data-stu-id="70d95-104">TLSDisconnectFromServer function</span></span>

<span data-ttu-id="70d95-105">Ferme un handle ouvert sur un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="70d95-105">Closes an open handle to a Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="70d95-106">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="70d95-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="70d95-107">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="70d95-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="70d95-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70d95-108">Syntax</span></span>


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a><span data-ttu-id="70d95-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70d95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70d95-110">*hHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70d95-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d95-111">Handle vers un serveur de licences Bureau à distance qui est ouvert par un appel à la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="70d95-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70d95-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70d95-112">Return value</span></span>

<span data-ttu-id="70d95-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="70d95-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70d95-114">Notes</span><span class="sxs-lookup"><span data-stu-id="70d95-114">Remarks</span></span>

<span data-ttu-id="70d95-115">Appelez la fonction **TLSDisconnectFromServer** dans le cadre de la routine de nettoyage de votre programme pour fermer tous les descripteurs de serveur ouverts par les appels à la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="70d95-115">Call the **TLSDisconnectFromServer** function as part of your program's clean-up routine to close all the server handles that are opened by calls to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="70d95-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70d95-116">Requirements</span></span>



| <span data-ttu-id="70d95-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70d95-117">Requirement</span></span> | <span data-ttu-id="70d95-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="70d95-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70d95-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70d95-119">Minimum supported client</span></span><br/> | <span data-ttu-id="70d95-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70d95-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="70d95-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70d95-121">Minimum supported server</span></span><br/> | <span data-ttu-id="70d95-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70d95-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70d95-123">DLL</span><span class="sxs-lookup"><span data-stu-id="70d95-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70d95-124"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70d95-124"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70d95-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70d95-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d95-126">**\_handle TLS**</span><span class="sxs-lookup"><span data-stu-id="70d95-126">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="70d95-127">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="70d95-127">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

