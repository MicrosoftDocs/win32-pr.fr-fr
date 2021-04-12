---
title: IMsRdpClientShell, méthode de lancement
description: Lance le contenu des fichiers distants à partir de Bureau à distance Accès web (RD Accès web) ou d’un autre portail Web.
ms.assetid: a0aa12e4-8b6f-4a3a-a6b8-f5def0b8bd90
ms.tgt_platform: multiple
keywords:
- Launch, méthode Services Bureau à distance
- Launch, méthode Services Bureau à distance, IMsRdpClientShell, interface
- Services Bureau à distance de l’interface IMsRdpClientShell, méthode Launch
topic_type:
- apiref
api_name:
- IMsRdpClientShell.Launch
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae895d8a12824c6aca1dcbd69c5055b3ca6f3e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384176"
---
# <a name="imsrdpclientshelllaunch-method"></a><span data-ttu-id="e7efe-106">IMsRdpClientShell :: Launch, méthode</span><span class="sxs-lookup"><span data-stu-id="e7efe-106">IMsRdpClientShell::Launch method</span></span>

<span data-ttu-id="e7efe-107">Lance le contenu des fichiers distants à partir de Bureau à distance Accès web (RD Accès web) ou d’un autre portail Web.</span><span class="sxs-lookup"><span data-stu-id="e7efe-107">Launches remote file content from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7efe-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7efe-108">Syntax</span></span>


```C++
HRESULT Launch();
```



## <a name="parameters"></a><span data-ttu-id="e7efe-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7efe-109">Parameters</span></span>

<span data-ttu-id="e7efe-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e7efe-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7efe-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7efe-111">Return value</span></span>

<span data-ttu-id="e7efe-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e7efe-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7efe-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7efe-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7efe-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7efe-114">Requirements</span></span>



| <span data-ttu-id="e7efe-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7efe-115">Requirement</span></span> | <span data-ttu-id="e7efe-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7efe-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7efe-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7efe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7efe-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7efe-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e7efe-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7efe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7efe-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7efe-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e7efe-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e7efe-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7efe-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7efe-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7efe-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e7efe-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7efe-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7efe-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7efe-125">IID</span><span class="sxs-lookup"><span data-stu-id="e7efe-125">IID</span></span><br/>                      | <span data-ttu-id="e7efe-126">IID \_ IMsRdpClientShell est défini en tant que d012ae6d-C19A-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="e7efe-126">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="e7efe-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7efe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7efe-128">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="e7efe-128">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





