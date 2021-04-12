---
title: WSMan. Error, propriété (WSManDisp. h)
description: Obtient des informations supplémentaires sur l’erreur, dans un flux XML, pour l’appel précédent à une méthode WSMan si Windows Remote Management Service n’a pas pu créer un objet de session, un objet ConnectionOptions ou un objet ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de propriétés d’erreur
- Windows Remote Management de propriété Error, objet WSMan
- Objet WSMan Windows Remote Management, propriété Error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103804"
---
# <a name="wsmanerror-property"></a><span data-ttu-id="717bb-106">WSMan. Error, propriété</span><span class="sxs-lookup"><span data-stu-id="717bb-106">WSMan.Error property</span></span>

<span data-ttu-id="717bb-107">Obtient des informations supplémentaires sur l’erreur, dans un flux XML, pour l’appel précédent à une méthode [**WSMan**](wsman.md) si Windows Remote Management Service n’a pas pu créer un objet de [**session**](session.md) , un objet [**ConnectionOptions**](connectionoptions.md) ou un objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="717bb-107">Gets additional error information, in an XML stream, for the preceding call to a [**WSMan**](wsman.md) method if Windows Remote Management service was unable to create a [**Session**](session.md) object, a [**ConnectionOptions**](connectionoptions.md) object, or a [**ResourceLocator**](resourcelocator.md) object.</span></span>

<span data-ttu-id="717bb-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="717bb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="717bb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="717bb-109">Syntax</span></span>


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a><span data-ttu-id="717bb-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="717bb-110">Property value</span></span>

<span data-ttu-id="717bb-111">Représentation XML des informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="717bb-111">The XML representation of the error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="717bb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="717bb-112">Requirements</span></span>



| <span data-ttu-id="717bb-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="717bb-113">Requirement</span></span> | <span data-ttu-id="717bb-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="717bb-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="717bb-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="717bb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="717bb-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="717bb-116">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="717bb-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="717bb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="717bb-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="717bb-118">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="717bb-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="717bb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="717bb-120"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="717bb-120"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="717bb-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="717bb-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="717bb-122"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="717bb-122"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="717bb-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="717bb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="717bb-124"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="717bb-124"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="717bb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="717bb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="717bb-126"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="717bb-126"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="717bb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="717bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="717bb-128">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="717bb-128">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





