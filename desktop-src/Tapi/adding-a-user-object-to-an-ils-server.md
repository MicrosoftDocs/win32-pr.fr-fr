---
description: Le fragment de code suivant illustre la publication d’un objet utilisateur dans un serveur ILS. Après la publication d’un objet utilisateur, les tiers distants peuvent utiliser l’objet utilisateur pour effectuer des appels à l’utilisateur spécifié.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Ajout d’un objet utilisateur à un serveur ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750781"
---
# <a name="adding-a-user-object-to-an-ils-server"></a><span data-ttu-id="51fbf-104">Ajout d’un objet utilisateur à un serveur ILS</span><span class="sxs-lookup"><span data-stu-id="51fbf-104">Adding a User Object to an ILS Server</span></span>

<span data-ttu-id="51fbf-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="51fbf-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="51fbf-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="51fbf-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="51fbf-107">Le fragment de code suivant illustre la publication d’un objet utilisateur dans un serveur ILS.</span><span class="sxs-lookup"><span data-stu-id="51fbf-107">The following code fragment illustrates publishing a user object in an ILS server.</span></span> <span data-ttu-id="51fbf-108">Après la publication d’un objet utilisateur, les tiers distants peuvent utiliser l’objet utilisateur pour effectuer des appels à l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="51fbf-108">After a user object is published, remote parties can use the user object to make calls to the specified user.</span></span>

<span data-ttu-id="51fbf-109">Ce fragment part du principe que la [connexion à un serveur ils](connecting-to-an-ils-server.md) a déjà été effectuée.</span><span class="sxs-lookup"><span data-stu-id="51fbf-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a><span data-ttu-id="51fbf-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51fbf-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51fbf-111">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="51fbf-111">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="51fbf-112">**ITDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="51fbf-112">**ITDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[<span data-ttu-id="51fbf-113">**ITDirectoryObjectUser**</span><span class="sxs-lookup"><span data-stu-id="51fbf-113">**ITDirectoryObjectUser**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



