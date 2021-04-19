---
title: IGatherNotify init (déconseillé), méthode
description: Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | IGatherNotify init (déconseillé), méthode
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Méthode Init (déconseillée) fonctionnalités héritées de l’environnement Windows
- Méthode Init (obsolète) fonctionnalités héritées de l’environnement Windows, interface IGatherNotify
- Interface IGatherNotify fonctionnalités d’environnement Windows héritées, méthode Init (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538046"
---
# <a name="igathernotifyinit-deprecated-method"></a><span data-ttu-id="c903a-107">IGatherNotify :: init (déconseillé), méthode</span><span class="sxs-lookup"><span data-stu-id="c903a-107">IGatherNotify::Init (Deprecated) method</span></span>

<span data-ttu-id="c903a-108">\[**Init** peut être modifié ou non disponible dans les versions ultérieures du système d’exploitation ou du produit.\]</span><span class="sxs-lookup"><span data-stu-id="c903a-108">\[**Init** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="c903a-109">Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c903a-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="c903a-110">Initialise l’interface du Rassembleur.</span><span class="sxs-lookup"><span data-stu-id="c903a-110">Initializes the Gatherer interface.</span></span> <span data-ttu-id="c903a-111">Spécifie également l’index à notifier et le magasin d’applications à surveiller.</span><span class="sxs-lookup"><span data-stu-id="c903a-111">Also specifies the index to notify and the application store to monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c903a-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c903a-112">Syntax</span></span>


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a><span data-ttu-id="c903a-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c903a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c903a-114">*bstrApplication* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c903a-114">*bstrApplication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c903a-115">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c903a-115">Type: **BSTR**</span></span>

<span data-ttu-id="c903a-116">Chaîne qui spécifie l’application cible.</span><span class="sxs-lookup"><span data-stu-id="c903a-116">A string that specifies the target application.</span></span>

</dd> <dt>

<span data-ttu-id="c903a-117">*bstrProject* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c903a-117">*bstrProject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c903a-118">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c903a-118">Type: **BSTR**</span></span>

<span data-ttu-id="c903a-119">Chaîne qui spécifie le nom de l’indexeur auquel transmettre les informations du Rassembleur.</span><span class="sxs-lookup"><span data-stu-id="c903a-119">A string that specifies the name of the indexer to pass gatherer information to.</span></span>

</dd> <dt>

<span data-ttu-id="c903a-120">*varScopesBstrArray* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c903a-120">*varScopesBstrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c903a-121">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="c903a-121">Type: **variant**</span></span>

<span data-ttu-id="c903a-122">Paramètre facultatif qui vous permet de passer un tableau d’étendues à initialiser.</span><span class="sxs-lookup"><span data-stu-id="c903a-122">Optional parameter, that enables you to pass an array of scopes to be initialized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c903a-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c903a-123">Return value</span></span>

<span data-ttu-id="c903a-124">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c903a-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c903a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c903a-125">Remarks</span></span>

<span data-ttu-id="c903a-126">Initialize with application = "RSApp", Project = "MyIndex".</span><span class="sxs-lookup"><span data-stu-id="c903a-126">Initialize with application="RSApp", Project="MyIndex".</span></span>

 

 
