---
description: À compter de Windows 8, Microsoft a commencé à distribuer les fournisseurs qui vous permettent de partager en toute sécurité des secrets et des messages chiffrés sur les ordinateurs.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Fournisseurs de protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951682"
---
# <a name="protection-providers"></a><span data-ttu-id="e021d-103">Fournisseurs de protection</span><span class="sxs-lookup"><span data-stu-id="e021d-103">Protection Providers</span></span>

<span data-ttu-id="e021d-104">À compter de Windows 8, Microsoft a commencé à distribuer les fournisseurs qui vous permettent de partager en toute sécurité des secrets et des messages chiffrés sur les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="e021d-104">Beginning with Windows 8, Microsoft began distributing the providers that enable you to securely share encrypted secrets and messages across computers.</span></span> <span data-ttu-id="e021d-105">Il existe actuellement deux fournisseurs de protection de clé.</span><span class="sxs-lookup"><span data-stu-id="e021d-105">There are currently two key protection providers.</span></span> <span data-ttu-id="e021d-106">Le fournisseur de protection de clé Microsoft vous permet de protéger le contenu d’un groupe dans une forêt Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e021d-106">The Microsoft Key Protection provider allows you to protect content to a group in an Active Directory forest.</span></span> <span data-ttu-id="e021d-107">Le fournisseur de protection de clé client Microsoft vous permet de protéger le contenu d’un ensemble d’informations d’identification Web.</span><span class="sxs-lookup"><span data-stu-id="e021d-107">The Microsoft Client Key Protection provider allows you to protect content to a set of web credentials.</span></span>

<span data-ttu-id="e021d-108">Le protecteur approprié à utiliser est automatiquement choisi lorsque la fonction [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analyse la chaîne de règle du descripteur de protection que vous fournissez en tant qu’entrée.</span><span class="sxs-lookup"><span data-stu-id="e021d-108">The correct protector to use is automatically chosen for you when the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function parses the protection descriptor rule string your provide as input.</span></span> <span data-ttu-id="e021d-109">Le fournisseur de protection de clé Microsoft est choisi pour les chaînes de règle qui commencent par SID, SDDL et LOCAL.</span><span class="sxs-lookup"><span data-stu-id="e021d-109">The Microsoft Key Protection provider is chosen for rule strings that begin with SID, SDDL, and LOCAL.</span></span> <span data-ttu-id="e021d-110">Le fournisseur de protection de clé client Microsoft analyse les chaînes de règles qui commencent par webinformation.</span><span class="sxs-lookup"><span data-stu-id="e021d-110">The Microsoft Client Key Protection provider parses rule strings that begin with WEBCREDENTIALS.</span></span> <span data-ttu-id="e021d-111">Pour plus d’informations sur les chaînes de règle, consultez [descripteurs de protection](protection-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="e021d-111">For more information about rule strings, see [Protection Descriptors](protection-descriptors.md).</span></span>

> [!Note]  
> <span data-ttu-id="e021d-112">Les fournisseurs personnalisés ne sont pas autorisés actuellement. [DPAPI CNG](cng-dpapi.md)</span><span class="sxs-lookup"><span data-stu-id="e021d-112">Custom providers are not currently allowed.[CNG DPAPI](cng-dpapi.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e021d-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e021d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e021d-114">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="e021d-114">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="e021d-115">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e021d-115">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[<span data-ttu-id="e021d-116">Descripteurs de protection</span><span class="sxs-lookup"><span data-stu-id="e021d-116">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> </dl>

 

 



