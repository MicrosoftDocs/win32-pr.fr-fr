---
title: Attributs de type pointeur
description: Les attributs suivants spécifient les caractéristiques des pointeurs.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL MIDL, attributs, pointer-type
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675770"
---
# <a name="pointer-type-attributes"></a><span data-ttu-id="f4c09-104">Attributs de type pointeur</span><span class="sxs-lookup"><span data-stu-id="f4c09-104">Pointer Type Attributes</span></span>

<span data-ttu-id="f4c09-105">Les attributs suivants spécifient les caractéristiques des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="f4c09-105">The following attributes specify the characteristics of pointers.</span></span>



| <span data-ttu-id="f4c09-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="f4c09-106">Attribute</span></span>                                   | <span data-ttu-id="f4c09-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="f4c09-107">Usage</span></span>                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4c09-108">**ptr**</span><span class="sxs-lookup"><span data-stu-id="f4c09-108">**ptr**</span></span>](ptr.md)                          | <span data-ttu-id="f4c09-109">Désigne un pointeur comme pointeur complet, avec toutes les fonctionnalités d’un pointeur en langage C, y compris les alias.</span><span class="sxs-lookup"><span data-stu-id="f4c09-109">Designates a pointer as a full pointer, with all the capabilities of a C-language pointer, including aliasing.</span></span>                                                                                       |
| [<span data-ttu-id="f4c09-110">**ref**</span><span class="sxs-lookup"><span data-stu-id="f4c09-110">**ref**</span></span>](ref.md)                          | <span data-ttu-id="f4c09-111">Désigne le type de pointeur le plus simple dans MIDL, un qui fournit simplement l’adresse de certaines données.</span><span class="sxs-lookup"><span data-stu-id="f4c09-111">Designates the simplest type of pointer in MIDL—one that simply provides the address of some data.</span></span> <span data-ttu-id="f4c09-112">Les pointeurs de référence ne peuvent jamais avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f4c09-112">Reference pointers can never be null.</span></span>                                                             |
| [<span data-ttu-id="f4c09-113">**unique**</span><span class="sxs-lookup"><span data-stu-id="f4c09-113">**unique**</span></span>](unique.md)                    | <span data-ttu-id="f4c09-114">Permet à un pointeur d’avoir la valeur null, mais ne prend pas en charge les alias.</span><span class="sxs-lookup"><span data-stu-id="f4c09-114">Lets a pointer be null, but does not support aliasing.</span></span>                                                                                                                                               |
| [<span data-ttu-id="f4c09-115">**pointeur \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="f4c09-115">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="f4c09-116">Appliqué à une interface pour spécifier le type de pointeur par défaut pour tous les pointeurs de cette interface, à l’exception des pointeurs de paramètre de niveau supérieur, qui sont automatiquement par défaut des pointeurs [**ref**](ref.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c09-116">Applied to an interface to specify the default pointer type for all pointers in that interface, except for top-level parameter pointers, which automatically default to [**ref**](ref.md) pointers.</span></span> |
| [<span data-ttu-id="f4c09-117">**IID \_ est**</span><span class="sxs-lookup"><span data-stu-id="f4c09-117">**iid\_is**</span></span>](iid-is.md)                   | <span data-ttu-id="f4c09-118">Fournit l’identificateur d’interface de l’interface COM qui est l’objet du pointeur.</span><span class="sxs-lookup"><span data-stu-id="f4c09-118">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                                                                                            |
| [<span data-ttu-id="f4c09-119">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4c09-119">**string**</span></span>](string.md)                    | <span data-ttu-id="f4c09-120">Spécifie que le pointeur pointe vers une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f4c09-120">Specifies that the pointer points to a string.</span></span>                                                                                                                                                       |



 

 

 




