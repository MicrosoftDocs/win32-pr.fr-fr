---
description: Supprime les informations d’identification de l’utilisateur utilisées pour l’identité connectée.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: DeleteConnectedIdentity, fonction (Indentitystore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033862"
---
# <a name="deleteconnectedidentity-function"></a><span data-ttu-id="57ab5-103">DeleteConnectedIdentity fonction)</span><span class="sxs-lookup"><span data-stu-id="57ab5-103">DeleteConnectedIdentity function</span></span>

<span data-ttu-id="57ab5-104">Supprime les informations d’identification de l’utilisateur utilisées pour l’identité connectée.</span><span class="sxs-lookup"><span data-stu-id="57ab5-104">Deletes the user credential used for the connected identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ab5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57ab5-105">Syntax</span></span>


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a><span data-ttu-id="57ab5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57ab5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ab5-107">*ProviderHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57ab5-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ab5-108">Descripteur de fournisseur d’identité.</span><span class="sxs-lookup"><span data-stu-id="57ab5-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="57ab5-109">*UserToken* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="57ab5-109">*UserToken* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="57ab5-110">Jeton de l’utilisateur connecté dont le compte va être converti en compte local.</span><span class="sxs-lookup"><span data-stu-id="57ab5-110">Token of the connected user whose account is going to be converted to a local account.</span></span> <span data-ttu-id="57ab5-111">Si *userToken* n’a pas la **valeur null**, le fournisseur d’identité utilise ce jeton pour charger le profil utilisateur et nettoyer les États connectés.</span><span class="sxs-lookup"><span data-stu-id="57ab5-111">If *UserToken* is not **NULL**, the identity provider uses this token to load the user profile and clean up connected states.</span></span> <span data-ttu-id="57ab5-112">Si *userToken* a la **valeur null**, LSA force la déconnexion.</span><span class="sxs-lookup"><span data-stu-id="57ab5-112">If *UserToken* is **NULL**, LSA is forcing the disconnection.</span></span> <span data-ttu-id="57ab5-113">Le fournisseur d’identité doit nettoyer tous les États connectés globaux sur cet utilisateur, mais il n’est pas nécessaire que le fournisseur nettoie les États connectés dans le profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57ab5-113">The identity provider should clean up any global connected states on this user, but the provider does not have to clean up connected states in the user profile.</span></span>

</dd> <dt>

<span data-ttu-id="57ab5-114">*UserSid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57ab5-114">*UserSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ab5-115">SID principal de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="57ab5-115">The primary SID of the connected user.</span></span> <span data-ttu-id="57ab5-116">Si *userToken* n’a pas la **valeur null**, ce paramètre est le SID de l’utilisateur du jeton.</span><span class="sxs-lookup"><span data-stu-id="57ab5-116">If *UserToken* is not **NULL**, this parameter is the user SID of the token.</span></span> <span data-ttu-id="57ab5-117">Si *userToken* a la **valeur null**, ce paramètre est utilisé pour identifier l’utilisateur connecté et nettoyer les États connectés globaux de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57ab5-117">If *UserToken* is **NULL**, this parameter is used to identify the connected user and clean up global connected states of that user.</span></span>

</dd> <dt>

<span data-ttu-id="57ab5-118">*IdentityUserName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57ab5-118">*IdentityUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ab5-119">Nom d’utilisateur de l’identité.</span><span class="sxs-lookup"><span data-stu-id="57ab5-119">The user name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ab5-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57ab5-120">Return value</span></span>

<span data-ttu-id="57ab5-121">Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="57ab5-121">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="57ab5-122">Si la fonction échoue, la fonction peut retourner l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="57ab5-122">If the function fails, the function may return one of the following error codes.</span></span>



| <span data-ttu-id="57ab5-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57ab5-123">Return value</span></span>                                                                                               | <span data-ttu-id="57ab5-124">Description</span><span class="sxs-lookup"><span data-stu-id="57ab5-124">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57ab5-125"><dt>paramètre d’état \_ non valide \_</dt></span><span class="sxs-lookup"><span data-stu-id="57ab5-125"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>      | <span data-ttu-id="57ab5-126">Un paramètre n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="57ab5-126">A parameter is not valid.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="57ab5-127"><dt>ÉTAT \_ non de \_ ce type d' \_ utilisateur</dt></span><span class="sxs-lookup"><span data-stu-id="57ab5-127"><dt>STATUS\_NO\_SUCH\_USER</dt></span></span> </dl>          | <span data-ttu-id="57ab5-128">L’utilisateur identifié par *UserSid* n’existe pas, n’est pas connecté actuellement, ou il n’existe aucune identité dont le nom d’utilisateur correspond à *IdentityUserName*.</span><span class="sxs-lookup"><span data-stu-id="57ab5-128">The user identified by *UserSid* does not exist, is not currently connected, or there is no identity whose user name matches *IdentityUserName*.</span></span><br/> |
| <dl> <span data-ttu-id="57ab5-129"><dt>ressources dont l’État est \_ insuffisant \_</dt></span><span class="sxs-lookup"><span data-stu-id="57ab5-129"><dt>STATUS\_INSUFFICIENT\_RESOURCES</dt></span></span> </dl> | <span data-ttu-id="57ab5-130">La mémoire est insuffisante pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="57ab5-130">There is not enough memory to process the request.</span></span><br/>                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="57ab5-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57ab5-131">Requirements</span></span>



| <span data-ttu-id="57ab5-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57ab5-132">Requirement</span></span> | <span data-ttu-id="57ab5-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="57ab5-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ab5-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57ab5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="57ab5-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57ab5-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="57ab5-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57ab5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="57ab5-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57ab5-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57ab5-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="57ab5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="57ab5-139"><dt>Indentitystore. h</dt></span><span class="sxs-lookup"><span data-stu-id="57ab5-139"><dt>Indentitystore.h</dt></span></span> </dl> |



 

 




