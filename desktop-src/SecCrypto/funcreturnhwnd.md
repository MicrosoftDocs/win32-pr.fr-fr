---
description: Utilisé par un fournisseur de services de chiffrement (CSP) pour obtenir le handle de fenêtre que le fournisseur CSP doit utiliser comme parent ou propriétaire d’une interface utilisateur affichée.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND pointeur de fonction (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524447"
---
# <a name="crypt_return_hwnd-function-pointer"></a><span data-ttu-id="832f5-103">CRYPT \_ retourne le \_ pointeur de fonction HWND</span><span class="sxs-lookup"><span data-stu-id="832f5-103">CRYPT\_RETURN\_HWND function pointer</span></span>

<span data-ttu-id="832f5-104">La fonction de rappel **FuncReturnhWnd** est utilisée par un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) pour obtenir le handle de fenêtre que le CSP doit utiliser comme parent ou propriétaire d’une interface utilisateur affichée.</span><span class="sxs-lookup"><span data-stu-id="832f5-104">The **FuncReturnhWnd** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to obtain the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="832f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="832f5-105">Syntax</span></span>


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a><span data-ttu-id="832f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="832f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="832f5-107">*phWnd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="832f5-107">*phWnd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="832f5-108">Adresse d’une variable **HWND** qui reçoit le handle de fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="832f5-108">The address of an **HWND** variable that receives the parent window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="832f5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="832f5-109">Return value</span></span>

<span data-ttu-id="832f5-110">Ce pointeur de fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="832f5-110">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="832f5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="832f5-111">Requirements</span></span>



| <span data-ttu-id="832f5-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="832f5-112">Requirement</span></span> | <span data-ttu-id="832f5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="832f5-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="832f5-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="832f5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="832f5-115">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="832f5-115">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="832f5-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="832f5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="832f5-117">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="832f5-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="832f5-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="832f5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="832f5-119"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="832f5-119"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="832f5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="832f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="832f5-121">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="832f5-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="832f5-122">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="832f5-122">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
