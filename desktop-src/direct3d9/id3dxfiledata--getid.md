---
description: Récupère le GUID de cet objet de données de fichier.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'ID3DXFileData :: GetId, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1dafb296541b1702e9163dcc6d460cf149b4007
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762146"
---
# <a name="id3dxfiledatagetid-method"></a><span data-ttu-id="63627-103">ID3DXFileData :: GetId, méthode</span><span class="sxs-lookup"><span data-stu-id="63627-103">ID3DXFileData::GetId method</span></span>

<span data-ttu-id="63627-104">Récupère le GUID de cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="63627-104">Retrieves the GUID of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="63627-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63627-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="63627-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63627-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63627-107">*PID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="63627-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63627-108">Type : **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="63627-108">Type: **LPGUID**</span></span>

<span data-ttu-id="63627-109">Pointeur vers un GUID pour recevoir l’ID de cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="63627-109">Pointer to a GUID to receive the ID of this file data object.</span></span> <span data-ttu-id="63627-110">Si l’objet de données de fichier n’a pas d’ID, la valeur de paramètre retournée est le GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="63627-110">If the file data object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63627-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63627-111">Return value</span></span>

<span data-ttu-id="63627-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63627-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63627-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="63627-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="63627-114">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="63627-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="63627-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63627-115">Requirements</span></span>



| <span data-ttu-id="63627-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63627-116">Requirement</span></span> | <span data-ttu-id="63627-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="63627-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63627-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="63627-118">Header</span></span><br/>  | <dl> <span data-ttu-id="63627-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="63627-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="63627-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63627-120">Library</span></span><br/> | <dl> <span data-ttu-id="63627-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63627-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="63627-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63627-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63627-123">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="63627-123">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




