---
title: Fonctions Netfile (gestion de réseau)
description: Les fonctions de fichiers de gestion de réseau permettent de surveiller et de fermer les ressources de fichier, de périphérique et de canal ouvertes sur un serveur. Les fonctions de fichier sont répertoriées ci-dessous.
ms.assetid: 3cfb5222-7e02-4bc3-959e-0fc7bc4f0f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b56d1c6d50463989e64386f5829a8e663cddd4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508261"
---
# <a name="netfile-functions-network-management"></a><span data-ttu-id="6fd0c-104">Fonctions Netfile (gestion de réseau)</span><span class="sxs-lookup"><span data-stu-id="6fd0c-104">NetFile Functions (Network Management)</span></span>

<span data-ttu-id="6fd0c-105">Les fonctions de fichiers de gestion de réseau permettent de surveiller et de fermer les ressources de fichier, de périphérique et de canal ouvertes sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-105">The network management file functions provide a way to monitor and close the file, device, and pipe resources open on a server.</span></span> <span data-ttu-id="6fd0c-106">Les fonctions de fichier sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-106">The file functions are listed following.</span></span>



| <span data-ttu-id="6fd0c-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="6fd0c-107">Function</span></span>                                | <span data-ttu-id="6fd0c-108">Description</span><span class="sxs-lookup"><span data-stu-id="6fd0c-108">Description</span></span>                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="6fd0c-109">**NetFileClose**</span><span class="sxs-lookup"><span data-stu-id="6fd0c-109">**NetFileClose**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | <span data-ttu-id="6fd0c-110">Force la fermeture d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-110">Forces a resource to close.</span></span>                                          |
| [<span data-ttu-id="6fd0c-111">**NetFileEnum**</span><span class="sxs-lookup"><span data-stu-id="6fd0c-111">**NetFileEnum**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | <span data-ttu-id="6fd0c-112">Retourne des informations sur les fichiers ouverts sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-112">Returns information about open files on a server.</span></span>                    |
| [<span data-ttu-id="6fd0c-113">**NetFileGetInfo**</span><span class="sxs-lookup"><span data-stu-id="6fd0c-113">**NetFileGetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | <span data-ttu-id="6fd0c-114">Retourne des informations sur une ouverture particulière d’une ressource de serveur.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-114">Returns information about a particular opening of a server resource.</span></span> |



 

<span data-ttu-id="6fd0c-115">Appelez la fonction [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) lorsque le fichier ne peut pas être fermé par un autre moyen.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-115">Call the [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) function when the file cannot be closed by any other means.</span></span> <span data-ttu-id="6fd0c-116">Cette fonction doit être utilisée avec précaution, car **NetFileClose** n’écrit pas les données mises en cache sur le système client dans le fichier avant de fermer le fichier.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-116">This function should be used with caution because **NetFileClose** does not write data cached on the client system to the file before closing the file.</span></span>

<span data-ttu-id="6fd0c-117">La fonction [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) retourne des informations sur les ressources ouvertes sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-117">The [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) function returns information about resources open on a server.</span></span> <span data-ttu-id="6fd0c-118">Un fichier peut être ouvert une ou plusieurs fois par une ou plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-118">A file can be opened one or more times by one or more applications.</span></span> <span data-ttu-id="6fd0c-119">Chaque ouverture de fichier est identifiée de manière unique.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-119">Each file opening is uniquely identified.</span></span> <span data-ttu-id="6fd0c-120">La fonction **NetFileEnum** retourne une entrée pour chaque ouverture de fichier.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-120">The **NetFileEnum** function returns an entry for each file opening.</span></span> <span data-ttu-id="6fd0c-121">La fonction [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) retourne des informations sur l’ouverture d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-121">The [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) function returns information about one opening of a resource.</span></span>

<span data-ttu-id="6fd0c-122">Les informations de fichier sont disponibles aux niveaux suivants :</span><span class="sxs-lookup"><span data-stu-id="6fd0c-122">File information is available at the following levels:</span></span>

-   [<span data-ttu-id="6fd0c-123">**\_Informations sur le fichier \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6fd0c-123">**FILE\_INFO\_2**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-file_info_2)
-   [<span data-ttu-id="6fd0c-124">**\_Informations sur le fichier \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6fd0c-124">**FILE\_INFO\_3**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-file_info_3)

<span data-ttu-id="6fd0c-125">Les niveaux 0 et 1 ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-125">Levels 0 and 1 are not supported.</span></span> <span data-ttu-id="6fd0c-126">Le niveau 2 retourne uniquement le numéro d’identification affecté à la ressource lors de son ouverture.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-126">Level 2 returns only the identification number assigned to the resource when it was opened.</span></span> <span data-ttu-id="6fd0c-127">Le niveau 3 retourne le numéro d’identification, les autorisations, les verrous de fichier et le nom de l’utilisateur qui a ouvert la ressource.</span><span class="sxs-lookup"><span data-stu-id="6fd0c-127">Level 3 returns the identification number, permissions, file locks, and the name of the user who opened the resource.</span></span>

<span data-ttu-id="6fd0c-128">Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) et [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) .</span><span class="sxs-lookup"><span data-stu-id="6fd0c-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) and [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) functions.</span></span> <span data-ttu-id="6fd0c-129">Pour plus d’informations, consultez [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) et [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="6fd0c-129">For more information, see [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
