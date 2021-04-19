---
title: External. attemptLogin, méthode
description: La méthode attemptLogin affiche une boîte de dialogue qui permet à l’utilisateur d’essayer de se connecter au magasin en ligne.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- méthode attemptLogin lecteur Windows Media
- méthode attemptLogin lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode attemptLogin
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536005"
---
# <a name="externalattemptlogin-method"></a><span data-ttu-id="d4465-106">External. attemptLogin, méthode</span><span class="sxs-lookup"><span data-stu-id="d4465-106">External.attemptLogin method</span></span>

<span data-ttu-id="d4465-107">La méthode **attemptLogin** affiche une boîte de dialogue qui permet à l’utilisateur d’essayer de se connecter au magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="d4465-107">The **attemptLogin** method displays a dialog box so the user can attempt to log in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4465-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4465-108">Syntax</span></span>


```JScript
External.attemptLogin()
```



## <a name="parameters"></a><span data-ttu-id="d4465-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4465-109">Parameters</span></span>

<span data-ttu-id="d4465-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d4465-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4465-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4465-111">Return value</span></span>

<span data-ttu-id="d4465-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d4465-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4465-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d4465-113">Remarks</span></span>

<span data-ttu-id="d4465-114">Si la tentative de connexion entraîne une modification de l’état de la connexion, le lecteur Windows Media déclenche l’événement [OnLoginChange](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="d4465-114">If the log-in attempt results in a change of log-in status, Windows Media Player raises the [OnLoginChange](external-onloginchange-event.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4465-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4465-115">Requirements</span></span>



| <span data-ttu-id="d4465-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4465-116">Requirement</span></span> | <span data-ttu-id="d4465-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4465-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4465-118">Version</span><span class="sxs-lookup"><span data-stu-id="d4465-118">Version</span></span><br/> | <span data-ttu-id="d4465-119">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="d4465-119">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="d4465-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d4465-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4465-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4465-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4465-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4465-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4465-123">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="d4465-123">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d4465-124">**External. OnLoginChange, événement**</span><span class="sxs-lookup"><span data-stu-id="d4465-124">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="d4465-125">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="d4465-125">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="d4465-126">**IWMPContentPartner :: login**</span><span class="sxs-lookup"><span data-stu-id="d4465-126">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="d4465-127">**Gestion de la connexion**</span><span class="sxs-lookup"><span data-stu-id="d4465-127">**Managing Login**</span></span>](managing-login.md)
</dt> </dl>

 

 





