---
description: Tout comme le système utilise des descripteurs de sécurité pour contrôler l’accès aux objets sécurisables, un serveur peut utiliser des descripteurs de sécurité pour contrôler l’accès à ses objets privés. Pour plus d’informations sur le modèle de sécurité Windows, consultez Access Control modèle.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Access Control basées sur les listes de contrôle d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756181"
---
# <a name="acl-based-access-control"></a><span data-ttu-id="da003-104">Access Control basées sur les listes de contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="da003-104">ACL-based Access Control</span></span>

<span data-ttu-id="da003-105">Tout comme le système utilise des [descripteurs de sécurité](security-descriptors.md) pour contrôler l’accès aux objets sécurisables, un serveur peut utiliser des descripteurs de sécurité pour contrôler l’accès à ses objets privés.</span><span class="sxs-lookup"><span data-stu-id="da003-105">Just as the system uses [security descriptors](security-descriptors.md) to control access to securable objects, a server can use security descriptors to control access to its private objects.</span></span> <span data-ttu-id="da003-106">Pour plus d’informations sur le modèle de sécurité Windows, consultez [Access Control modèle](access-control-model.md).</span><span class="sxs-lookup"><span data-stu-id="da003-106">For more information about the Windows security model, see [Access Control Model](access-control-model.md).</span></span>

<span data-ttu-id="da003-107">Un serveur protégé peut [créer un descripteur de sécurité](security-descriptors-for-private-objects.md) avec une liste DACL qui spécifie les types d’accès autorisés pour différents types de [confiance](trustees.md).</span><span class="sxs-lookup"><span data-stu-id="da003-107">A protected server can [create a security descriptor](security-descriptors-for-private-objects.md) with a DACL that specifies the types of access allowed for various [trustees](trustees.md).</span></span> <span data-ttu-id="da003-108">Dans un cas simple, le serveur peut créer un descripteur de sécurité unique pour [contrôler l’accès à toutes les données et fonctionnalités du serveur](checking-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="da003-108">In a simple case, the server could create a single security descriptor to [control access to all of the server's data and functionality](checking-access-to-private-objects.md).</span></span> <span data-ttu-id="da003-109">Pour une granularité plus fine de la protection, le serveur peut créer des descripteurs de sécurité pour chacun de ses objets privés ou pour différents types de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="da003-109">For a finer granularity of protection, the server could create security descriptors for each of its private objects, or for different types of functionality.</span></span>

<span data-ttu-id="da003-110">Par exemple, lorsqu’un client demande au serveur de créer un nouvel objet dans une base de données, le serveur peut créer un descripteur de sécurité pour le nouvel objet privé.</span><span class="sxs-lookup"><span data-stu-id="da003-110">For example, when a client asks the server to create a new object in a database, the server could create a security descriptor for the new private object.</span></span> <span data-ttu-id="da003-111">Le serveur peut ensuite stocker le descripteur de sécurité avec l’objet privé dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="da003-111">The server could then store the security descriptor with the private object in the database.</span></span> <span data-ttu-id="da003-112">Lorsqu’un client tente d’accéder à l’objet, le serveur récupère le descripteur de sécurité pour vérifier les droits d’accès du client.</span><span class="sxs-lookup"><span data-stu-id="da003-112">When a client tries to access the object, the server retrieves the security descriptor to check the client's access rights.</span></span> <span data-ttu-id="da003-113">Il est important de noter qu’il n’y a rien dans un descripteur de sécurité qui l’associe à l’objet ou aux fonctionnalités qu’il protège.</span><span class="sxs-lookup"><span data-stu-id="da003-113">It is important to note that there is nothing in a security descriptor that associates it with the object or functionality it is protecting.</span></span> <span data-ttu-id="da003-114">Au lieu de cela, il revient au serveur protégé de conserver l’Association.</span><span class="sxs-lookup"><span data-stu-id="da003-114">Instead, it is up to the protected server to maintain the association.</span></span>

<span data-ttu-id="da003-115">L’accès à l’objet privé peut également être audité.</span><span class="sxs-lookup"><span data-stu-id="da003-115">Access to the private object can also be audited.</span></span> <span data-ttu-id="da003-116">Pour obtenir une description de cet objet, consultez [auditer l’accès aux objets privés](auditing-access-to-private-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="da003-116">Refer to [Auditing Access to Private Objects](auditing-access-to-private-objects.md) for a description of this.</span></span>

 

 



