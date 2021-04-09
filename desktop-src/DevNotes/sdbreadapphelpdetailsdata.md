---
Description: Récupère les données de la base de données des détails AppHelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: SdbReadApphelpDetailsData fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942062"
---
# <a name="sdbreadapphelpdetailsdata-function"></a><span data-ttu-id="da28d-103">SdbReadApphelpDetailsData fonction)</span><span class="sxs-lookup"><span data-stu-id="da28d-103">SdbReadApphelpDetailsData function</span></span>

<span data-ttu-id="da28d-104">Récupère les données de la base de données des détails AppHelp.</span><span class="sxs-lookup"><span data-stu-id="da28d-104">Retrieves data from the Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="da28d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da28d-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="da28d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da28d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da28d-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da28d-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da28d-108">Un descripteur de la base de données de détails AppHelp, AppHelp. sdb.</span><span class="sxs-lookup"><span data-stu-id="da28d-108">A handle to the Apphelp details database, Apphelp.sdb.</span></span>

</dd> <dt>

<span data-ttu-id="da28d-109">*pData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="da28d-109">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da28d-110">Structure [**de \_ données APPHELP**](apphelp-data.md) .</span><span class="sxs-lookup"><span data-stu-id="da28d-110">An [**APPHELP\_DATA**](apphelp-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da28d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da28d-111">Return value</span></span>

<span data-ttu-id="da28d-112">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="da28d-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="da28d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da28d-113">Requirements</span></span>



| <span data-ttu-id="da28d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da28d-114">Requirement</span></span> | <span data-ttu-id="da28d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="da28d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da28d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da28d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da28d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da28d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="da28d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da28d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da28d-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da28d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="da28d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="da28d-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da28d-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da28d-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




