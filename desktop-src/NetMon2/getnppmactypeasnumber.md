---
description: Récupère le type MAC de la catégorie NetworkInfo de la section NPP de l’objet BLOB et convertit les données de type en un numéro de type MAC.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: GetNPPMacTypeAsNumber, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525132"
---
# <a name="getnppmactypeasnumber-function"></a><span data-ttu-id="1f128-103">GetNPPMacTypeAsNumber fonction)</span><span class="sxs-lookup"><span data-stu-id="1f128-103">GetNPPMacTypeAsNumber function</span></span>

<span data-ttu-id="1f128-104">La fonction **GetNPPMacTypeAsNumber** récupère le type Mac de la catégorie NetworkInfo de la section NPP de l’objet BLOB et convertit les données de type en un numéro de type Mac.</span><span class="sxs-lookup"><span data-stu-id="1f128-104">The **GetNPPMacTypeAsNumber** function retrieves the MAC type from the NetworkInfo category of the NPP section of the BLOB and converts the type data into a MAC type number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f128-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f128-105">Syntax</span></span>


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a><span data-ttu-id="1f128-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f128-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f128-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f128-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f128-108">Handle vers l’objet BLOB spécifié.</span><span class="sxs-lookup"><span data-stu-id="1f128-108">A handle to the specified BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="1f128-109">*lpMacType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f128-109">*lpMacType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f128-110">Pointeur vers le type MAC.</span><span class="sxs-lookup"><span data-stu-id="1f128-110">A pointer to the MAC type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f128-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f128-111">Return value</span></span>

<span data-ttu-id="1f128-112">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1f128-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1f128-113">Si la balise n’est pas disponible, la valeur de retour est de \_ type Mac \_ Unknown.</span><span class="sxs-lookup"><span data-stu-id="1f128-113">If the tag is unavailable, the return value is MAC\_TYPE\_UNKNOWN.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f128-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1f128-114">Remarks</span></span>

<span data-ttu-id="1f128-115">Cette fonction mappe la balise, **NPP : NetworkInfo : MacType** au **\_ type \_ \* Mac** , comme défini dans le fichier Npptypes. h.</span><span class="sxs-lookup"><span data-stu-id="1f128-115">This function maps the tag, **NPP:NetworkInfo:MacType** to the **MAC\_TYPE\_\*** as defined in the Npptypes.h file.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f128-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f128-116">Requirements</span></span>



| <span data-ttu-id="1f128-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f128-117">Requirement</span></span> | <span data-ttu-id="1f128-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f128-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f128-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f128-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1f128-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f128-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1f128-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f128-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1f128-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f128-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f128-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f128-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f128-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f128-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1f128-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f128-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f128-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f128-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f128-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1f128-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f128-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f128-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




