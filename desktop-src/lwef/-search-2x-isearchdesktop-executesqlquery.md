---
title: Méthode ISearchDesktop ExecuteSQLQuery
description: Prend un pointeur vers une chaîne qui contient une requête langage SQL (SQL) et ses attributs, et retourne un pointeur vers le jeu retourné.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Méthode ExecuteSQLQuery fonctionnalités d’environnement Windows héritées
- Méthode ExecuteSQLQuery fonctionnalités d’environnement Windows héritées, interface ISearchDesktop
- Fonctionnalités d’environnement Windows héritées de l’interface ISearchDesktop, méthode ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724010"
---
# <a name="isearchdesktopexecutesqlquery-method"></a><span data-ttu-id="be3b2-106">ISearchDesktop :: ExecuteSQLQuery, méthode</span><span class="sxs-lookup"><span data-stu-id="be3b2-106">ISearchDesktop::ExecuteSQLQuery method</span></span>

> [!NOTE]
> <span data-ttu-id="be3b2-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="be3b2-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="be3b2-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="be3b2-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="be3b2-109">Prend un pointeur vers une chaîne qui contient une requête langage SQL (SQL) et ses attributs, et retourne un pointeur vers le jeu retourné.</span><span class="sxs-lookup"><span data-stu-id="be3b2-109">Takes a pointer to a string that contains a Structured Query Language (SQL) query and its attributes and returns a pointer to the return set.</span></span>

## <a name="syntax"></a><span data-ttu-id="be3b2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be3b2-110">Syntax</span></span>


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a><span data-ttu-id="be3b2-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be3b2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be3b2-112">*pdwAttributes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be3b2-112">*pdwAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be3b2-113">Type : **LPCWSTR \***</span><span class="sxs-lookup"><span data-stu-id="be3b2-113">Type: **LPCWSTR\***</span></span>

<span data-ttu-id="be3b2-114">Chaîne qui contient les autres attributs de la requête.</span><span class="sxs-lookup"><span data-stu-id="be3b2-114">A string that contains the other attributes for the query.</span></span>

</dd> <dt>

<span data-ttu-id="be3b2-115">*pwszURL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be3b2-115">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be3b2-116">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="be3b2-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="be3b2-117">Chaîne qui contient la requête SQL.</span><span class="sxs-lookup"><span data-stu-id="be3b2-117">A string that contains the SQL query.</span></span>

</dd> <dt>

<span data-ttu-id="be3b2-118">*ppidUrl* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="be3b2-118">*ppidUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be3b2-119">Type : **ppidUrl \***</span><span class="sxs-lookup"><span data-stu-id="be3b2-119">Type: **ppidUrl\***</span></span>

<span data-ttu-id="be3b2-120">Lorsque cette méthode est retournée avec succès, contient un pointeur vers le Recordset retourné.</span><span class="sxs-lookup"><span data-stu-id="be3b2-120">When this method returns successfully, contains a pointer to the returned recordset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be3b2-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be3b2-121">Return value</span></span>

<span data-ttu-id="be3b2-122">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="be3b2-122">Type: **HRESULT**</span></span>

<span data-ttu-id="be3b2-123">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="be3b2-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be3b2-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be3b2-124">Otherwise, it returns an **HRESULT** error code.</span></span>

 

 




