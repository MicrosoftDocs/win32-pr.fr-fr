---
title: Type-Conversion et marshaling des attributs ACF
description: Utilisez ces attributs pour contrôler la façon dont vos données sont transmises sur le réseau.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- ACF MIDL, attributs, conversion de type et marshaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940211"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a><span data-ttu-id="0ad34-104">Type-Conversion et marshaling des attributs ACF</span><span class="sxs-lookup"><span data-stu-id="0ad34-104">Type-Conversion and Marshaling ACF Attributes</span></span>

<span data-ttu-id="0ad34-105">Utilisez ces attributs pour contrôler la façon dont vos données sont transmises sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="0ad34-105">Use these attributes to control how your data is transmitted over the network.</span></span>



| <span data-ttu-id="0ad34-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="0ad34-106">Attribute</span></span>                                        | <span data-ttu-id="0ad34-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0ad34-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad34-108">[**coder**](encode.md)le [**décode**](decode.md)</span><span class="sxs-lookup"><span data-stu-id="0ad34-108">[**encode**](encode.md)[**decode**](decode.md)</span></span> | <span data-ttu-id="0ad34-109">Ordonne à MIDL d’exposer les routines de sérialisation de type ou de procédure qu’il génère pour les stubs.</span><span class="sxs-lookup"><span data-stu-id="0ad34-109">Instructs MIDL to expose the type or procedure serialization (pickling) routines it generates for the stubs.</span></span> <span data-ttu-id="0ad34-110">Votre application cliente peut appeler ces routines pour marshaler les données par valeur.</span><span class="sxs-lookup"><span data-stu-id="0ad34-110">Your client application can call those routines to marshal data by value.</span></span>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="0ad34-111">**représenter \_ comme**</span><span class="sxs-lookup"><span data-stu-id="0ad34-111">**represent\_as**</span></span>](represent-as.md)            | <span data-ttu-id="0ad34-112">Spécifie la manière dont un type de données est représenté sur le câble, lorsque la nature exacte du type de données d’un client n’a pas d’importance pour le serveur (parce qu’il n’a besoin que des données elles-mêmes et non de la structure réelle), ou que le type de client réel est inconnu de MIDL au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="0ad34-112">Specifies how a data type will be represented on the wire, when the exact nature of a client's data type is unimportant to the server (because it only needs the data itself and not the actual structure), or the actual client type is unknown to MIDL at compile time.</span></span> <span data-ttu-id="0ad34-113">Par exemple, si votre application cliente utilise une liste liée de nombres à virgule flottante, vous pouvez spécifier que la représentation filaire de cette liste soit un tableau de type [**float**](float.md).</span><span class="sxs-lookup"><span data-stu-id="0ad34-113">For example, if your client application uses a linked list of floating-point numbers, you could specify that the wire-representation of that list be an array of type [**float**](float.md).</span></span> |
| [<span data-ttu-id="0ad34-114">**Marshal d’utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="0ad34-114">**user\_marshal**</span></span>](user-marshal.md)            | <span data-ttu-id="0ad34-115">Contrôle la façon dont les données sont transmises sur le réseau en implémentant vos propres routines de marshaling.</span><span class="sxs-lookup"><span data-stu-id="0ad34-115">Controls how data is transmitted over the wire by implementing your own marshaling routines.</span></span> <span data-ttu-id="0ad34-116">Cet attribut est utile si vous avez un type de données inconnu pour MIDL ou si vous transmettez des informations entre des plateformes Big-endian et Little-endian.</span><span class="sxs-lookup"><span data-stu-id="0ad34-116">This attribute is useful if you have a data type that is unknown to MIDL or if you are passing information between big-endian and little-endian platforms.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="0ad34-117">Les attributs de marshaling DCE [**en \_ ligne**](in-line.md) et [**hors \_ \_ ligne**](out-of-line.md) ne sont pas implémentés dans Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="0ad34-117">The DCE marshaling attributes [**in\_line**](in-line.md) and [**out\_of\_line**](out-of-line.md) are not implemented in Microsoft RPC.</span></span> <span data-ttu-id="0ad34-118">Le compilateur MIDL marshale automatiquement les types de données complexes hors ligne.</span><span class="sxs-lookup"><span data-stu-id="0ad34-118">The MIDL compiler automatically marshals complex data types out-of-line.</span></span>

 

 




