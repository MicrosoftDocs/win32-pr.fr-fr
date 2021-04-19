---
title: IGatherNotify OnDataChange (déprécié), méthode
description: Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | IGatherNotify OnDataChange (déprécié), méthode
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Méthode OnDataChange (déconseillée) fonctionnalités héritées de l’environnement Windows
- OnDataChange (déprécié), méthode fonctionnalités d’environnement Windows héritées, interface IGatherNotify
- Interface IGatherNotify fonctionnalités d’environnement Windows héritées, méthode OnDataChange (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106532396"
---
# <a name="igathernotifyondatachange-deprecated-method"></a><span data-ttu-id="1aa90-107">IGatherNotify :: OnDataChange (déconseillé), méthode</span><span class="sxs-lookup"><span data-stu-id="1aa90-107">IGatherNotify::OnDataChange (Deprecated) method</span></span>

<span data-ttu-id="1aa90-108">\[**OnDataChange** peut être modifié ou non disponible dans les versions ultérieures du système d’exploitation ou du produit.\]</span><span class="sxs-lookup"><span data-stu-id="1aa90-108">\[**OnDataChange** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="1aa90-109">Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="1aa90-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="1aa90-110">Cette méthode avertit l’indexeur des données qui ont changé.</span><span class="sxs-lookup"><span data-stu-id="1aa90-110">This method notifies the indexer of data that has changed.</span></span> <span data-ttu-id="1aa90-111">Lorsqu’il envoie la notification à l’indexeur, il comprend le type de modification, l’adresse physique et l’adresse logique.</span><span class="sxs-lookup"><span data-stu-id="1aa90-111">When it sends the notification to the indexer, it includes the type of change, physical address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa90-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1aa90-112">Syntax</span></span>


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="1aa90-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1aa90-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa90-114">*eChangeAdvise* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1aa90-114">*eChangeAdvise* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa90-115">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="1aa90-115">Type: **long**</span></span>

<span data-ttu-id="1aa90-116">Valeur énumérée qui spécifie le type de modification.</span><span class="sxs-lookup"><span data-stu-id="1aa90-116">An enumerated value that specifies the type of change.</span></span>

</dd> <dt>

<span data-ttu-id="1aa90-117">*bstrPhysicalAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1aa90-117">*bstrPhysicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa90-118">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1aa90-118">Type: **BSTR**</span></span>

<span data-ttu-id="1aa90-119">Adresse physique de l’élément qui a changé.</span><span class="sxs-lookup"><span data-stu-id="1aa90-119">The physical address of the item that changed.</span></span>

</dd> <dt>

<span data-ttu-id="1aa90-120">*bstrLogicalAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1aa90-120">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa90-121">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1aa90-121">Type: **BSTR**</span></span>

<span data-ttu-id="1aa90-122">Adresse logique de l’élément qui a changé.</span><span class="sxs-lookup"><span data-stu-id="1aa90-122">The logical address of the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa90-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1aa90-123">Return value</span></span>

<span data-ttu-id="1aa90-124">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1aa90-124">This method does not return a value.</span></span>

 

 
