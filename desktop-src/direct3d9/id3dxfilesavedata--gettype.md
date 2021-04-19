---
description: Récupère l’ID de modèle de ce nœud de données de fichier.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: 'ID3DXFileSaveData :: GetType, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b774f71b4be111efcdbdaf8bc41b40d4b0efaa95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520353"
---
# <a name="id3dxfilesavedatagettype-method"></a><span data-ttu-id="54570-103">ID3DXFileSaveData :: GetType, méthode</span><span class="sxs-lookup"><span data-stu-id="54570-103">ID3DXFileSaveData::GetType method</span></span>

<span data-ttu-id="54570-104">Récupère l’ID de modèle de ce nœud de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="54570-104">Retrieves the template ID of this file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="54570-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54570-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a><span data-ttu-id="54570-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54570-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54570-107">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54570-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54570-108">Type : **[ **GUID**](guid.md)\***</span><span class="sxs-lookup"><span data-stu-id="54570-108">Type: **[**GUID**](guid.md)\***</span></span>

<span data-ttu-id="54570-109">Pointeur vers le GUID représentant le modèle dans ce nœud de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="54570-109">Pointer to the GUID representing the template in this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54570-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54570-110">Return value</span></span>

<span data-ttu-id="54570-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54570-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54570-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54570-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="54570-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="54570-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="54570-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54570-114">Requirements</span></span>



| <span data-ttu-id="54570-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54570-115">Requirement</span></span> | <span data-ttu-id="54570-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="54570-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54570-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="54570-117">Header</span></span><br/>  | <dl> <span data-ttu-id="54570-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="54570-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="54570-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54570-119">Library</span></span><br/> | <dl> <span data-ttu-id="54570-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54570-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="54570-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54570-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54570-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="54570-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




