---
title: Méthode IGatherNotify paramètre addscope (déconseillée)
description: Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | Méthode IGatherNotify paramètre addscope (déconseillée)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Méthode paramètre addscope (déconseillée) fonctionnalités héritées de l’environnement Windows
- Méthode paramètre addscope (déconseillée) fonctionnalités d’environnement Windows héritées, interface IGatherNotify
- Interface IGatherNotify fonctionnalités d’environnement Windows héritées, méthode paramètre addscope (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322181"
---
# <a name="igathernotifyaddscope-deprecated-method"></a><span data-ttu-id="26415-107">IGatherNotify :: paramètre addscope (méthode déconseillée)</span><span class="sxs-lookup"><span data-stu-id="26415-107">IGatherNotify::AddScope (Deprecated) method</span></span>

<span data-ttu-id="26415-108">\[Les **paramètre addscope** peuvent être modifiés ou non disponibles dans les versions ultérieures du système d’exploitation ou du produit.\]</span><span class="sxs-lookup"><span data-stu-id="26415-108">\[**AddScope** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="26415-109">Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="26415-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="26415-110">Ajoute la page de démarrage ou l’URL que vous analysez.</span><span class="sxs-lookup"><span data-stu-id="26415-110">Adds the start page or URL you are monitoring.</span></span> <span data-ttu-id="26415-111">Cela lance une analyse incrémentielle lorsque vous vous connectez, puis suppose que toutes les autres modifications d’URL sont effectuées par notification.</span><span class="sxs-lookup"><span data-stu-id="26415-111">This initiates an incremental crawl when you connect, and then assumes all further URL changes are by notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="26415-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26415-112">Syntax</span></span>


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a><span data-ttu-id="26415-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26415-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26415-114">*bstrScope* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26415-114">*bstrScope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26415-115">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="26415-115">Type: **BSTR**</span></span>

<span data-ttu-id="26415-116">Chaîne qui spécifie la page de démarrage ou URLthat que vous analysez.</span><span class="sxs-lookup"><span data-stu-id="26415-116">A string that specifies the start page or URLthat you are monitoring.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26415-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26415-117">Return value</span></span>

<span data-ttu-id="26415-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="26415-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26415-119">Notes</span><span class="sxs-lookup"><span data-stu-id="26415-119">Remarks</span></span>

<span data-ttu-id="26415-120">L’appel de cette méthode démarre une analyse incrémentielle lorsqu’elle est connectée au magasin.</span><span class="sxs-lookup"><span data-stu-id="26415-120">Calling this method starts an incremental crawl when connected to the store.</span></span> <span data-ttu-id="26415-121">Par la suite, il est supposé que toutes les modifications d’URL sont effectuées par notification après la mise à jour initiale.</span><span class="sxs-lookup"><span data-stu-id="26415-121">Thereafter, it is assumed that all URL changes are by notification after the initial update.</span></span>

 

 
