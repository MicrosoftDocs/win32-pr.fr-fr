---
description: Récupère l’ID de modèle dans cet objet de données de fichier.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'ID3DXFileData :: GetType, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 566052c06d5f7e55629a26442dd774a2f80fd647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394188"
---
# <a name="id3dxfiledatagettype-method"></a><span data-ttu-id="22b02-103">ID3DXFileData :: GetType, méthode</span><span class="sxs-lookup"><span data-stu-id="22b02-103">ID3DXFileData::GetType method</span></span>

<span data-ttu-id="22b02-104">Récupère l’ID de modèle dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="22b02-104">Retrieves the template ID in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22b02-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a><span data-ttu-id="22b02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22b02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b02-107">*PTYPE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="22b02-107">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22b02-108">Type : **const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="22b02-108">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="22b02-109">Pointeur vers le GUID représentant le modèle dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="22b02-109">Pointer to the GUID representing the template in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b02-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22b02-110">Return value</span></span>

<span data-ttu-id="22b02-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22b02-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22b02-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22b02-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="22b02-113">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="22b02-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="22b02-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22b02-114">Requirements</span></span>



| <span data-ttu-id="22b02-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22b02-115">Requirement</span></span> | <span data-ttu-id="22b02-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="22b02-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22b02-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="22b02-117">Header</span></span><br/>  | <dl> <span data-ttu-id="22b02-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b02-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="22b02-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22b02-119">Library</span></span><br/> | <dl> <span data-ttu-id="22b02-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22b02-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="22b02-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22b02-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b02-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="22b02-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




