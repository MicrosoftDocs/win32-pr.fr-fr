---
title: Attributs d’identification utilisateur
description: L’identité de l’utilisateur demandant l’authentification est fournie aux DLL d’extension NPS dans plusieurs attributs différents.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Attributs, identification de l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511090"
---
# <a name="user-identification-attributes"></a><span data-ttu-id="bb08b-104">Attributs d’identification utilisateur</span><span class="sxs-lookup"><span data-stu-id="bb08b-104">User Identification Attributes</span></span>

> [!Note]  
> <span data-ttu-id="bb08b-105">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bb08b-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="bb08b-106">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="bb08b-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="bb08b-107">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="bb08b-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="bb08b-108">L’identité de l’utilisateur demandant l’authentification est fournie aux DLL d’extension NPS dans plusieurs attributs différents.</span><span class="sxs-lookup"><span data-stu-id="bb08b-108">The identity of the user requesting authentication is supplied to the NPS Extension DLLs in a number of different attributes.</span></span>

-   <span data-ttu-id="bb08b-109">**ratUserName**</span><span class="sxs-lookup"><span data-stu-id="bb08b-109">**ratUserName**</span></span>
-   <span data-ttu-id="bb08b-110">**ratStrippedUserName**</span><span class="sxs-lookup"><span data-stu-id="bb08b-110">**ratStrippedUserName**</span></span>
-   <span data-ttu-id="bb08b-111">**ratFQUserName**</span><span class="sxs-lookup"><span data-stu-id="bb08b-111">**ratFQUserName**</span></span>

<span data-ttu-id="bb08b-112">Chaque attribut fournit l’identité de l’utilisateur dans un format différent.</span><span class="sxs-lookup"><span data-stu-id="bb08b-112">Each attribute provides the user identity in a different format.</span></span> <span data-ttu-id="bb08b-113">En général, les développeurs doivent utiliser **ratStrippedUserName**.</span><span class="sxs-lookup"><span data-stu-id="bb08b-113">In general, developers should use **ratStrippedUserName**.</span></span> <span data-ttu-id="bb08b-114">Les utilisations des attributs **ratUserName** et **ratFQUserName** sont plus spécialisées.</span><span class="sxs-lookup"><span data-stu-id="bb08b-114">The uses of the **ratUserName** and **ratFQUserName** attributes are more specialized.</span></span>

> [!Note]  
> <span data-ttu-id="bb08b-115">L’attribut User-Password, **ratUserPassword**, a déjà été déchiffré lorsqu’il est envoyé à la dll d’extension et est utilisable sous cette forme.</span><span class="sxs-lookup"><span data-stu-id="bb08b-115">The User-Password attribute, **ratUserPassword**, has already been decrypted when it is sent to the extension DLL and is usable in that form.</span></span>

 

## <a name="ratusername"></a><span data-ttu-id="bb08b-116">ratUserName</span><span class="sxs-lookup"><span data-stu-id="bb08b-116">ratUserName</span></span>

<span data-ttu-id="bb08b-117">L’attribut **ratUserName** contient le nom qui a été réellement envoyé « sur le réseau ».</span><span class="sxs-lookup"><span data-stu-id="bb08b-117">The **ratUserName** attribute contains the name that was actually sent "over the wire."</span></span> <span data-ttu-id="bb08b-118">NPS n’a pas, de quelque manière, traité ni validé le contenu de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="bb08b-118">NPS has not, in any way, processed or validated the contents of this attribute.</span></span> <span data-ttu-id="bb08b-119">Cet attribut n’est peut-être pas disponible du tout car l’utilisateur a peut-être été identifié par un moyen tel que ID de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="bb08b-119">This attribute may not be available at all because the user may have been identified through a means such as caller ID.</span></span>

<span data-ttu-id="bb08b-120">Lors de l’utilisation de [**RadiusExtensionProcess/ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), si cet attribut est disponible, il est disponible uniquement au point de plug-in de DLL d’extension d’authentification.</span><span class="sxs-lookup"><span data-stu-id="bb08b-120">When using [**RadiusExtensionProcess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), if this attribute is available, it is available only at the Authentication Extension DLL plug-in point.</span></span> <span data-ttu-id="bb08b-121">L’attribut **ratUserName** n’est pas disponible sur le point de plug-in de DLL d’extension d’autorisation, car dans les dll d’extension d’autorisation les fonctions **RadiusExtensionProcess/ex** affichent uniquement les attributs « sortants ».</span><span class="sxs-lookup"><span data-stu-id="bb08b-121">The **ratUserName** attribute is not available at the Authorization Extension DLL plug-in point because in Authorization Extension DLLs the **RadiusExtensionProcess/Ex** functions see only the "outbound" attributes.</span></span>

<span data-ttu-id="bb08b-122">Quand vous utilisez [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), si cet attribut est disponible, il est disponible à la fois dans le point de plug-in de DLL d’extension d’authentification et dans le point de plug-in de DLL d’extension d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="bb08b-122">When using [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), if this attribute is available, it is available at both the Authentication Extension DLL plug-in point and the Authorization Extension DLL plug-in point.</span></span>

