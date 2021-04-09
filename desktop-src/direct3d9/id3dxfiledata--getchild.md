---
description: Récupère un objet enfant dans cet objet de données de fichier.
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: 'ID3DXFileData :: GetChild, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 37982ca1e4801b7d70bec503ff9510fc66772651
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953910"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="47f5c-103">ID3DXFileData :: GetChild, méthode</span><span class="sxs-lookup"><span data-stu-id="47f5c-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="47f5c-104">Récupère un objet enfant dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="47f5c-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f5c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47f5c-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="47f5c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47f5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f5c-107">*uiChild* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47f5c-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5c-108">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47f5c-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47f5c-109">ID de l’objet enfant à récupérer.</span><span class="sxs-lookup"><span data-stu-id="47f5c-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="47f5c-110">*ppChild* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47f5c-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5c-111">Type : **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="47f5c-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="47f5c-112">Adresse d’un pointeur pour recevoir le pointeur d’interface de l’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="47f5c-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f5c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47f5c-113">Return value</span></span>

<span data-ttu-id="47f5c-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47f5c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47f5c-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47f5c-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="47f5c-116">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="47f5c-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f5c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47f5c-117">Requirements</span></span>



| <span data-ttu-id="47f5c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47f5c-118">Requirement</span></span> | <span data-ttu-id="47f5c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="47f5c-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47f5c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="47f5c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="47f5c-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="47f5c-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="47f5c-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47f5c-122">Library</span></span><br/> | <dl> <span data-ttu-id="47f5c-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47f5c-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="47f5c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47f5c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f5c-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="47f5c-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
