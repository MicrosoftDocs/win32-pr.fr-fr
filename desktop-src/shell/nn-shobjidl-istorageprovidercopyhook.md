---
description: Définit une méthode qui détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.
title: " IStorageProviderCopyHook"
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384403"
---
# <a name="istorageprovidercopyhook-interface"></a><span data-ttu-id="efbaf-103"> IStorageProviderCopyHook</span><span class="sxs-lookup"><span data-stu-id="efbaf-103">IStorageProviderCopyHook interface</span></span>

<span data-ttu-id="efbaf-104">Expose une méthode qui détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.</span><span class="sxs-lookup"><span data-stu-id="efbaf-104">Exposes a method that determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="members"></a><span data-ttu-id="efbaf-105">Membres</span><span class="sxs-lookup"><span data-stu-id="efbaf-105">Members</span></span>

<span data-ttu-id="efbaf-106">L’interface **IStorageProviderCopyHook** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="efbaf-106">The **IStorageProviderCopyHook** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="efbaf-107">**IStorageProviderCopyHook** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="efbaf-107">**IStorageProviderCopyHook** also has these types of members:</span></span>

- [<span data-ttu-id="efbaf-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="efbaf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="efbaf-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="efbaf-109">Methods</span></span>

<span data-ttu-id="efbaf-110">L’interface **IStorageProviderCopyHook** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="efbaf-110">The **IStorageProviderCopyHook** interface has these methods.</span></span>



| <span data-ttu-id="efbaf-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="efbaf-111">Method</span></span>                                           | <span data-ttu-id="efbaf-112">Description</span><span class="sxs-lookup"><span data-stu-id="efbaf-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efbaf-113">**CopyCallback**</span><span class="sxs-lookup"><span data-stu-id="efbaf-113">**CopyCallback**</span></span>](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  <span data-ttu-id="efbaf-114">Détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.</span><span class="sxs-lookup"><span data-stu-id="efbaf-114">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>                                                           |


## <a name="requirements"></a><span data-ttu-id="efbaf-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="efbaf-115">Requirements</span></span>

| <span data-ttu-id="efbaf-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efbaf-116">Requirement</span></span> | <span data-ttu-id="efbaf-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="efbaf-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efbaf-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efbaf-118">Minimum supported client</span></span> | <span data-ttu-id="efbaf-119">Windows 10 Insider Preview, version 19624</span><span class="sxs-lookup"><span data-stu-id="efbaf-119">Windows 10 Insider Preview Build 19624</span></span>                                                |
| <span data-ttu-id="efbaf-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="efbaf-120">Header</span></span><br/>                   | <span data-ttu-id="efbaf-121">ShObjIdl. h</span><span class="sxs-lookup"><span data-stu-id="efbaf-121">shobjidl.h</span></span>   |
