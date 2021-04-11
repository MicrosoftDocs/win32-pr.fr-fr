---
description: Vérifie que le profil utilisateur en ligne est chargé.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: OnProfileLoaded, fonction (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756435"
---
# <a name="onprofileloaded-function"></a><span data-ttu-id="e9ef5-103">OnProfileLoaded fonction)</span><span class="sxs-lookup"><span data-stu-id="e9ef5-103">OnProfileLoaded function</span></span>

<span data-ttu-id="e9ef5-104">Vérifie que le profil utilisateur en ligne est chargé.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-104">Checks that the online user profile is loaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ef5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9ef5-105">Syntax</span></span>


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a><span data-ttu-id="e9ef5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9ef5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ef5-107">*ProviderHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9ef5-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ef5-108">Handle du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-108">The provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="e9ef5-109">*UserToken* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9ef5-109">*UserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ef5-110">Jeton de l’utilisateur dont le profil est chargé ou déchargé.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-110">Token of the user whose profile is being loaded or unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="e9ef5-111">*Chargé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9ef5-111">*Loaded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ef5-112">**True** si le profil a été chargé.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-112">**TRUE** if the profile has been loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ef5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9ef5-113">Return value</span></span>

<span data-ttu-id="e9ef5-114">Si la fonction réussit, la fonction retourne l’état \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-114">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="e9ef5-115">Si la fonction échoue, la fonction retourne un code d’erreur différent de zéro qui est une erreur spécifique au fournisseur à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-115">If the function fails, the function returns a nonzero error code that is a provider-specific error for diagnostic purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9ef5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e9ef5-116">Remarks</span></span>

<span data-ttu-id="e9ef5-117">Cette fonction est appelée chaque fois que la fonction [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) est appelée.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-117">This function is called each time the [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) function is called.</span></span> <span data-ttu-id="e9ef5-118">Elle n’est pas synchronisée avec **LoadUserProfile**; autrement dit, **LoadUserProfile** peut avoir retourné et le profil a peut-être été déchargé au moment où la fonction a été appelée.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-118">It is not synchronized with **LoadUserProfile**; that is, **LoadUserProfile** might have returned and the profile might have been unloaded by the time the function was called.</span></span> <span data-ttu-id="e9ef5-119">Cette fonction peut être appelée plusieurs fois, même lorsque le profil a été chargé.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-119">This function can be called more than once even when the profile has been loaded.</span></span> <span data-ttu-id="e9ef5-120">Le fournisseur d’identité ne doit pas supposer qu’un appel à cette fonction avec *Loaded* égal à true sera suivi d’un appel avec *Loaded* égal à false.</span><span class="sxs-lookup"><span data-stu-id="e9ef5-120">The identity provider must not assume that a call to this function with *Loaded* equal to TRUE will be followed by a call with *Loaded* equal to FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ef5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9ef5-121">Requirements</span></span>



| <span data-ttu-id="e9ef5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9ef5-122">Requirement</span></span> | <span data-ttu-id="e9ef5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9ef5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ef5-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9ef5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ef5-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9ef5-125">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e9ef5-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9ef5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ef5-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9ef5-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e9ef5-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9ef5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ef5-129"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ef5-129"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

 
