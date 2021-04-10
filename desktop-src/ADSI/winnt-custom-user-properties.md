---
title: Propriétés de l’utilisateur personnalisé Winnt
description: Le fournisseur Winnt met à disposition les propriétés personnalisées suivantes pour la classe utilisateur. Elles sont accessibles par le biais des méthodes IADs. obten et IADs. put. Pour plus d’informations, consultez la \_ structure User info \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Propriétés de l’utilisateur personnalisé Winnt ADSI
- Fournisseur WinNT ADSI, objet utilisateur, propriétés personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941367"
---
# <a name="winnt-custom-user-properties"></a><span data-ttu-id="f966a-107">Propriétés de l’utilisateur personnalisé Winnt</span><span class="sxs-lookup"><span data-stu-id="f966a-107">WinNT Custom User Properties</span></span>

<span data-ttu-id="f966a-108">Le fournisseur Winnt met à disposition les propriétés personnalisées suivantes pour la classe utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f966a-108">The WinNT provider makes available the following custom properties for the User class.</span></span> <span data-ttu-id="f966a-109">Elles sont accessibles par le biais des méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="f966a-109">They may be accessed through the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) methods.</span></span> <span data-ttu-id="f966a-110">Pour plus d’informations, consultez la structure [**User \_ info \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) .</span><span class="sxs-lookup"><span data-stu-id="f966a-110">For more information, see the [**USER\_INFO\_3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) structure.</span></span>