## <a name="ratstrippedusername"></a><span data-ttu-id="bb08b-123">ratStrippedUserName</span><span class="sxs-lookup"><span data-stu-id="bb08b-123">ratStrippedUserName</span></span>

<span data-ttu-id="bb08b-124">Le **ratStrippedUserName** est l’identité de l’utilisateur après « suppression du domaine ».</span><span class="sxs-lookup"><span data-stu-id="bb08b-124">The **ratStrippedUserName** is the user's identity after "realm stripping."</span></span> <span data-ttu-id="bb08b-125">Pour plus d’informations sur la suppression de domaines, consultez la rubrique relative aux [noms de domaine](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) sur http : \\ \\ technet2.Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="bb08b-125">For more information on realm stripping, see the [Realm names](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) topic on http:\\\\technet2.microsoft.com.</span></span>

<span data-ttu-id="bb08b-126">Cet attribut peut être présent au point de plug-in de DLL d’extension d’authentification, au point de plug-in DLL d’extension d’autorisation ou aux deux.</span><span class="sxs-lookup"><span data-stu-id="bb08b-126">This attribute may be present at the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="bb08b-127">Le format de cet attribut est garanti :</span><span class="sxs-lookup"><span data-stu-id="bb08b-127">This attribute is guaranteed to have the format:</span></span>

<span data-ttu-id="bb08b-128">\*\*\*\*\\*\*\* Nom d’utilisateur du domaine\*</span><span class="sxs-lookup"><span data-stu-id="bb08b-128">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="bb08b-129">Où *domaine* est le nom de domaine NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="bb08b-129">Where *Domain* is the NetBIOS domain name.</span></span>

## <a name="ratfqusername"></a><span data-ttu-id="bb08b-130">ratFQUserName</span><span class="sxs-lookup"><span data-stu-id="bb08b-130">ratFQUserName</span></span>

<span data-ttu-id="bb08b-131">L’attribut **ratFQUserName** est le nom d’utilisateur « complet ».</span><span class="sxs-lookup"><span data-stu-id="bb08b-131">The **ratFQUserName** attribute is the "fully qualified" user name.</span></span>

<span data-ttu-id="bb08b-132">Cet attribut peut être présent dans le point de plug-in de DLL d’extension d’authentification, le point de plug-in DLL d’extension d’autorisation, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="bb08b-132">This attribute may be present in the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="bb08b-133">Toutefois, le format de l’attribut peut varier entre les deux points de plug-in.</span><span class="sxs-lookup"><span data-stu-id="bb08b-133">However, the format of the attribute may differ between the two plug-in points.</span></span> <span data-ttu-id="bb08b-134">Au point de plug-in de DLL d’extension d’authentification, cet attribut aura toujours la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="bb08b-134">At the Authentication Extension DLL plug-in point, this attribute will always be of the form:</span></span>

<span data-ttu-id="bb08b-135">\*\*\*\*\\*\*\* Nom d’utilisateur du domaine\*</span><span class="sxs-lookup"><span data-stu-id="bb08b-135">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="bb08b-136">Le format de l’attribut **ratFQUserName** au point de plug-in de DLL d’extension d’autorisation varie selon que l’utilisateur est un utilisateur Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bb08b-136">The format of the **ratFQUserName** attribute at the Authorization Extension DLL plug-in point depends on whether the user is an Active Directory user.</span></span>

-   <span data-ttu-id="bb08b-137">Si l’utilisateur est un utilisateur local, **ratFQUserName** a le même format que pour le point de plug-in de DLL d’extension d’authentification :</span><span class="sxs-lookup"><span data-stu-id="bb08b-137">If the user is a local user **ratFQUserName** has the same format as for the Authentication Extension DLL plug-in point:</span></span>

    <span data-ttu-id="bb08b-138">\*\*\*\*\\*\*\* Nom d’utilisateur du domaine\*</span><span class="sxs-lookup"><span data-stu-id="bb08b-138">*Domain ***\\*** UserName*</span></span>

    <span data-ttu-id="bb08b-139">.</span><span class="sxs-lookup"><span data-stu-id="bb08b-139">.</span></span>

-   <span data-ttu-id="bb08b-140">Si l’utilisateur est un utilisateur Active Directory, **ratFQUserName** peut contenir le nom de l’utilisateur au format « canonique ».</span><span class="sxs-lookup"><span data-stu-id="bb08b-140">If the user is an Active Directory user, **ratFQUserName** may contain the user's name in "canonical" format.</span></span> <span data-ttu-id="bb08b-141">Le format canonique est le format utilisé par le Active Directory pour identifier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bb08b-141">Canonical format is the format used by the Active Directory to identify the user.</span></span> <span data-ttu-id="bb08b-142">Il s’agit du chemin d’accès à la racine de l’arborescence de Active Directory et comprend l’unité d’organisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bb08b-142">It is the path from the root of the Active Directory tree, and includes the user's Organizational Unit (OU).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb08b-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bb08b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb08b-144">Configuration des dll d’extension</span><span class="sxs-lookup"><span data-stu-id="bb08b-144">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[<span data-ttu-id="bb08b-145">Appel des dll d’extension</span><span class="sxs-lookup"><span data-stu-id="bb08b-145">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 