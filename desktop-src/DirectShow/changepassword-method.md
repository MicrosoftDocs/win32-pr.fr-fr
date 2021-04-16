---
description: La méthode DVDAdm. ChangePassword enregistre un nouveau mot de passe d’application dans le registre.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword, méthode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481032"
---
# <a name="changepassword-method"></a><span data-ttu-id="4ee3b-103">ChangePassword, méthode</span><span class="sxs-lookup"><span data-stu-id="4ee3b-103">ChangePassword Method</span></span>

> [!Note]  
> <span data-ttu-id="4ee3b-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4ee3b-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4ee3b-106">La `DVDAdm.ChangePassword` méthode enregistre un nouveau mot de passe d’application dans le registre.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-106">The `DVDAdm.ChangePassword` method saves a new application password in the registry.</span></span>

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a><span data-ttu-id="4ee3b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ee3b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee3b-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="4ee3b-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="4ee3b-109">Spécifie le nom d’ouverture de session de l’utilisateur actuel en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-109">Specifies the current user's logon name as a String.</span></span> <span data-ttu-id="4ee3b-110">L’objet MSDVDAdm ignore ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-110">The MSDVDAdm object ignores this parameter.</span></span> <span data-ttu-id="4ee3b-111">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4ee3b-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Vendus*</span><span class="sxs-lookup"><span data-stu-id="4ee3b-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*sOld*</span></span>
</dt> <dd>

<span data-ttu-id="4ee3b-113">Spécifie l’ancien mot de passe de l’utilisateur sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-113">Specifies the user's old password as a String.</span></span>

</dd> <dt>

<span data-ttu-id="4ee3b-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span><span class="sxs-lookup"><span data-stu-id="4ee3b-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span></span>
</dt> <dd>

<span data-ttu-id="4ee3b-115">Spécifie le nouveau mot de passe de l’utilisateur sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-115">Specifies the user's new password as a String.</span></span> <span data-ttu-id="4ee3b-116">ne peut pas être une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-116">Cannot be an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ee3b-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4ee3b-117">Return Value</span></span>

<span data-ttu-id="4ee3b-118">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee3b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4ee3b-119">Remarks</span></span>

<span data-ttu-id="4ee3b-120">Actuellement, le paramètre *sUserName* est ignoré sur cette et toutes les méthodes associées.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-120">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span> <span data-ttu-id="4ee3b-121">Cela signifie que toute personne connaissant le mot de passe peut définir le niveau parental.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-121">This means that whoever knows the password can set the parental level.</span></span> <span data-ttu-id="4ee3b-122">Il n’existe qu’un seul mot de passe et un seul niveau parental pour l’application.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-122">There is only one password and one parental level for the application.</span></span> <span data-ttu-id="4ee3b-123">Il n’existe aucune prise en charge pour les noms d’ouverture de session des utilisateurs individuels ou la gestion de plusieurs mots de passe.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-123">There is no support for individual user logon names or multiple password management.</span></span> <span data-ttu-id="4ee3b-124">Pour appliquer des niveaux de gestion parental, les parents doivent définir le mot de passe, puis définir le niveau parental approprié pour les jeunes membres du groupe de parents.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-124">To enforce parental management levels, parents should set the password and then set the parental level appropriate for younger members of the group of relatives.</span></span> <span data-ttu-id="4ee3b-125">Lorsque les parents souhaitent afficher un disque avec un contenu classé pour adultes, ils peuvent modifier le niveau, puis le modifier à la fin de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-125">When parents want to view a disc with adult-rated content, they can change the level, and then change it back when they are done viewing.</span></span> <span data-ttu-id="4ee3b-126">Tant que les enfants ne connaissent pas le mot de passe, ils peuvent uniquement regarder le contenu au niveau ou au-dessous du niveau défini pour eux.</span><span class="sxs-lookup"><span data-stu-id="4ee3b-126">As long as the children do not know the password, they can only watch content at or below the level set for them.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ee3b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ee3b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee3b-128">**ConfirmPassword**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-128">**ConfirmPassword**</span></span>](confirmpassword-method.md)
</dt> <dt>

[<span data-ttu-id="4ee3b-129">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="4ee3b-129">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



