---
title: External. userLoggedIn
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. userLoggedIn
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- External. userLoggedIn Windows Media Player
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532645"
---
# <a name="externaluserloggedin"></a><span data-ttu-id="b4ffc-105">External. userLoggedIn</span><span class="sxs-lookup"><span data-stu-id="b4ffc-105">External.userLoggedIn</span></span>

> [!Note]  
> <span data-ttu-id="b4ffc-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b4ffc-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b4ffc-108">La propriété **userLoggedIn** récupère une valeur indiquant si l’utilisateur est connecté au magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-108">The **userLoggedIn** property retrieves a value indicating whether the user is logged in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ffc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4ffc-109">Syntax</span></span>

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a><span data-ttu-id="b4ffc-110">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b4ffc-110">Possible Values</span></span>

<span data-ttu-id="b4ffc-111">Cette propriété est une **valeur booléenne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="b4ffc-112">La **valeur true** indique que l’utilisateur est connecté, et **false** indique que l’utilisateur a ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-112">**TRUE** indicates that the user is logged in, and **FALSE** indicates that the user is logged out.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4ffc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4ffc-113">Requirements</span></span>



| <span data-ttu-id="b4ffc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4ffc-114">Requirement</span></span> | <span data-ttu-id="b4ffc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4ffc-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ffc-116">Version</span><span class="sxs-lookup"><span data-stu-id="b4ffc-116">Version</span></span><br/> | <span data-ttu-id="b4ffc-117">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-117">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="b4ffc-118">DLL</span><span class="sxs-lookup"><span data-stu-id="b4ffc-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="b4ffc-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4ffc-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4ffc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4ffc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ffc-121">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="b4ffc-121">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b4ffc-122">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="b4ffc-122">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="b4ffc-123">**External. OnLoginChange, événement**</span><span class="sxs-lookup"><span data-stu-id="b4ffc-123">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> </dl>

 

 





