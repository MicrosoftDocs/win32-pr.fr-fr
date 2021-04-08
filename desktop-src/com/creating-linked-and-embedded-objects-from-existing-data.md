---
title: Création d’objets liés et incorporés à partir de données existantes
description: Création d’objets liés et incorporés à partir de données existantes
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675710"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a><span data-ttu-id="e8f48-103">Création d’objets liés et incorporés à partir de données existantes</span><span class="sxs-lookup"><span data-stu-id="e8f48-103">Creating Linked and Embedded Objects from Existing Data</span></span>

<span data-ttu-id="e8f48-104">Un utilisateur assemble généralement un document composé à l’aide du presse-papiers ou du glisser-déplacer pour copier un objet de données de son application serveur vers l’application conteneur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8f48-104">A user typically assembles a compound document by using either the clipboard or drag and drop to copy a data object from its server application to the user's container application.</span></span> <span data-ttu-id="e8f48-105">Avec les applications qui prennent en charge OLE, l’utilisateur peut lancer le transfert à partir du serveur ou du conteneur.</span><span class="sxs-lookup"><span data-stu-id="e8f48-105">With applications that support OLE, the user can initiate the transfer from either the server or the container.</span></span> <span data-ttu-id="e8f48-106">Par exemple, le serveur peut copier des données dans le presse-papiers de l’application serveur, puis basculer vers l’application conteneur et choisir coller un objet spécial/incorporé ou une commande de menu équivalente pour créer un nouvel objet incorporé à partir des données sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="e8f48-106">For example, the server can copy data to the clipboard in the server application, then switch to the container application and choose Paste Special/Embedded Object or an equivalent menu command to create a new embedded object from the selected data.</span></span> <span data-ttu-id="e8f48-107">Ou, l’utilisateur peut faire glisser les données d’une application à l’autre.</span><span class="sxs-lookup"><span data-stu-id="e8f48-107">Or, the user can drag the data from one application to the other.</span></span> <span data-ttu-id="e8f48-108">Le processus est similaire pour la création d’un objet lié.</span><span class="sxs-lookup"><span data-stu-id="e8f48-108">The process is similar for creating a linked object.</span></span>

> [!Note]  
> <span data-ttu-id="e8f48-109">Une application qui fonctionne comme un serveur OLE et un conteneur peut utiliser une sélection de ses propres données pour créer un objet incorporé ou lié à un nouvel emplacement dans le même document.</span><span class="sxs-lookup"><span data-stu-id="e8f48-109">An application that functions as both OLE server and container can use a selection of its own data to create an embedded or linked object at a new location within the same document.</span></span>

 

<span data-ttu-id="e8f48-110">Le transfert de données entre le serveur OLE et les applications de conteneur repose sur le transfert de données uniforme, comme décrit dans [transfert de données](data-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="e8f48-110">Data transfer between OLE server and container applications is built on uniform data transfer, as described in [Data Transfer](data-transfer.md).</span></span> <span data-ttu-id="e8f48-111">Les serveurs OLE et les gestionnaires d’objets implémentent [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) afin que leurs données soient disponibles pour les transferts à l’aide du presse-papiers ou du glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="e8f48-111">OLE servers and object handlers implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) in order to make their data available for transfers using either the clipboard or drag and drop.</span></span> <span data-ttu-id="e8f48-112">Les objets OLE prennent en charge tous les formats de presse-papiers habituels.</span><span class="sxs-lookup"><span data-stu-id="e8f48-112">OLE objects support all the usual clipboard formats.</span></span> <span data-ttu-id="e8f48-113">En outre, ils prennent en charge six formats de presse-papiers qui prennent en charge la création d’objets liés et incorporés à partir d’un objet de données sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e8f48-113">In addition, they support six clipboard formats that support the creation of linked and embedded objects from a selected data object.</span></span>

<span data-ttu-id="e8f48-114">Les formats de presse-papiers OLE décrivent les objets de données qui, en cas de suppression ou de collage dans des conteneurs OLE, doivent devenir des objets incorporés ou liés à des documents composés.</span><span class="sxs-lookup"><span data-stu-id="e8f48-114">OLE clipboard formats describe data objects that, upon being dropped or pasted in OLE containers, are to become embedded or linked compound-document objects.</span></span> <span data-ttu-id="e8f48-115">L’objet de données présente ces formats aux applications conteneur par ordre de fidélité comme description des données.</span><span class="sxs-lookup"><span data-stu-id="e8f48-115">The data object presents these formats to container applications in order of their fidelity as descriptions of the data.</span></span> <span data-ttu-id="e8f48-116">En d’autres termes, l’objet présente le format le mieux représenté, suivi du meilleur format, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e8f48-116">In other words, the object presents first the format that best represents it, followed by the next best format, and so on.</span></span> <span data-ttu-id="e8f48-117">Ce classement intentionnel encourage une application de conteneur à utiliser le meilleur format possible.</span><span class="sxs-lookup"><span data-stu-id="e8f48-117">This intentional ordering encourages a container application to use the best possible format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8f48-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8f48-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8f48-119">Documents composés</span><span class="sxs-lookup"><span data-stu-id="e8f48-119">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="e8f48-120">Transfert de données</span><span class="sxs-lookup"><span data-stu-id="e8f48-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




