---
description: La fonction Extract extrait les fichiers d’un fichier CAB.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Extraire une fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533137"
---
# <a name="extract-function"></a><span data-ttu-id="f2c5f-103">Extraire une fonction</span><span class="sxs-lookup"><span data-stu-id="f2c5f-103">Extract function</span></span>

<span data-ttu-id="f2c5f-104">\[Cette fonction n’étant plus prise en charge, son comportement ne peut pas être garanti.\]</span><span class="sxs-lookup"><span data-stu-id="f2c5f-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="f2c5f-105">La fonction **extract** extrait les fichiers d’un fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="f2c5f-105">The **Extract** function extracts files from a cabinet.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c5f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2c5f-106">Syntax</span></span>


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a><span data-ttu-id="f2c5f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2c5f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c5f-108">*alimentation*</span><span class="sxs-lookup"><span data-stu-id="f2c5f-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c5f-109">Pointeur vers une structure de [**session**](session.md) qui contient des informations sur la session active.</span><span class="sxs-lookup"><span data-stu-id="f2c5f-109">Pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

</dd> <dt>

<span data-ttu-id="f2c5f-110">*lpCabName*</span><span class="sxs-lookup"><span data-stu-id="f2c5f-110">*lpCabName*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c5f-111">Pointeur vers le nom du fichier cab à partir duquel les fichiers doivent être extraits.</span><span class="sxs-lookup"><span data-stu-id="f2c5f-111">Pointer to the name of the cabinet from which files are to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c5f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2c5f-112">Return value</span></span>

<span data-ttu-id="f2c5f-113">Si la fonction est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f2c5f-113">If the function succeeds, it returns **S\_OK**; otherwise, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2c5f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f2c5f-114">Remarks</span></span>

<span data-ttu-id="f2c5f-115">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f2c5f-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2c5f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2c5f-116">Requirements</span></span>



| <span data-ttu-id="f2c5f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2c5f-117">Requirement</span></span> | <span data-ttu-id="f2c5f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2c5f-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c5f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f2c5f-119">DLL</span></span><br/> | <dl> <span data-ttu-id="f2c5f-120"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2c5f-120"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2c5f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2c5f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c5f-122">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="f2c5f-122">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="f2c5f-123">**ERF**</span><span class="sxs-lookup"><span data-stu-id="f2c5f-123">**ERF**</span></span>](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[<span data-ttu-id="f2c5f-124">**SESSION**</span><span class="sxs-lookup"><span data-stu-id="f2c5f-124">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
