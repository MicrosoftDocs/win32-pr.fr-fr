---
title: External. accountType
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété accountType récupère le type de compte de l’utilisateur actuel.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- External. accountType Windows Media Player
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545556"
---
# <a name="externalaccounttype"></a><span data-ttu-id="709c3-106">External. accountType</span><span class="sxs-lookup"><span data-stu-id="709c3-106">External.accountType</span></span>

> [!Note]  
> <span data-ttu-id="709c3-107">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="709c3-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="709c3-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="709c3-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="709c3-109">La propriété **AccountType** récupère le type de compte de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="709c3-109">The **accountType** property retrieves the account type of the current user.</span></span>

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a><span data-ttu-id="709c3-110">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="709c3-110">Possible Values</span></span>

<span data-ttu-id="709c3-111">Cette propriété est une **chaîne** en lecture seule qui représente le type de compte.</span><span class="sxs-lookup"><span data-stu-id="709c3-111">This property is a read-only **String** that represents the account type.</span></span> <span data-ttu-id="709c3-112">Les chaînes qui représentent différents types de compte sont définies par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="709c3-112">Strings that represent various account types are defined by the online store.</span></span>

## <a name="remarks"></a><span data-ttu-id="709c3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="709c3-113">Remarks</span></span>

<span data-ttu-id="709c3-114">Cette propriété récupère le type de compte en appelant la méthode [IWMPContentPartner :: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) , qui est implémentée par le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="709c3-114">This property retrieves the account type by calling the [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="709c3-115">Si l’utilisateur actuel est connecté au magasin en ligne ou si le plug-in a mis en cache les informations d’identification de l’utilisateur, la méthode **getContentPartnerInfo** peut déterminer le type de compte de l’utilisateur et le renvoyer au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="709c3-115">If the current user is logged in to the online store or the plug-in has cached the user's credentials, the **getContentPartnerInfo** method can determine the user's account type and return it to Windows Media Player.</span></span> <span data-ttu-id="709c3-116">Le type de compte est une chaîne que le lecteur Windows Media n’interprète pas.</span><span class="sxs-lookup"><span data-stu-id="709c3-116">The account type is a string that Windows Media Player does not interpret.</span></span> <span data-ttu-id="709c3-117">Au lieu de cela, le lecteur Windows Media transmet la chaîne du plug-in du magasin en ligne au script sur la page de découverte du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="709c3-117">Rather, Windows Media Player passes the string from the online store's plug-in to the script on the online store's discovery page.</span></span>

<span data-ttu-id="709c3-118">Si l’utilisateur actuel n’est pas connecté au magasin en ligne et que le plug-in de la boutique en ligne ne dispose pas d’informations d’identification mises en cache pour l’utilisateur, cette propriété récupère toute chaîne renvoyée par la méthode **getContentPartnerInfo** dans cette situation.</span><span class="sxs-lookup"><span data-stu-id="709c3-118">If the current user is not logged in to the online store and the online store's plug-in does not have cached credentials for the user, this property retrieves whatever string the **getContentPartnerInfo** method returns in that situation.</span></span>

## <a name="requirements"></a><span data-ttu-id="709c3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="709c3-119">Requirements</span></span>



| <span data-ttu-id="709c3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="709c3-120">Requirement</span></span> | <span data-ttu-id="709c3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="709c3-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="709c3-122">Version</span><span class="sxs-lookup"><span data-stu-id="709c3-122">Version</span></span><br/> | <span data-ttu-id="709c3-123">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="709c3-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="709c3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="709c3-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="709c3-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="709c3-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="709c3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="709c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709c3-127">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="709c3-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="709c3-128">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="709c3-128">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





