---
title: External. Authenticate, méthode
description: La méthode Authenticate lance une tentative d’authentification de l’utilisateur.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- méthode d’authentification du lecteur Windows Media
- méthode Authenticate lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode Authenticate
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525265"
---
# <a name="externalauthenticate-method"></a><span data-ttu-id="8b77b-106">External. Authenticate, méthode</span><span class="sxs-lookup"><span data-stu-id="8b77b-106">External.authenticate method</span></span>

<span data-ttu-id="8b77b-107">La méthode **Authenticate** lance une tentative d’authentification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8b77b-107">The **authenticate** method initiates an attempt to authenticate the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b77b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b77b-108">Syntax</span></span>


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a><span data-ttu-id="8b77b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b77b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b77b-110">*AuthenticationIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b77b-110">*AuthenticationIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b77b-111">**Nombre** (**long**) qui spécifie l’index d’une page Web d’authentification-réussite.</span><span class="sxs-lookup"><span data-stu-id="8b77b-111">**Number** (**long**) that specifies the index of an authentication-success webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b77b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b77b-112">Return value</span></span>

<span data-ttu-id="8b77b-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8b77b-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b77b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8b77b-114">Remarks</span></span>

<span data-ttu-id="8b77b-115">Certains liens sur une page de découverte ont des cibles qui ne doivent être affichées qu’une fois que l’utilisateur a été authentifié.</span><span class="sxs-lookup"><span data-stu-id="8b77b-115">Certain links on a discovery page have targets that should be displayed only after the user has been authenticated.</span></span> <span data-ttu-id="8b77b-116">La page détection, le lecteur Windows Media et le plug-in de la boutique en ligne utilisent les étapes suivantes pour authentifier l’utilisateur et afficher la page Web cible :</span><span class="sxs-lookup"><span data-stu-id="8b77b-116">The discovery page, Windows Media Player, and the online store's plug-in use the following steps to authenticate the user and display the target webpage:</span></span>

1.  <span data-ttu-id="8b77b-117">Un script sur une page de découverte appelle le *externe*. méthode **Authenticate** .</span><span class="sxs-lookup"><span data-stu-id="8b77b-117">Script on a discovery page calls the *External*.**authenticate** method.</span></span>
2.  <span data-ttu-id="8b77b-118">Le lecteur Windows Media affiche une boîte de dialogue pour obtenir un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="8b77b-118">Windows Media Player displays a dialog box to obtain a user name and password.</span></span>
3.  <span data-ttu-id="8b77b-119">Le lecteur Windows Media appelle [IWMPContentPartner :: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), qui lance la tentative d’authentification et retourne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="8b77b-119">Windows Media Player calls [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), which initiates the authentication attempt and returns immediately.</span></span>
4.  <span data-ttu-id="8b77b-120">Lorsque la tentative d’authentification est terminée, le plug-in du magasin en ligne appelle [IWMPContentPartnerCallback :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), en passant wmpcnAuthResult et une valeur booléenne qui indique si la tentative a réussi.</span><span class="sxs-lookup"><span data-stu-id="8b77b-120">When the authentication attempt is complete, the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnAuthResult and a Boolean value that indicates whether the attempt was successful.</span></span>
5.  <span data-ttu-id="8b77b-121">Si la tentative d’authentification a réussi, le lecteur Windows Media appelle [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), en passant g \_ szItemInfo \_ AuthenticationSuccessURL, pour obtenir l’URL d’une page Web d’authentification-réussite.</span><span class="sxs-lookup"><span data-stu-id="8b77b-121">If the authentication attempt was successful, Windows Media Player calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_AuthenticationSuccessURL, to obtain the URL of an authentication-success webpage.</span></span> <span data-ttu-id="8b77b-122">Dans cet appel, le lecteur Windows Media transmet le même index que la page de découverte transmise à l' *externe*. méthode **Authenticate** .</span><span class="sxs-lookup"><span data-stu-id="8b77b-122">In this call, Windows Media Player passes the same index that the discovery page passed to the *External*.**authenticate** method.</span></span>
6.  <span data-ttu-id="8b77b-123">Le lecteur Windows Media affiche la page Web authentification-réussite.</span><span class="sxs-lookup"><span data-stu-id="8b77b-123">Windows Media Player displays the authentication-success webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b77b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b77b-124">Requirements</span></span>



| <span data-ttu-id="8b77b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b77b-125">Requirement</span></span> | <span data-ttu-id="8b77b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b77b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b77b-127">Version</span><span class="sxs-lookup"><span data-stu-id="8b77b-127">Version</span></span><br/> | <span data-ttu-id="8b77b-128">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="8b77b-128">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="8b77b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8b77b-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="8b77b-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b77b-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b77b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b77b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b77b-132">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="8b77b-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8b77b-133">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="8b77b-133">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="8b77b-134">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="8b77b-134">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





