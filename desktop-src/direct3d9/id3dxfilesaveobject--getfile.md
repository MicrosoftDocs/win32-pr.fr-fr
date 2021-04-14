---
description: Obtient l’interface ID3DXFile de l’objet qui a créé cet objet ID3DXFileSaveObject.
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: 'ID3DXFileSaveObject :: GetFile, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 137f8245b94bb0ebd14e81d5f73a7ba9622a4933
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394175"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a><span data-ttu-id="88775-103">ID3DXFileSaveObject :: GetFile, méthode</span><span class="sxs-lookup"><span data-stu-id="88775-103">ID3DXFileSaveObject::GetFile method</span></span>

<span data-ttu-id="88775-104">Obtient l’interface [**ID3DXFile**](id3dxfile.md) de l’objet qui a créé cet objet [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="88775-104">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="88775-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88775-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="88775-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88775-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88775-107">*ppFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="88775-107">*ppFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88775-108">Type : **[ **ID3DXFile**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="88775-108">Type: **[**ID3DXFile**](id3dxfile.md)**</span></span>

<span data-ttu-id="88775-109">Adresse d’un pointeur vers un objet [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="88775-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88775-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88775-110">Return value</span></span>

<span data-ttu-id="88775-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="88775-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="88775-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="88775-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="88775-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADVALUE, e \_ nointerface, e \_ pointer.</span><span class="sxs-lookup"><span data-stu-id="88775-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, E\_NOINTERFACE, E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="88775-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88775-114">Requirements</span></span>



| <span data-ttu-id="88775-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88775-115">Requirement</span></span> | <span data-ttu-id="88775-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="88775-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88775-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="88775-117">Header</span></span><br/>  | <dl> <span data-ttu-id="88775-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="88775-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="88775-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="88775-119">Library</span></span><br/> | <dl> <span data-ttu-id="88775-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88775-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="88775-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88775-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88775-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="88775-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




