---
description: La méthode DVDAdm. ConfirmPassword teste si le mot de passe spécifié correspond au mot de passe enregistré précédemment.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Méthode ConfirmPassword (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526111"
---
# <a name="confirmpassword-method"></a><span data-ttu-id="ca9d6-103">Méthode ConfirmPassword</span><span class="sxs-lookup"><span data-stu-id="ca9d6-103">ConfirmPassword Method</span></span>

> [!Note]  
> <span data-ttu-id="ca9d6-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ca9d6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ca9d6-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ca9d6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ca9d6-106">La `DVDAdm.ConfirmPassword` méthode teste si le mot de passe spécifié correspond au mot de passe enregistré précédemment.</span><span class="sxs-lookup"><span data-stu-id="ca9d6-106">The `DVDAdm.ConfirmPassword` method tests whether the specified password matches the previously saved password.</span></span>

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="ca9d6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca9d6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca9d6-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="ca9d6-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="ca9d6-109">Spécifie le nom de l’utilisateur sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="ca9d6-109">Specifies the user's name as a String.</span></span>

</dd> <dt>

<span data-ttu-id="ca9d6-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="ca9d6-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="ca9d6-111">Spécifie le nouveau mot de passe sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="ca9d6-111">Specifies the new password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca9d6-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ca9d6-112">Return Value</span></span>

<span data-ttu-id="ca9d6-113">Retourne la valeur true si le mot de passe spécifié correspond au mot de passe existant, false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ca9d6-113">Returns true if the specified password matches the existing password, false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca9d6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ca9d6-114">Remarks</span></span>

<span data-ttu-id="ca9d6-115">Actuellement, le paramètre *sUserName* est ignoré sur cette et toutes les méthodes associées.</span><span class="sxs-lookup"><span data-stu-id="ca9d6-115">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca9d6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca9d6-116">Requirements</span></span>



| <span data-ttu-id="ca9d6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca9d6-117">Requirement</span></span> | <span data-ttu-id="ca9d6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca9d6-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca9d6-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca9d6-119">Header</span></span><br/> | <dl> <span data-ttu-id="ca9d6-120"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca9d6-120"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca9d6-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca9d6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca9d6-122">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="ca9d6-122">**ChangePassword**</span></span>](changepassword-method.md)
</dt> <dt>

[<span data-ttu-id="ca9d6-123">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="ca9d6-123">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