| <span data-ttu-id="f966a-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="f966a-111">Property</span></span>            | <span data-ttu-id="f966a-112">Type</span><span class="sxs-lookup"><span data-stu-id="f966a-112">Type</span></span>         | <span data-ttu-id="f966a-113">Description</span><span class="sxs-lookup"><span data-stu-id="f966a-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f966a-114">**HomeDirDrive**</span><span class="sxs-lookup"><span data-stu-id="f966a-114">**HomeDirDrive**</span></span>    | <span data-ttu-id="f966a-115">String</span><span class="sxs-lookup"><span data-stu-id="f966a-115">String</span></span>       | <span data-ttu-id="f966a-116">Lecteur du répertoire de démarrage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f966a-116">Home Directory Drive of the user.</span></span> <span data-ttu-id="f966a-117">Pointeur vers une chaîne Unicode qui spécifie le chemin d’accès du répertoire de départ.</span><span class="sxs-lookup"><span data-stu-id="f966a-117">This is a pointer to a Unicode string that specifies the path of the home directory.</span></span> <span data-ttu-id="f966a-118">La chaîne peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="f966a-118">The string can be **null**.</span></span> <span data-ttu-id="f966a-119">Consultez l’exemple de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f966a-119">See example in this topic.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="f966a-120">**ObjectSID**</span><span class="sxs-lookup"><span data-stu-id="f966a-120">**ObjectSID**</span></span>       | <span data-ttu-id="f966a-121">Chaîne d’octets</span><span class="sxs-lookup"><span data-stu-id="f966a-121">Octet String</span></span> | <span data-ttu-id="f966a-122">SID de l’objet de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f966a-122">Object SID of the user.</span></span> <span data-ttu-id="f966a-123">Pour obtenir un exemple de récupération du SID de l’objet à l’aide du fournisseur WinNT, consultez [SID d’objet (fournisseur WinNT)](object-sid.md) .</span><span class="sxs-lookup"><span data-stu-id="f966a-123">For an example of how to retrieve the Object SID using the WinNT Provider, see [Object SID (WinNT Provider)](object-sid.md)</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="f966a-124">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="f966a-124">**Parameters**</span></span>      | <span data-ttu-id="f966a-125">String</span><span class="sxs-lookup"><span data-stu-id="f966a-125">String</span></span>       | <span data-ttu-id="f966a-126">Paramètres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f966a-126">Parameters of the user.</span></span> <span data-ttu-id="f966a-127">Pointe vers une chaîne Unicode qui est réservée à une utilisation par des applications.</span><span class="sxs-lookup"><span data-stu-id="f966a-127">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="f966a-128">Cette chaîne peut être une chaîne NULL, ou elle peut contenir un nombre quelconque de caractères avant le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="f966a-128">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="f966a-129">Les produits Microsoft utilisent ce membre pour stocker les données de configuration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f966a-129">Microsoft products use this member to store user configuration data.</span></span> <span data-ttu-id="f966a-130">Cette propriété ne peut être modifiée que par une application au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="f966a-130">This property can only be modified by an application during installation.</span></span> |
| <span data-ttu-id="f966a-131">**Mot de passe**</span><span class="sxs-lookup"><span data-stu-id="f966a-131">**PasswordAge**</span></span>     | <span data-ttu-id="f966a-132">Temps</span><span class="sxs-lookup"><span data-stu-id="f966a-132">Time</span></span>         | <span data-ttu-id="f966a-133">Durée d’utilisation du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f966a-133">Time duration of the password in use.</span></span> <span data-ttu-id="f966a-134">Cette propriété indique le nombre de secondes qui se sont écoulées depuis la dernière modification du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f966a-134">This property indicates the number of seconds that have elapsed since the password was last changed.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="f966a-135">**PasswordExpired**</span><span class="sxs-lookup"><span data-stu-id="f966a-135">**PasswordExpired**</span></span> | <span data-ttu-id="f966a-136">Integer</span><span class="sxs-lookup"><span data-stu-id="f966a-136">Integer</span></span>      | <span data-ttu-id="f966a-137">Indique quand le mot de passe a expiré.</span><span class="sxs-lookup"><span data-stu-id="f966a-137">Tells when the password was expired.</span></span> <span data-ttu-id="f966a-138">Quand vous utilisez l’opération obtenir, la valeur zéro est retournée si le mot de passe n’a pas expiré, ou une valeur différente de zéro si elle a expiré.</span><span class="sxs-lookup"><span data-stu-id="f966a-138">When you use Get, it will return zero is the password has not expired, or nonzero if it has expired.</span></span> <span data-ttu-id="f966a-139">Consultez l’exemple de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f966a-139">See example in this topic.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="f966a-140">**PrimaryGroupID**</span><span class="sxs-lookup"><span data-stu-id="f966a-140">**PrimaryGroupID**</span></span>  | <span data-ttu-id="f966a-141">Integer</span><span class="sxs-lookup"><span data-stu-id="f966a-141">Integer</span></span>      | <span data-ttu-id="f966a-142">ID de groupe principal de l’utilisateur, par exemple, l’ID de groupe d’utilisateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="f966a-142">User's primary group ID, for example, domain user group ID.</span></span> <span data-ttu-id="f966a-143">Consultez l’exemple de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f966a-143">See example in this topic.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f966a-144">**UserFlags**</span><span class="sxs-lookup"><span data-stu-id="f966a-144">**UserFlags**</span></span>       | <span data-ttu-id="f966a-145">Integer</span><span class="sxs-lookup"><span data-stu-id="f966a-145">Integer</span></span>      | <span data-ttu-id="f966a-146">Indicateur utilisateur défini dans [**l' \_ \_ \_ énumération de l’indicateur utilisateur ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span><span class="sxs-lookup"><span data-stu-id="f966a-146">User Flag defined in [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span></span> <span data-ttu-id="f966a-147">Pour obtenir un exemple d’utilisation de UserFlags, consultez [mot de passe n’expire jamais (fournisseur WinNT)](winnt-password-never-expires.md) .</span><span class="sxs-lookup"><span data-stu-id="f966a-147">For an example of how to use UserFlags, see [Password Never Expires (WinNT Provider)](winnt-password-never-expires.md)</span></span>                                                                                                                                                             |



 

<span data-ttu-id="f966a-148">Cet exemple montre comment définir le répertoire du lecteur de démarrage d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f966a-148">This example shows how to set a user's Home Drive Directory.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



<span data-ttu-id="f966a-149">Cet exemple montre comment utiliser PasswordExpired pour forcer un utilisateur à modifier le mot de passe à la prochaine ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="f966a-149">This example shows how to use PasswordExpired to force a user to change the password at the next logon.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



<span data-ttu-id="f966a-150">Cet exemple montre comment récupérer le groupe principal de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f966a-150">This example shows how to get the user's primary group.</span></span>


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 