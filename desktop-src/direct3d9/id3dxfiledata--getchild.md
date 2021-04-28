---
description: 'ID3DXFileData :: GetChild, méthode-récupère un objet enfant dans cet objet de données de fichier.'
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
ms.openlocfilehash: 7fe6c0393e5cfb9ed8aeaf5808d33175e7f9bfe5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090377"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="98474-103">ID3DXFileData :: GetChild, méthode</span><span class="sxs-lookup"><span data-stu-id="98474-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="98474-104">Récupère un objet enfant dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="98474-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="98474-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98474-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="98474-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98474-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98474-107">*uiChild* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98474-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98474-108">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98474-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98474-109">ID de l’objet enfant à récupérer.</span><span class="sxs-lookup"><span data-stu-id="98474-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="98474-110">*ppChild* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98474-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98474-111">Type : **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="98474-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="98474-112">Adresse d’un pointeur pour recevoir le pointeur d’interface de l’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="98474-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98474-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98474-113">Return value</span></span>

<span data-ttu-id="98474-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="98474-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="98474-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="98474-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="98474-116">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="98474-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="98474-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98474-117">Requirements</span></span>



| <span data-ttu-id="98474-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98474-118">Requirement</span></span> | <span data-ttu-id="98474-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="98474-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98474-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="98474-120">Header</span></span><br/>  | <dl> <span data-ttu-id="98474-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="98474-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="98474-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="98474-122">Library</span></span><br/> | <dl> <span data-ttu-id="98474-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98474-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="98474-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98474-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98474-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="98474-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
