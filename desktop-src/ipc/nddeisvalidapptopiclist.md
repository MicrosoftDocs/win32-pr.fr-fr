---
description: Détermine si une application et une chaîne de rubrique (&\# 0034 ; AppName \| thème&\# 0034 ;) utilise la syntaxe appropriée.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: NDdeIsValidAppTopicList, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518877"
---
# <a name="nddeisvalidapptopiclist-function"></a><span data-ttu-id="b19f3-103">NDdeIsValidAppTopicList fonction)</span><span class="sxs-lookup"><span data-stu-id="b19f3-103">NDdeIsValidAppTopicList function</span></span>

<span data-ttu-id="b19f3-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b19f3-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="b19f3-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="b19f3-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="b19f3-106">Détermine si une application et une chaîne de rubrique («*appname* \| *thème*») utilisent la syntaxe appropriée.</span><span class="sxs-lookup"><span data-stu-id="b19f3-106">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="b19f3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b19f3-107">Syntax</span></span>


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a><span data-ttu-id="b19f3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b19f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b19f3-109">*targetTopic* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b19f3-109">*targetTopic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b19f3-110">Pointeur vers l’application et la chaîne de rubrique à valider.</span><span class="sxs-lookup"><span data-stu-id="b19f3-110">A pointer to the application and topic string to validate.</span></span> <span data-ttu-id="b19f3-111">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="b19f3-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b19f3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b19f3-112">Return value</span></span>

<span data-ttu-id="b19f3-113">Si la syntaxe du paramètre *targetTopic* est valide, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="b19f3-113">If the *targetTopic* parameter has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="b19f3-114">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="b19f3-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b19f3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b19f3-115">Remarks</span></span>

<span data-ttu-id="b19f3-116">Cette fonction est également appelée par [**NDdeShareAdd**](nddeshareadd.md) lors de la création du partage DDE.</span><span class="sxs-lookup"><span data-stu-id="b19f3-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="b19f3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b19f3-117">Requirements</span></span>



| <span data-ttu-id="b19f3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b19f3-118">Requirement</span></span> | <span data-ttu-id="b19f3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b19f3-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b19f3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b19f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b19f3-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b19f3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b19f3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b19f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b19f3-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b19f3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b19f3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b19f3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b19f3-125"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b19f3-125"><dt>Nddeapi.h</dt></span></span> </dl>      |
| <span data-ttu-id="b19f3-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b19f3-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b19f3-127"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b19f3-127"><dt>Nddeapi.lib</dt></span></span> </dl>    |
| <span data-ttu-id="b19f3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b19f3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b19f3-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b19f3-129"><dt>Nddeapi.dll</dt></span></span> </dl>    |
| <span data-ttu-id="b19f3-130">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="b19f3-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b19f3-131">**NDdeIsValidAppTopicListW** (Unicode) et **NDdeIsValidAppTopicListA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b19f3-131">**NDdeIsValidAppTopicListW** (Unicode) and **NDdeIsValidAppTopicListA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b19f3-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b19f3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b19f3-133">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="b19f3-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="b19f3-134">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="b19f3-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="b19f3-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="b19f3-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




