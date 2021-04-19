---
description: Décode et stocke une chaîne.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526398"
---
# <a name="cchlszofid2-function"></a><span data-ttu-id="ec370-103">CchLszOfId2 fonction)</span><span class="sxs-lookup"><span data-stu-id="ec370-103">CchLszOfId2 function</span></span>

<span data-ttu-id="ec370-104">Décode et stocke une chaîne.</span><span class="sxs-lookup"><span data-stu-id="ec370-104">Decodes and stores a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec370-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec370-105">Syntax</span></span>


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a><span data-ttu-id="ec370-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec370-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec370-107">*id*</span><span class="sxs-lookup"><span data-stu-id="ec370-107">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="ec370-108">Identificateur de la chaîne dans le fichier de ressources à décoder et à stocker.</span><span class="sxs-lookup"><span data-stu-id="ec370-108">The identifier of the string in the resource file to be decoded and stored.</span></span> <span data-ttu-id="ec370-109">La validité de la chaîne n’est pas vérifiée.</span><span class="sxs-lookup"><span data-stu-id="ec370-109">The validity of the string is not verified.</span></span>

</dd> <dt>

<span data-ttu-id="ec370-110">*lsz*</span><span class="sxs-lookup"><span data-stu-id="ec370-110">*lsz*</span></span> 
</dt> <dd>

<span data-ttu-id="ec370-111">Pointeur vers une mémoire tampon avec une longueur de *Cbmax*.</span><span class="sxs-lookup"><span data-stu-id="ec370-111">A pointer to a buffer with a length of *cbmax*.</span></span> <span data-ttu-id="ec370-112">Les chaînes dont la longueur est supérieure à *Cbmax* sont tronquées.</span><span class="sxs-lookup"><span data-stu-id="ec370-112">Strings that are longer than *cbmax* are truncated.</span></span>

</dd> <dt>

<span data-ttu-id="ec370-113">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="ec370-113">*cbmax*</span></span> 
</dt> <dd>

<span data-ttu-id="ec370-114">Longueur maximale de la chaîne à stocker dans le paramètre *LSZ* .</span><span class="sxs-lookup"><span data-stu-id="ec370-114">The maximum length of the string to be stored in the *lsz* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec370-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec370-115">Return value</span></span>

<span data-ttu-id="ec370-116">Cette fonction retourne la chaîne décodée.</span><span class="sxs-lookup"><span data-stu-id="ec370-116">This function returns the decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec370-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ec370-117">Remarks</span></span>

<span data-ttu-id="ec370-118">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ec370-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec370-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec370-119">Requirements</span></span>



| <span data-ttu-id="ec370-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec370-120">Requirement</span></span> | <span data-ttu-id="ec370-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec370-121">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec370-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ec370-122">DLL</span></span><br/> | <dl> <span data-ttu-id="ec370-123"><dt>Msjint40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec370-123"><dt>Msjint40.dll</dt></span></span> </dl> |



 

 
