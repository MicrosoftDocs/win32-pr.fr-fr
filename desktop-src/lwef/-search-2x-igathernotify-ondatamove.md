---
title: Méthode IGatherNotify OnDataMove (déconseillée)
description: Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | Méthode IGatherNotify OnDataMove (déconseillée)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Méthode OnDataMove (déconseillée) fonctionnalités héritées de l’environnement Windows
- Méthode OnDataMove (déconseillée) fonctionnalités d’environnement Windows héritées, interface IGatherNotify
- Interface IGatherNotify fonctionnalités d’environnement Windows héritées, méthode OnDataMove (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322178"
---
# <a name="igathernotifyondatamove-deprecated-method"></a><span data-ttu-id="3dcb0-107">IGatherNotify :: OnDataMove (méthode déconseillée)</span><span class="sxs-lookup"><span data-stu-id="3dcb0-107">IGatherNotify::OnDataMove (Deprecated) method</span></span>

<span data-ttu-id="3dcb0-108">\[Les **OnDataMove** peuvent être modifiés ou non disponibles dans les versions ultérieures du système d’exploitation ou du produit.\]</span><span class="sxs-lookup"><span data-stu-id="3dcb0-108">\[**OnDataMove** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="3dcb0-109">Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="3dcb0-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="3dcb0-110">Cette méthode avertit l’indexeur des données qui ont été déplacées.</span><span class="sxs-lookup"><span data-stu-id="3dcb0-110">This method notifies the indexer of data that has been moved.</span></span> <span data-ttu-id="3dcb0-111">Lorsqu’il envoie la notification à l’indexeur, il comprend l’ancienne adresse, la nouvelle adresse et l’adresse logique.</span><span class="sxs-lookup"><span data-stu-id="3dcb0-111">When it sends the notification to the indexer, it includes the old address, new address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dcb0-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dcb0-112">Syntax</span></span>


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="3dcb0-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dcb0-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dcb0-114">*eChangeAdviseSemantics* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3dcb0-114">*eChangeAdviseSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dcb0-115">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="3dcb0-115">Type: **long**</span></span>

<span data-ttu-id="3dcb0-116">Paramètre énuméré qui décrit le type de déplacement qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="3dcb0-116">An enumerated parameter that describes the type of move that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3dcb0-117">*bstrOldAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3dcb0-117">*bstrOldAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dcb0-118">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3dcb0-118">Type: **BSTR**</span></span>

<span data-ttu-id="3dcb0-119">Ancienne adresse de l’élément qui a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="3dcb0-119">The old address of the item that moved.</span></span> <span data-ttu-id="3dcb0-120">Pour les fichiers normaux,*eChangeAdviseSematics* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3dcb0-120">For normal files,*eChangeAdviseSematics* is **NULL**.</span></span> <span data-ttu-id="3dcb0-121">Dans le cas d’un dossier ou d’un répertoire, définissez *eChangeAdviseSematics* sur le \_ répertoire sémantique d’autorité de certification GTHR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3dcb0-121">For a folder or directory, set *eChangeAdviseSematics* to GTHR\_CA\_SEMANTICS\_DIRECTORY.</span></span>

</dd> <dt>

<span data-ttu-id="3dcb0-122">*bstrNewAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3dcb0-122">*bstrNewAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dcb0-123">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3dcb0-123">Type: **BSTR**</span></span>

<span data-ttu-id="3dcb0-124">Nouvelle adresse de l’élément qui a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="3dcb0-124">The new address of the item that moved.</span></span>

</dd> <dt>

<span data-ttu-id="3dcb0-125">*bstrLogicalAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3dcb0-125">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dcb0-126">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3dcb0-126">Type: **BSTR**</span></span>

<span data-ttu-id="3dcb0-127">Adresse logique de l’élément qui a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="3dcb0-127">The logical address of the item that moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dcb0-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3dcb0-128">Return value</span></span>

<span data-ttu-id="3dcb0-129">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3dcb0-129">This method does not return a value.</span></span>

 

 
