---
description: Libère les chargeurs de classes Java qui ont pu être consommés lors de l’exploration des applets.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: NotifyBrowserShutdown fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520917"
---
# <a name="notifybrowsershutdown-function"></a><span data-ttu-id="b7b9f-103">NotifyBrowserShutdown fonction)</span><span class="sxs-lookup"><span data-stu-id="b7b9f-103">NotifyBrowserShutdown function</span></span>

<span data-ttu-id="b7b9f-104">Libère les chargeurs de classes Java qui ont pu être consommés lors de l’exploration des applets.</span><span class="sxs-lookup"><span data-stu-id="b7b9f-104">Frees Java class loaders that may have been consumed while browsing the applets.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b9f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7b9f-105">Syntax</span></span>


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="b7b9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7b9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7b9f-107">*lpvReserved*</span><span class="sxs-lookup"><span data-stu-id="b7b9f-107">*lpvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="b7b9f-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="b7b9f-108">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7b9f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7b9f-109">Return value</span></span>

<span data-ttu-id="b7b9f-110">Si la fonction est réussie, la valeur de retour est **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b7b9f-110">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="b7b9f-111">Dans le cas contraire, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b7b9f-111">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7b9f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b7b9f-112">Remarks</span></span>

<span data-ttu-id="b7b9f-113">Lorsque le nombre de fenêtres du navigateur atteint zéro en mode Web intégré, cette fonction libère les chargeurs de classe Java.</span><span class="sxs-lookup"><span data-stu-id="b7b9f-113">When the count of browser windows reaches zero in integrated Web mode, this function frees the Java class loaders.</span></span> <span data-ttu-id="b7b9f-114">Lorsque l’utilisateur redémarre l’exploration des applets, la machine virtuelle Java télécharge les derniers fichiers de classe.</span><span class="sxs-lookup"><span data-stu-id="b7b9f-114">When the user starts browsing applets again, the Java VM will download the latest class files.</span></span>

<span data-ttu-id="b7b9f-115">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b7b9f-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b9f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7b9f-116">Requirements</span></span>



| <span data-ttu-id="b7b9f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7b9f-117">Requirement</span></span> | <span data-ttu-id="b7b9f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7b9f-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b9f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="b7b9f-119">DLL</span></span><br/> | <dl> <span data-ttu-id="b7b9f-120"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7b9f-120"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
