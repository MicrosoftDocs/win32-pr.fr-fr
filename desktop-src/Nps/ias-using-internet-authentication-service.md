---
title: Utilisation des extensions NPS
description: En savoir plus sur l’utilisation des extensions NPS. Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Service d’authentification Internet IAS, tâches
- Service d’authentification Internet IAS, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f422c005d6810a4035450e24de1324b28361f1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989068"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="eb0cd-106">Utilisation des extensions NPS</span><span class="sxs-lookup"><span data-stu-id="eb0cd-106">Using NPS Extensions</span></span>

<span data-ttu-id="eb0cd-107">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server).</span><span class="sxs-lookup"><span data-stu-id="eb0cd-107">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="eb0cd-108">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-108">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="eb0cd-109">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-109">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="eb0cd-110">\* \* Windows Server 2008 R2 et Windows Server 2008 : \* \*</span><span class="sxs-lookup"><span data-stu-id="eb0cd-110">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="eb0cd-111">Les exemples Dial et MapName étendent les fonctionnalités du serveur NPS.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-111">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="eb0cd-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb0cd-112">Sample</span></span>             | <span data-ttu-id="eb0cd-113">Description</span><span class="sxs-lookup"><span data-stu-id="eb0cd-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0cd-114">Profil</span><span class="sxs-lookup"><span data-stu-id="eb0cd-114">DialIn</span></span><br/>  | <span data-ttu-id="eb0cd-115">Cet exemple implémente une DLL d’extension RADIUS qui vérifie le bit d’accès à distance pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-115">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="eb0cd-116">MapName</span><span class="sxs-lookup"><span data-stu-id="eb0cd-116">MapName</span></span><br/> | <span data-ttu-id="eb0cd-117">Cet exemple de DLL d’extension recherche le compte désigné dans tous les domaines approuvés.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-117">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="eb0cd-118">Cela permet aux utilisateurs de plusieurs domaines d’être authentifiés sans que les utilisateurs aient à fournir leur nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-118">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="eb0cd-119">Vous pouvez trouver le code source pour les exemples d’applications MapName et Dial dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-119">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="eb0cd-120">L' *emplacement*% Installation Path%, désigne le répertoire d’installation de base pour les ordinateurs x64.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-120">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="eb0cd-121">Consultez également le [Kit de développement logiciel (SDK) Windows pour Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), le kit de développement logiciel (SDK) Microsoft Windows et les [téléchargements pour le développement d’applications du Windows Store](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="eb0cd-121">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="eb0cd-122">SDK Windows pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="eb0cd-122">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="eb0cd-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eb0cd-123">Windows Server 2012</span></span>

<span data-ttu-id="eb0cd-124">Lien de téléchargement : N/A</span><span class="sxs-lookup"><span data-stu-id="eb0cd-124">Download link: N/A</span></span>

<span data-ttu-id="eb0cd-125">MapName : non</span><span class="sxs-lookup"><span data-stu-id="eb0cd-125">MapName: No</span></span>

<span data-ttu-id="eb0cd-126">Numérotation : non</span><span class="sxs-lookup"><span data-stu-id="eb0cd-126">DialIn: No</span></span>

<span data-ttu-id="eb0cd-127">Emplacement : N/A</span><span class="sxs-lookup"><span data-stu-id="eb0cd-127">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="eb0cd-128">Kit de développement logiciel (SDK) Microsoft Windows pour Windows 7 et .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="eb0cd-128">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="eb0cd-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eb0cd-129">Windows Server 2008 R2</span></span>

<span data-ttu-id="eb0cd-130">Lien de téléchargement : <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="eb0cd-130">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="eb0cd-131">MapName : Oui</span><span class="sxs-lookup"><span data-stu-id="eb0cd-131">MapName: Yes</span></span>

<span data-ttu-id="eb0cd-132">Numérotation : non</span><span class="sxs-lookup"><span data-stu-id="eb0cd-132">DialIn: No</span></span>

<span data-ttu-id="eb0cd-133">Emplacement :% installation chemin%% \\ SDK \\ Microsoft \\ exemples Windows v 7.1 \\ \\ netds \\ IAS</span><span class="sxs-lookup"><span data-stu-id="eb0cd-133">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="eb0cd-134">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="eb0cd-134">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="eb0cd-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb0cd-135">Windows Server 2008</span></span>

<span data-ttu-id="eb0cd-136">Lien de téléchargement : <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="eb0cd-136">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="eb0cd-137">MapName : Oui</span><span class="sxs-lookup"><span data-stu-id="eb0cd-137">MapName: Yes</span></span>

<span data-ttu-id="eb0cd-138">Numérotation : non</span><span class="sxs-lookup"><span data-stu-id="eb0cd-138">DialIn: No</span></span>

<span data-ttu-id="eb0cd-139">Emplacement :% installation chemin%% \\ SDK \\ Microsoft \\ exemples Windows v 6.1 \\ \\ NetDs \\ IAS</span><span class="sxs-lookup"><span data-stu-id="eb0cd-139">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="eb0cd-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb0cd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb0cd-141">Téléchargements pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="eb0cd-141">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="eb0cd-142">SDK Windows pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="eb0cd-142">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





