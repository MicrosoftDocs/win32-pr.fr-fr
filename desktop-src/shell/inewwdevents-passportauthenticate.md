---
description: Permet aux pages côté serveur hébergées dans un assistant de vérifier que l’utilisateur a été authentifié par le biais d’un compte Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Méthode NewWDEvents. PassportAuthenticate (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760515"
---
# <a name="newwdeventspassportauthenticate-method"></a><span data-ttu-id="9cdfa-103">Méthode NewWDEvents. PassportAuthenticate</span><span class="sxs-lookup"><span data-stu-id="9cdfa-103">NewWDEvents.PassportAuthenticate method</span></span>

<span data-ttu-id="9cdfa-104">Permet aux pages côté serveur hébergées dans un assistant de vérifier que l’utilisateur a été authentifié par le biais d’un compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9cdfa-104">Enables server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cdfa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9cdfa-105">Syntax</span></span>


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a><span data-ttu-id="9cdfa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9cdfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cdfa-107">*bstrSignInUrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9cdfa-107">*bstrSignInUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cdfa-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="9cdfa-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="9cdfa-109">Chaîne contenant l’URL d’une page Web qui redirige vers l’interface utilisateur de connexion compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9cdfa-109">A string containing the URL of a webpage that redirects to the Microsoft account log on UI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cdfa-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9cdfa-110">Return value</span></span>

<span data-ttu-id="9cdfa-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9cdfa-111">Type: **Boolean**</span></span>

<span data-ttu-id="9cdfa-112">A la valeur **true** si l’authentification est réussie ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="9cdfa-112">Set to **true** if authentication succeeds, **false** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cdfa-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9cdfa-113">Remarks</span></span>

<span data-ttu-id="9cdfa-114">Cette méthode peut être appelée même si un utilisateur est déjà connecté à un compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9cdfa-114">This method may be called even if a user is already logged on to a Microsoft account.</span></span> <span data-ttu-id="9cdfa-115">Dans ce cas, la méthode retourne la **valeur true** sans afficher l’interface utilisateur de connexion compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9cdfa-115">In that case, the method returns **true** without displaying the Microsoft account log on UI.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cdfa-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9cdfa-116">Requirements</span></span>



| <span data-ttu-id="9cdfa-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9cdfa-117">Requirement</span></span> | <span data-ttu-id="9cdfa-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9cdfa-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cdfa-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cdfa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9cdfa-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9cdfa-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="9cdfa-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cdfa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9cdfa-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9cdfa-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9cdfa-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9cdfa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cdfa-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cdfa-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9cdfa-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="9cdfa-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9cdfa-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9cdfa-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9cdfa-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9cdfa-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cdfa-128"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="9cdfa-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
