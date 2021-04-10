---
title: Propriété ConnectionOptions. UserName (WSManDisp. h)
description: Définit et obtient le nom d’utilisateur d’un compte local ou d’un compte de domaine sur l’ordinateur distant. Cette propriété détermine le nom d’utilisateur pour l’authentification.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Propriété UserName Windows Remote Management
- Propriété UserName Windows Remote Management, objet ConnectionOptions
- Objet ConnectionOptions Windows Remote Management, propriété UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104584"
---
# <a name="connectionoptionsusername-property"></a><span data-ttu-id="dc742-107">ConnectionOptions. UserName, propriété</span><span class="sxs-lookup"><span data-stu-id="dc742-107">ConnectionOptions.UserName property</span></span>

<span data-ttu-id="dc742-108">Définit et obtient le nom d’utilisateur d’un compte local ou d’un compte de domaine sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="dc742-108">Sets and gets the user name of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="dc742-109">Cette propriété détermine le nom d’utilisateur pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="dc742-109">This property determines the user name for authentication.</span></span> <span data-ttu-id="dc742-110">Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="dc742-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="dc742-111">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="dc742-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc742-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc742-112">Syntax</span></span>


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a><span data-ttu-id="dc742-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="dc742-113">Property value</span></span>

<span data-ttu-id="dc742-114">Chaîne qui contient le nom d’utilisateur d’un compte local ou d’un compte de domaine sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="dc742-114">String that contains the user name of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="dc742-115">Si aucune valeur n’est fournie et que l’indicateur **WSManFlagCredUsernamePassword** n’est pas défini, le nom d’utilisateur du compte qui exécute le script est utilisé.</span><span class="sxs-lookup"><span data-stu-id="dc742-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the user name of the account that is running the script is used.</span></span>

<span data-ttu-id="dc742-116">Si aucune valeur n’est fournie et que l’indicateur **WSManFlagCredUsernamePassword** est défini, le script invite l’utilisateur à entrer le nom d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="dc742-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the user name and password.</span></span> <span data-ttu-id="dc742-117">Si un nom d’utilisateur et un mot de passe valides ne sont pas entrés, une erreur d’accès refusé est retournée.</span><span class="sxs-lookup"><span data-stu-id="dc742-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc742-118">Notes</span><span class="sxs-lookup"><span data-stu-id="dc742-118">Remarks</span></span>

<span data-ttu-id="dc742-119">La syntaxe suivante est utilisée pour spécifier cette propriété.</span><span class="sxs-lookup"><span data-stu-id="dc742-119">The following syntax is used to specify this property.</span></span>


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



<span data-ttu-id="dc742-120">Vous pouvez fournir le **nom d’utilisateur** et le [**mot de passe**](connectionoptions-password.md) d’un compte de domaine lors de l’utilisation de l’authentification [*Negotiate*](windows-remote-management-glossary.md) ou *Kerberos* , ou pour un compte local avec l’authentification de [*base*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="dc742-120">You can supply **UserName** and [**Password**](connectionoptions-password.md) for a domain account when using [*negotiate*](windows-remote-management-glossary.md) or *Kerberos* authentication, or for a local account with [*Basic*](windows-remote-management-glossary.md) authentication.</span></span> <span data-ttu-id="dc742-121">Pour se connecter à un compte local, les indicateurs [**WSMan. CreateSession**](wsman-createsession.md) doivent contenir la combinaison de l’indicateur **WSManFlagUseBasic** et de l’indicateur **WsmanFlagCredUserNamePassword** .</span><span class="sxs-lookup"><span data-stu-id="dc742-121">To connect to a local account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseBasic** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="dc742-122">Pour vous connecter à un compte de domaine, les indicateurs **WSMan. CreateSession** doivent contenir la combinaison de l’indicateur **WSManFlagUseNegotiate** et de l’indicateur **WsmanFlagCredUserNamePassword** , ou bien la combinaison de l’indicateur **WSManFlagUseKerberos** et de l’indicateur **WsmanFlagCredUserNamePassword** .</span><span class="sxs-lookup"><span data-stu-id="dc742-122">To connect to a domain account, the **WSMan.CreateSession** flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag, or the combination of the **WSManFlagUseKerberos** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="dc742-123">Pour un compte de domaine, le nom **d’utilisateur** doit être spécifié sous la forme « nom \\ d’utilisateur de l’ordinateur », où la partie « ordinateur » de la chaîne peut être le nom ou l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="dc742-123">For a domain account, **UserName** must be specified in the form "computer\\username", where the "computer" part of the string can be either the name or the IP address.</span></span> <span data-ttu-id="dc742-124">Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="dc742-124">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



<span data-ttu-id="dc742-125">Pour la connexion à un compte de domaine, les indicateurs [**WSMan. CreateSession**](wsman-createsession.md) doivent contenir la combinaison de l’indicateur **WSManFlagUseNegotiate** et de l’indicateur **WsmanFlagCredUserNamePassword** pour la connexion à un compte de domaine, qui requiert l’authentification par négociation.</span><span class="sxs-lookup"><span data-stu-id="dc742-125">For connecting to a domain account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag for connecting to a domain account, which requires Negotiate authentication.</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



## <a name="requirements"></a><span data-ttu-id="dc742-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc742-126">Requirements</span></span>



| <span data-ttu-id="dc742-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc742-127">Requirement</span></span> | <span data-ttu-id="dc742-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc742-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc742-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc742-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dc742-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc742-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="dc742-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc742-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dc742-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc742-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="dc742-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc742-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc742-134"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc742-134"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc742-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="dc742-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc742-136"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc742-136"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="dc742-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dc742-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc742-138"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc742-138"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc742-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dc742-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc742-140"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc742-140"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc742-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc742-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc742-142">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="dc742-142">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





