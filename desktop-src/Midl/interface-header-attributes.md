---
title: Attributs d’en-tête d’interface
description: Incorporez ces attributs dans l’en-tête d’interface pour transmettre des informations sur l’interface entière.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL MIDL, attributs, en-tête d’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029016"
---
# <a name="interface-header-attributes"></a><span data-ttu-id="d4e3d-104">Attributs d’en-tête d’interface</span><span class="sxs-lookup"><span data-stu-id="d4e3d-104">Interface Header Attributes</span></span>

<span data-ttu-id="d4e3d-105">Incorporez ces attributs dans l’en-tête d’interface pour transmettre des informations sur l’interface entière.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-105">Incorporate these attributes in the interface header to convey information about the entire interface.</span></span>



| <span data-ttu-id="d4e3d-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="d4e3d-106">Attribute</span></span>                                   | <span data-ttu-id="d4e3d-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="d4e3d-107">Usage</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4e3d-108">**\_UUID asynchrone**</span><span class="sxs-lookup"><span data-stu-id="d4e3d-108">**async\_uuid**</span></span>](async-uuid.md)           | <span data-ttu-id="d4e3d-109">Indique au compilateur MIDL de définir à la fois les versions synchrones et asynchrones d’une interface COM.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-109">Directs the MIDL compiler to define both synchronous and asynchronous versions of a COM interface.</span></span>                                                                                                                                               |
| [<span data-ttu-id="d4e3d-110">**universel**</span><span class="sxs-lookup"><span data-stu-id="d4e3d-110">**uuid**</span></span>](uuid.md)                        | <span data-ttu-id="d4e3d-111">Désigne une valeur 128 bits qui distingue une interface particulière des autres.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-111">Designates a 128-bit value that distinguishes a particular interface from all others.</span></span> <span data-ttu-id="d4e3d-112">La valeur réelle peut représenter un GUID, un CLSID ou un IID.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-112">The actual value may represent a GUID, a CLSID, or an IID.</span></span>                                                                                                 |
| [<span data-ttu-id="d4e3d-113">**localisé**</span><span class="sxs-lookup"><span data-stu-id="d4e3d-113">**local**</span></span>](local.md)                      | <span data-ttu-id="d4e3d-114">Indique au compilateur MIDL de générer uniquement des fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-114">Directs the MIDL compiler to generate header files only.</span></span> <span data-ttu-id="d4e3d-115">Une interface doit avoir un [**UUID**](uuid.md) ou un attribut [**local**](local.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e3d-115">An interface must have either a [**uuid**](uuid.md) or a [**local**](local.md) attribute.</span></span>                                                                                             |
| [<span data-ttu-id="d4e3d-116">**MS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="d4e3d-116">**ms\_union**</span></span>](-ms-union.md)              | <span data-ttu-id="d4e3d-117">Contrôle l’alignement du rapport de non-remise des unions non encapsulées.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-117">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="d4e3d-118">Utilisez pour la compatibilité descendante avec les interfaces basées sur MIDL 1,0 ou 2,0.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-118">Use for backward compatibility with interfaces built on MIDL 1.0 or 2.0.</span></span>                                                                                                                   |
| [<span data-ttu-id="d4e3d-119">**object**</span><span class="sxs-lookup"><span data-stu-id="d4e3d-119">**object**</span></span>](object.md)                    | <span data-ttu-id="d4e3d-120">Identifie l’interface en tant qu’interface COM et indique au compilateur MIDL de générer le code proxy/stub au lieu des stubs du client et du serveur RPC.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-120">Identifies the interface as a COM interface and directs the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span>                                                                                                    |
| [<span data-ttu-id="d4e3d-121">**Version**</span><span class="sxs-lookup"><span data-stu-id="d4e3d-121">**version**</span></span>](version.md)                  | <span data-ttu-id="d4e3d-122">Identifie une version particulière d’une interface dans les cas où plusieurs versions de l’interface existent.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-122">Identifies a particular version of an interface in cases where multiple versions of the interface exist.</span></span> <span data-ttu-id="d4e3d-123">Étant donné que les interfaces COM sont immuables, vous ne pouvez pas utiliser l’attribut [**version**](version.md) sur une interface d' [**objet**](object.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e3d-123">Because COM interfaces are immutable, you cannot use the [**version**](version.md) attribute on an [**object**](object.md) interface.</span></span> |
| [<span data-ttu-id="d4e3d-124">**pointeur \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="d4e3d-124">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="d4e3d-125">Spécifie le type de pointeur par défaut pour tous les pointeurs, à l’exception de ceux inclus dans les listes de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-125">Specifies the default pointer type for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="d4e3d-126">Le type par défaut peut être [**unique**](unique.md), [**ref**](ref.md)ou [**ptr**](ptr.md).</span><span class="sxs-lookup"><span data-stu-id="d4e3d-126">The default type can be [**unique**](unique.md), [**ref**](ref.md), or [**ptr**](ptr.md).</span></span>                                                   |
| [<span data-ttu-id="d4e3d-127">**poste**</span><span class="sxs-lookup"><span data-stu-id="d4e3d-127">**endpoint**</span></span>](endpoint.md)                | <span data-ttu-id="d4e3d-128">Spécifie un point de terminaison statique (connu) sur lequel une application serveur doit écouter les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-128">Specifies a static (well-known) endpoint on which a server application will listen for remote procedure calls.</span></span>                                                                                                                                   |



 

<span data-ttu-id="d4e3d-129">Consultez les [attributs de bibliothèque de types](type-library-attributes.md) pour les attributs d’interface, tels que [**double**](dual.md) et [**oleautomation**](oleautomation.md), qui sont spécifiques aux interfaces définies ou référencées dans une instruction de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d4e3d-129">See [Type Library Attributes](type-library-attributes.md) for interface attributes, such as [**dual**](dual.md) and [**oleautomation**](oleautomation.md), that are specific to interfaces defined or referenced inside a library statement.</span></span>

 

 




