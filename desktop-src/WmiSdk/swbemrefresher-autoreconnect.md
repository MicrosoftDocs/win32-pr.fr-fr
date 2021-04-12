---
description: La propriété reconnexion automatique de l’objet SWbemRefresher est une valeur booléenne qui indique si l’actualisateur se reconnecte automatiquement à un fournisseur distant si la connexion est interrompue.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: SWbemRefresher. reconnexion automatique, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321505"
---
# <a name="swbemrefresherautoreconnect-property"></a><span data-ttu-id="758d5-103">SWbemRefresher. reconnexion automatique, propriété</span><span class="sxs-lookup"><span data-stu-id="758d5-103">SWbemRefresher.AutoReconnect property</span></span>

<span data-ttu-id="758d5-104">La propriété **reconnexion automatique** de l’objet [**SWbemRefresher**](swbemrefresher.md) est une valeur booléenne qui indique si l’actualisateur se reconnecte automatiquement à un fournisseur distant si la connexion est interrompue.</span><span class="sxs-lookup"><span data-stu-id="758d5-104">The **AutoReconnect** property of the [**SWbemRefresher**](swbemrefresher.md) object is a Boolean value that indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span>

<span data-ttu-id="758d5-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="758d5-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="758d5-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="758d5-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="758d5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="758d5-107">Syntax</span></span>


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a><span data-ttu-id="758d5-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="758d5-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="758d5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="758d5-109">Remarks</span></span>

<span data-ttu-id="758d5-110">La modification de cette propriété affecte uniquement les objets de l’actualisateur qui sont sauvegardés par un fournisseur à hautes performances.</span><span class="sxs-lookup"><span data-stu-id="758d5-110">Modifying this property affects only objects in the refresher that are backed by a high-performance provider.</span></span> <span data-ttu-id="758d5-111">Si le fournisseur n’est pas un fournisseur à hautes performances, l’affectation de la **valeur true** à la propriété **reconnexion automatique** n’a aucun effet, car l’objet [**SWbemRefresher**](swbemrefresher.md) ne se reconnecte jamais.</span><span class="sxs-lookup"><span data-stu-id="758d5-111">If the provider is not a high-performance provider, then setting the **AutoReconnect** property to **TRUE** has no effect because the [**SWbemRefresher**](swbemrefresher.md) object never reconnects.</span></span>

## <a name="requirements"></a><span data-ttu-id="758d5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="758d5-112">Requirements</span></span>



| <span data-ttu-id="758d5-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="758d5-113">Requirement</span></span> | <span data-ttu-id="758d5-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="758d5-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="758d5-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="758d5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="758d5-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="758d5-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="758d5-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="758d5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="758d5-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="758d5-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="758d5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="758d5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="758d5-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="758d5-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="758d5-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="758d5-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="758d5-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="758d5-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="758d5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="758d5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="758d5-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="758d5-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="758d5-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="758d5-125">CLSID</span></span><br/>                    | <span data-ttu-id="758d5-126">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="758d5-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="758d5-127">IID</span><span class="sxs-lookup"><span data-stu-id="758d5-127">IID</span></span><br/>                      | <span data-ttu-id="758d5-128">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="758d5-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="758d5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="758d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758d5-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="758d5-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




