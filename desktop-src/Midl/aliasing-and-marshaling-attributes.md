---
title: Attributs d’alias et de marshaling
description: Les applications distribuées passent presque toujours des données entre les programmes client et serveur lorsqu’elles appellent des procédures d’interface.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- IDL MIDL, attributs MIDL, crénelage et marshaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029791"
---
# <a name="aliasing-and-marshaling-attributes"></a><span data-ttu-id="82a07-104">Attributs d’alias et de marshaling</span><span class="sxs-lookup"><span data-stu-id="82a07-104">Aliasing and Marshaling Attributes</span></span>

<span data-ttu-id="82a07-105">Les applications distribuées passent presque toujours des données entre les programmes client et serveur lorsqu’elles appellent des procédures d’interface.</span><span class="sxs-lookup"><span data-stu-id="82a07-105">Distributed applications almost always pass data between client and server programs when they call interface procedures.</span></span> <span data-ttu-id="82a07-106">Les développeurs utilisent MIDL pour décrire les données que les programmes client et serveur transmettent de manière standard.</span><span class="sxs-lookup"><span data-stu-id="82a07-106">Developers use MIDL to describe the data that client and server programs pass in a standard way.</span></span> <span data-ttu-id="82a07-107">Le compilateur MIDL crée des programmes stub d’application, ou proxy, pour le client et le serveur qui convertissent les données en un format standardisé pouvant être envoyé sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="82a07-107">The MIDL compiler creates application stub, or proxy, programs for the client and the server that convert the data into a standardized form that can be sent over a network.</span></span> <span data-ttu-id="82a07-108">Ce format, le format de représentation de données réseau (NDR), est souvent appelé le format de transmission des données.</span><span class="sxs-lookup"><span data-stu-id="82a07-108">This format, the Network Data Representation (NDR) format, is often called the wire format of the data.</span></span> <span data-ttu-id="82a07-109">Les stubs doivent convertir les données à partir de leur format natif dans l’espace mémoire du programme vers NDR.</span><span class="sxs-lookup"><span data-stu-id="82a07-109">The stubs must convert data from its native format in the program's memory space to NDR.</span></span> <span data-ttu-id="82a07-110">Cette conversion est appelée marshaling des données.</span><span class="sxs-lookup"><span data-stu-id="82a07-110">This conversion is termed marshaling the data.</span></span> <span data-ttu-id="82a07-111">Lorsqu’un client ou un programme serveur reçoit des données, il doit convertir les données du rapport de non-remise au format natif de ce programme.</span><span class="sxs-lookup"><span data-stu-id="82a07-111">When a client or server program receives data, it must convert the data from NDR to the native format for that program.</span></span> <span data-ttu-id="82a07-112">C’est ce que l’on appelle démarshaler les données.</span><span class="sxs-lookup"><span data-stu-id="82a07-112">This is called unmarshaling the data.</span></span>

<span data-ttu-id="82a07-113">Utilisez des attributs d’alias et de marshaling pour contrôler la façon dont vos données sont empaquetées dans un format de rapport de non-remise et transmises sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="82a07-113">Use aliasing and marshaling attributes to control how your data is packaged into NDR format and transmitted over the network.</span></span>



| <span data-ttu-id="82a07-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="82a07-114">Attribute</span></span>                             | <span data-ttu-id="82a07-115">Utilisation</span><span class="sxs-lookup"><span data-stu-id="82a07-115">Usage</span></span>                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82a07-116">**appeler \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="82a07-116">**call\_as**</span></span>](call-as.md)           | <span data-ttu-id="82a07-117">Mappe une fonction qui n’est pas accessible à distance à un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="82a07-117">Maps a nonremotable function to a remote procedure call.</span></span>                                                                      |
| [<span data-ttu-id="82a07-118">**IID \_ est**</span><span class="sxs-lookup"><span data-stu-id="82a07-118">**iid\_is**</span></span>](iid-is.md)             | <span data-ttu-id="82a07-119">Fournit l’identificateur d’interface de l’interface COM qui est l’objet du pointeur.</span><span class="sxs-lookup"><span data-stu-id="82a07-119">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                     |
| [<span data-ttu-id="82a07-120">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="82a07-120">**transmit\_as**</span></span>](transmit-as.md)   | <span data-ttu-id="82a07-121">Convertit un type de données en un type plus simple pour la transmission sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="82a07-121">Converts a data type to a simpler type for transmission over a network.</span></span>                                                       |
| [<span data-ttu-id="82a07-122">**Marshal de câble \_**</span><span class="sxs-lookup"><span data-stu-id="82a07-122">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="82a07-123">Semblable à [**transmit \_ As**](transmit-as.md) , mais vous implémentez les routines de dimensionnement, de marshaler, de démarshaler et de libération des données.</span><span class="sxs-lookup"><span data-stu-id="82a07-123">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="82a07-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82a07-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82a07-125">Conversion de type et marshaling des attributs ACF</span><span class="sxs-lookup"><span data-stu-id="82a07-125">Type Conversion and Marshaling ACF Attributes</span></span>](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




