---
description: L’API du gestionnaire d’identités homologues vous permet de créer, d’énumérer et de manipuler des identités d’homologue dans une application homologue.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: À propos du gestionnaire d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865174"
---
# <a name="about-identity-manager"></a><span data-ttu-id="ae6d5-103">À propos du gestionnaire d’identité</span><span class="sxs-lookup"><span data-stu-id="ae6d5-103">About Identity Manager</span></span>

<span data-ttu-id="ae6d5-104">L’API du gestionnaire d’identités homologues vous permet de créer, d’énumérer et de manipuler des identités d’homologue dans une application homologue.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-104">The Peer Identity Manager API allows you to create, enumerate, and manipulate peer identities in a peer application.</span></span> <span data-ttu-id="ae6d5-105">Vous pouvez utiliser les identités d’homologue créées à l’aide de cette API comme entrée pour le regroupement d’homologues et les API du fournisseur d’espace de noms PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-105">You can use the peer identities created using this API as input for the Peer Grouping and Peer Name Resolution Protocol (PNRP) Namespace Provider APIs.</span></span>

## <a name="peer-identity-manager-best-practices"></a><span data-ttu-id="ae6d5-106">Meilleures pratiques pour Peer Identity Manager</span><span class="sxs-lookup"><span data-stu-id="ae6d5-106">Peer Identity Manager Best Practices</span></span>

<span data-ttu-id="ae6d5-107">Chaque utilisateur doit avoir plusieurs identités d’homologue qu’il peut utiliser pour les activités homologues.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-107">Each user should have a few peer identities that they can use for the peer activities.</span></span> <span data-ttu-id="ae6d5-108">Par exemple, un utilisateur peut avoir deux identités d’homologue pour le travail et le loisir.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-108">For example, a user might have two peer identities for work and leisure.</span></span>

<span data-ttu-id="ae6d5-109">Une application homologue bien conçue permet à un utilisateur de sélectionner une identité d’homologue à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-109">A well-designed peer application allows a user to select a peer identity to use.</span></span> <span data-ttu-id="ae6d5-110">Un utilisateur peut créer une nouvelle identité d’homologue si aucune des identités d’homologue existantes n’est appropriée pour une utilisation avec une application.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-110">A user can create a new peer identity if none of the existing peer identities are appropriate to use with an application.</span></span>

<span data-ttu-id="ae6d5-111">Une application homologue bien conçue contrôle également le nombre d’identités qu’elle crée.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-111">A well-designed peer application also controls the number of identities that it creates.</span></span> <span data-ttu-id="ae6d5-112">Si une application crée une identité d’homologue temporaire, l’application doit supprimer l’identité d’homologue lorsque l’identité n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-112">If an application creates a temporary peer identity, the application must delete the peer identity when the identity is not needed.</span></span> <span data-ttu-id="ae6d5-113">Si une application n’effectue pas cette opération de maintenance, le gestionnaire d’identité de l’homologue peut ne pas être en mesure de créer des identités d’homologue tant que certaines identités d’homologue n’ont pas été</span><span class="sxs-lookup"><span data-stu-id="ae6d5-113">If an application does not perform this maintenance, the Peer Identity Manager may not be able to create peer identities until some peer identities are removed.</span></span>

 

 



