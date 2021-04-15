---
title: Utilisation des extensions NPS
description: Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Service d’authentification Internet IAS, tâches
- Service d’authentification Internet IAS, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104507843"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="597ae-105">Utilisation des extensions NPS</span><span class="sxs-lookup"><span data-stu-id="597ae-105">Using NPS Extensions</span></span>

<span data-ttu-id="597ae-106">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server).</span><span class="sxs-lookup"><span data-stu-id="597ae-106">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="597ae-107">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="597ae-107">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="597ae-108">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="597ae-108">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="597ae-109">\* \* Windows Server 2008 R2 et Windows Server 2008 : \* \*</span><span class="sxs-lookup"><span data-stu-id="597ae-109">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="597ae-110">Les exemples Dial et MapName étendent les fonctionnalités du serveur NPS.</span><span class="sxs-lookup"><span data-stu-id="597ae-110">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="597ae-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="597ae-111">Sample</span></span>             | <span data-ttu-id="597ae-112">Description</span><span class="sxs-lookup"><span data-stu-id="597ae-112">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="597ae-113">Profil</span><span class="sxs-lookup"><span data-stu-id="597ae-113">DialIn</span></span><br/>  | <span data-ttu-id="597ae-114">Cet exemple implémente une DLL d’extension RADIUS qui vérifie le bit d’accès à distance pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="597ae-114">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="597ae-115">MapName</span><span class="sxs-lookup"><span data-stu-id="597ae-115">MapName</span></span><br/> | <span data-ttu-id="597ae-116">Cet exemple de DLL d’extension recherche le compte désigné dans tous les domaines approuvés.</span><span class="sxs-lookup"><span data-stu-id="597ae-116">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="597ae-117">Cela permet aux utilisateurs de plusieurs domaines d’être authentifiés sans que les utilisateurs aient à fournir leur nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="597ae-117">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="597ae-118">Vous pouvez trouver le code source pour les exemples d’applications MapName et Dial dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="597ae-118">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="597ae-119">L' *emplacement*% Installation Path%, désigne le répertoire d’installation de base pour les ordinateurs x64.</span><span class="sxs-lookup"><span data-stu-id="597ae-119">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="597ae-120">Consultez également le [Kit de développement logiciel (SDK) Windows pour Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), le kit de développement logiciel (SDK) Microsoft Windows et les [téléchargements pour le développement d’applications du Windows Store](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="597ae-120">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="597ae-121">SDK Windows pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="597ae-121">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="597ae-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="597ae-122">Windows Server 2012</span></span>

<span data-ttu-id="597ae-123">Lien de téléchargement : N/A</span><span class="sxs-lookup"><span data-stu-id="597ae-123">Download link: N/A</span></span>

<span data-ttu-id="597ae-124">MapName : non</span><span class="sxs-lookup"><span data-stu-id="597ae-124">MapName: No</span></span>

<span data-ttu-id="597ae-125">Numérotation : non</span><span class="sxs-lookup"><span data-stu-id="597ae-125">DialIn: No</span></span>

<span data-ttu-id="597ae-126">Emplacement : N/A</span><span class="sxs-lookup"><span data-stu-id="597ae-126">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="597ae-127">Kit de développement logiciel (SDK) Microsoft Windows pour Windows 7 et .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="597ae-127">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="597ae-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="597ae-128">Windows Server 2008 R2</span></span>

<span data-ttu-id="597ae-129">Lien de téléchargement : <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="597ae-129">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="597ae-130">MapName : Oui</span><span class="sxs-lookup"><span data-stu-id="597ae-130">MapName: Yes</span></span>

<span data-ttu-id="597ae-131">Numérotation : non</span><span class="sxs-lookup"><span data-stu-id="597ae-131">DialIn: No</span></span>

<span data-ttu-id="597ae-132">Emplacement :% installation chemin%% \\ SDK \\ Microsoft \\ exemples Windows v 7.1 \\ \\ netds \\ IAS</span><span class="sxs-lookup"><span data-stu-id="597ae-132">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="597ae-133">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="597ae-133">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="597ae-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="597ae-134">Windows Server 2008</span></span>

<span data-ttu-id="597ae-135">Lien de téléchargement : <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="597ae-135">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="597ae-136">MapName : Oui</span><span class="sxs-lookup"><span data-stu-id="597ae-136">MapName: Yes</span></span>

<span data-ttu-id="597ae-137">Numérotation : non</span><span class="sxs-lookup"><span data-stu-id="597ae-137">DialIn: No</span></span>

<span data-ttu-id="597ae-138">Emplacement :% installation chemin%% \\ SDK \\ Microsoft \\ exemples Windows v 6.1 \\ \\ NetDs \\ IAS</span><span class="sxs-lookup"><span data-stu-id="597ae-138">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="597ae-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="597ae-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="597ae-140">Téléchargements pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="597ae-140">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="597ae-141">SDK Windows pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="597ae-141">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





