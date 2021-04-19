---
description: Récupère les données de l’un des membres de l’objet ou les données de tous les membres. Action déconseillée.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'IDirectXFileData :: GetData, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532466"
---
# <a name="idirectxfiledatagetdata-method"></a><span data-ttu-id="8457d-104">IDirectXFileData :: GetData, méthode</span><span class="sxs-lookup"><span data-stu-id="8457d-104">IDirectXFileData::GetData method</span></span>

<span data-ttu-id="8457d-105">Récupère les données de l’un des membres de l’objet ou les données de tous les membres.</span><span class="sxs-lookup"><span data-stu-id="8457d-105">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="8457d-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8457d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="8457d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8457d-107">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a><span data-ttu-id="8457d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8457d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8457d-109">*szMember* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8457d-109">*szMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8457d-110">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8457d-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8457d-111">Pointeur vers le nom du membre pour lequel récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="8457d-111">Pointer to the name of the member for which to retrieve data.</span></span> <span data-ttu-id="8457d-112">Spécifiez **null** pour récupérer tous les données des membres requis.</span><span class="sxs-lookup"><span data-stu-id="8457d-112">Specify **NULL** to retrieve all required members' data.</span></span>

</dd> <dt>

<span data-ttu-id="8457d-113">*PCB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8457d-113">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8457d-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8457d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8457d-115">Pointeur qui reçoit la taille de la mémoire tampon ppvData, en octets.</span><span class="sxs-lookup"><span data-stu-id="8457d-115">Pointer to receive the ppvData buffer size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8457d-116">*ppvData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8457d-116">*ppvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8457d-117">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="8457d-117">Type: **void\*\***</span></span>

<span data-ttu-id="8457d-118">Adresse d’un pointeur vers la mémoire tampon pour recevoir les données associées à szMember.</span><span class="sxs-lookup"><span data-stu-id="8457d-118">Address of a pointer to the buffer to receive the data associated with szMember.</span></span> <span data-ttu-id="8457d-119">Si szMember a la **valeur null**, ppvData est défini pour pointer vers une mémoire tampon contenant toutes les données des membres requis dans un bloc de mémoire contigu.</span><span class="sxs-lookup"><span data-stu-id="8457d-119">If szMember is **NULL**, ppvData is set to point to a buffer containing all required members' data in a contiguous block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8457d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8457d-120">Return value</span></span>

<span data-ttu-id="8457d-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8457d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8457d-122">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8457d-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="8457d-123">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDATAREFERENCE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="8457d-123">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADDataReference, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="8457d-124">Notes</span><span class="sxs-lookup"><span data-stu-id="8457d-124">Remarks</span></span>

<span data-ttu-id="8457d-125">Cette méthode récupère les données pour les membres requis d’un objet de données, mais aucune donnée pour les membres facultatifs (enfants).</span><span class="sxs-lookup"><span data-stu-id="8457d-125">This method retrieves the data for required members of a data object but no data for optional (child) members.</span></span> <span data-ttu-id="8457d-126">Utilisez [**IDirectXFileData :: GetNextObject**](idirectxfiledata--getnextobject.md) pour récupérer des objets enfants.</span><span class="sxs-lookup"><span data-stu-id="8457d-126">Use [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) to retrieve child objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="8457d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8457d-127">Requirements</span></span>



| <span data-ttu-id="8457d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8457d-128">Requirement</span></span> | <span data-ttu-id="8457d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8457d-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8457d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8457d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8457d-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="8457d-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="8457d-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8457d-132">Library</span></span><br/> | <dl> <span data-ttu-id="8457d-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8457d-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8457d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8457d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8457d-135">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="8457d-135">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="8457d-136">**IDirectXFileData::GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="8457d-136">**IDirectXFileData::GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
