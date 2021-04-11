---
title: Propriété ConnectionOptions. Password (WSManDisp. h)
description: Définit le mot de passe d’un compte local ou d’un compte de domaine sur l’ordinateur distant. Cette propriété détermine le mot de passe pour l’authentification.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de propriétés de mot de passe
- Propriété Password Windows Remote Management, objet ConnectionOptions
- Windows Remote Management objet ConnectionOptions, propriété de mot de passe
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104587"
---
# <a name="connectionoptionspassword-property"></a><span data-ttu-id="b7e36-107">ConnectionOptions. Password, propriété</span><span class="sxs-lookup"><span data-stu-id="b7e36-107">ConnectionOptions.Password property</span></span>

<span data-ttu-id="b7e36-108">Définit le mot de passe d’un compte local ou d’un compte de domaine sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="b7e36-108">Sets the password of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="b7e36-109">Cette propriété détermine le mot de passe pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="b7e36-109">This property determines the password for authentication.</span></span> <span data-ttu-id="b7e36-110">Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="b7e36-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="b7e36-111">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b7e36-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e36-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7e36-112">Syntax</span></span>


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a><span data-ttu-id="b7e36-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b7e36-113">Property value</span></span>

<span data-ttu-id="b7e36-114">Chaîne qui contient le mot de passe d’un compte local ou d’un compte de domaine sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="b7e36-114">String that contains the password of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="b7e36-115">Si aucune valeur n’est fournie et que l’indicateur **WSManFlagCredUsernamePassword** n’est pas défini, le mot de passe du compte qui exécute le script est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b7e36-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the password of the account that is running the script is used.</span></span>

<span data-ttu-id="b7e36-116">Si aucune valeur n’est fournie et que l’indicateur **WSManFlagCredUsernamePassword** est défini, le script invite l’utilisateur à entrer le mot de passe (et le nom d’utilisateur, si ce n’est pas fourni).</span><span class="sxs-lookup"><span data-stu-id="b7e36-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the password (and the user name, if this is not supplied).</span></span> <span data-ttu-id="b7e36-117">Si un nom d’utilisateur et un mot de passe valides ne sont pas entrés, une erreur d’accès refusé est retournée.</span><span class="sxs-lookup"><span data-stu-id="b7e36-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e36-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b7e36-118">Remarks</span></span>

<span data-ttu-id="b7e36-119">N’oubliez pas que vous ne pouvez pas récupérer le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="b7e36-119">Be aware that you cannot retrieve the password.</span></span> <span data-ttu-id="b7e36-120">Le mot de passe ne peut être défini qu’avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="b7e36-120">The password can only be set with this property.</span></span>

<span data-ttu-id="b7e36-121">Si vous créez un objet [**ConnectionOptions**](connectionoptions.md) et que vous utilisez un nom d’utilisateur et un mot de passe pour vous connecter à Windows Remote Management, l’indicateur **WSManFlagCredUserNamePassword** doit être défini sur l’appel à [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="b7e36-121">If you create a [**ConnectionOptions**](connectionoptions.md) object and use a user name and password to connect to Windows Remote Management, then the **WSManFlagCredUserNamePassword** flag should be set on the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

<span data-ttu-id="b7e36-122">Pour plus d’informations sur la définition des mots de passe, consultez la section Notes dans [**ConnectionOptions**](connectionoptions.md).</span><span class="sxs-lookup"><span data-stu-id="b7e36-122">For more information about setting passwords, see the Remarks section in [**ConnectionOptions**](connectionoptions.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b7e36-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7e36-123">Examples</span></span>

<span data-ttu-id="b7e36-124">L’exemple de code suivant crée un objet [**ConnectionOptions**](connectionoptions.md) et définit le **mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="b7e36-124">The following code example creates a [**ConnectionOptions**](connectionoptions.md) object and sets the **Password**.</span></span>


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a><span data-ttu-id="b7e36-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7e36-125">Requirements</span></span>



| <span data-ttu-id="b7e36-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7e36-126">Requirement</span></span> | <span data-ttu-id="b7e36-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7e36-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e36-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7e36-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e36-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7e36-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b7e36-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7e36-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e36-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7e36-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b7e36-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7e36-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e36-133"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e36-133"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7e36-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="b7e36-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7e36-135"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7e36-135"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b7e36-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7e36-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7e36-137"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b7e36-137"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b7e36-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e36-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e36-139"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e36-139"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7e36-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7e36-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e36-141">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="b7e36-141">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





