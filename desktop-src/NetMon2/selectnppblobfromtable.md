---
description: La fonction SelectNPPBlobFromTable sélectionne une carte réseau à partir d’une table d’objets BLOB NPP fournie.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: SelectNPPBlobFromTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201596"
---
# <a name="selectnppblobfromtable-function"></a><span data-ttu-id="1823b-103">SelectNPPBlobFromTable fonction)</span><span class="sxs-lookup"><span data-stu-id="1823b-103">SelectNPPBlobFromTable function</span></span>

<span data-ttu-id="1823b-104">La fonction **SelectNPPBlobFromTable** sélectionne une carte réseau à partir d’une table d’objets BLOB NPP fournie.</span><span class="sxs-lookup"><span data-stu-id="1823b-104">The **SelectNPPBlobFromTable** function selects a NIC from a supplied NPP BLOB table.</span></span>

## <a name="syntax"></a><span data-ttu-id="1823b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1823b-105">Syntax</span></span>


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="1823b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1823b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1823b-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1823b-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1823b-108">Handle vers la fenêtre qui affiche la boîte de dialogue **Sélectionner un réseau** .</span><span class="sxs-lookup"><span data-stu-id="1823b-108">Handle to the window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="1823b-109">*pBlobTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1823b-109">*pBlobTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1823b-110">Pointeur vers la table d’objets BLOB fournie.</span><span class="sxs-lookup"><span data-stu-id="1823b-110">Pointer to the supplied BLOB table.</span></span> <span data-ttu-id="1823b-111">Moniteur réseau utilise ce tableau pour renseigner la boîte de dialogue **Sélectionner un réseau** .</span><span class="sxs-lookup"><span data-stu-id="1823b-111">Network Monitor uses this table to populate the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="1823b-112">*hBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1823b-112">*hBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1823b-113">Handle vers l’objet BLOB qui représente la carte réseau sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="1823b-113">Handle to the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1823b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1823b-114">Return value</span></span>

<span data-ttu-id="1823b-115">Si la fonction réussit et que l’utilisateur sélectionne une carte réseau, la valeur de retour est NMERR \_ Success ; l’objet BLOB vers lequel pointe *hBlob* est renseigné.</span><span class="sxs-lookup"><span data-stu-id="1823b-115">If the function is successful and the user selects a NIC, the return value is NMERR\_SUCCESS; the BLOB pointed to by *hBlob* is filled in.</span></span>

<span data-ttu-id="1823b-116">Si l’utilisateur ne sélectionne pas une carte réseau, la valeur de retour est NMERR \_ aucun NPP n’est \_ \_ sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1823b-116">If the user does not select a NIC, the return value is NMERR\_NO\_NPP\_SELECTED.</span></span>

<span data-ttu-id="1823b-117">Si la fonction échoue, la valeur de retour est une autre valeur NMERR.</span><span class="sxs-lookup"><span data-stu-id="1823b-117">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1823b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1823b-118">Remarks</span></span>

<span data-ttu-id="1823b-119">Quand elle est appelée, Moniteur réseau affiche la boîte de dialogue **Sélectionner un réseau** , que vous pouvez utiliser pour sélectionner une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="1823b-119">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="1823b-120">L’objet BLOB NPP qui représente la carte réseau sélectionnée retourne à l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="1823b-120">The NPP BLOB that represents the selected NIC returns to the calling application.</span></span>

<span data-ttu-id="1823b-121">Pour connaître les différentes façons de sélectionner des cartes réseau, consultez [sélection d’une carte d’interface réseau](selecting-a-network-interface-card.md) .</span><span class="sxs-lookup"><span data-stu-id="1823b-121">To learn the various ways you can select NICs, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="1823b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1823b-122">Requirements</span></span>



| <span data-ttu-id="1823b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1823b-123">Requirement</span></span> | <span data-ttu-id="1823b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1823b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1823b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1823b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1823b-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1823b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1823b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1823b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1823b-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1823b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1823b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1823b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1823b-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1823b-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1823b-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1823b-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="1823b-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1823b-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1823b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1823b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1823b-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1823b-134"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1823b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1823b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1823b-136">GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="1823b-136">GetNPPBlobFromUI</span></span>](getnppblobfromui.md)
</dt> <dt>

[<span data-ttu-id="1823b-137">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="1823b-137">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="1823b-138">Entrées d’objets BLOB spéciales</span><span class="sxs-lookup"><span data-stu-id="1823b-138">Special BLOB Entries</span></span>](special-blob-entries.md)
</dt> </dl>

 

 




