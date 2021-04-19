---
description: Récupère le GUID de ce nœud de données de fichier ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'ID3DXFileSaveData :: GetId, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b03322e03d1bedc10f9deec82c60418b5ad846b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529621"
---
# <a name="id3dxfilesavedatagetid-method"></a><span data-ttu-id="2d28b-103">ID3DXFileSaveData :: GetId, méthode</span><span class="sxs-lookup"><span data-stu-id="2d28b-103">ID3DXFileSaveData::GetId method</span></span>

<span data-ttu-id="2d28b-104">Récupère le GUID de ce nœud de données de fichier [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="2d28b-104">Retrieves the GUID of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d28b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d28b-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="2d28b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d28b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d28b-107">*PID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d28b-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d28b-108">Type : **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="2d28b-108">Type: **LPGUID**</span></span>

<span data-ttu-id="2d28b-109">Pointeur vers un GUID pour recevoir l’ID de ce nœud de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="2d28b-109">Pointer to a GUID to receive the ID of this file data node.</span></span> <span data-ttu-id="2d28b-110">Si l’objet n’a pas d’ID, la valeur de paramètre retournée est le GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="2d28b-110">If the object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d28b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d28b-111">Return value</span></span>

<span data-ttu-id="2d28b-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d28b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d28b-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2d28b-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2d28b-114">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="2d28b-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d28b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d28b-115">Requirements</span></span>



| <span data-ttu-id="2d28b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d28b-116">Requirement</span></span> | <span data-ttu-id="2d28b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d28b-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d28b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d28b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2d28b-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d28b-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="2d28b-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2d28b-120">Library</span></span><br/> | <dl> <span data-ttu-id="2d28b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d28b-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2d28b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d28b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d28b-123">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="2d28b-123">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




