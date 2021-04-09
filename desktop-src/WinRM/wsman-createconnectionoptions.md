---
title: Méthode WSMan. CreateConnectionOptions (WSManDisp. h)
description: Crée un objet ConnectionOptions qui spécifie le nom d’utilisateur et le mot de passe utilisés lors de la création d’une session.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode CreateConnectionOptions
- Méthode CreateConnectionOptions Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode CreateConnectionOptions
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843313"
---
# <a name="wsmancreateconnectionoptions-method"></a><span data-ttu-id="6a9b2-106">Méthode WSMan. CreateConnectionOptions</span><span class="sxs-lookup"><span data-stu-id="6a9b2-106">WSMan.CreateConnectionOptions method</span></span>

<span data-ttu-id="6a9b2-107">Crée un objet [**ConnectionOptions**](connectionoptions.md) qui spécifie le nom d’utilisateur et le mot de passe utilisés lors de la création d’une session.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-107">Creates a [**ConnectionOptions**](connectionoptions.md) object that specifies the user name and password used when creating a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a9b2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a9b2-108">Syntax</span></span>


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a><span data-ttu-id="6a9b2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a9b2-109">Parameters</span></span>

<span data-ttu-id="6a9b2-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a9b2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a9b2-111">Return value</span></span>

<span data-ttu-id="6a9b2-112">Objet [**ConnectionOptions**](connectionoptions.md) utilisé pour spécifier une paire nom d’utilisateur/mot de passe utilisée pour identifier un utilisateur à des fins d’authentification.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-112">A [**ConnectionOptions**](connectionoptions.md) object used to specify a user name and password pair that is used to identify a user for authentication.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a9b2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6a9b2-113">Remarks</span></span>

<span data-ttu-id="6a9b2-114">La syntaxe suivante est utilisée pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6a9b2-114">The following syntax is used to call this method.</span></span>


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a><span data-ttu-id="6a9b2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a9b2-115">Requirements</span></span>



| <span data-ttu-id="6a9b2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a9b2-116">Requirement</span></span> | <span data-ttu-id="6a9b2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a9b2-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9b2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a9b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6a9b2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a9b2-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6a9b2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a9b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6a9b2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a9b2-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6a9b2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a9b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a9b2-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a9b2-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a9b2-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="6a9b2-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a9b2-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a9b2-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6a9b2-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a9b2-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a9b2-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6a9b2-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6a9b2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6a9b2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a9b2-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a9b2-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a9b2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a9b2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a9b2-131">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="6a9b2-131">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="6a9b2-132">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="6a9b2-132">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





