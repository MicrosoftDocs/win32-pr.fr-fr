---
title: Référence du plug-in
description: Fonctions d’adaptateur, fonctions wrapper et structures pour créer des adaptateurs de plug-in personnalisés de trois types de moteur, de capteur et de stockage.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API Windows Biometric Framework API Windows Biometric Framework, référence de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462438"
---
# <a name="plug-in-reference"></a><span data-ttu-id="1ddc0-104">Référence du plug-in</span><span class="sxs-lookup"><span data-stu-id="1ddc0-104">Plug-in Reference</span></span>

<span data-ttu-id="1ddc0-105">Les périphériques biométriques sont fabriqués dans un large éventail de types et de configurations.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-105">Biometric devices are manufactured in a wide variety of types and configurations.</span></span> <span data-ttu-id="1ddc0-106">Le Windows Biometric Framework incorpore une architecture extensible qui vous permet de gérer cette variété en créant des plug-ins personnalisés. Au centre de cette architecture se trouve un objet logiciel appelé unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-106">The Windows Biometric Framework incorporates an extensible architecture that enables you to deal with this variety by creating custom plug-ins. At the center of this architecture is a software object called a biometric unit.</span></span> <span data-ttu-id="1ddc0-107">Vous pouvez considérer une unité biométrique comme une abstraction qui représente un périphérique biométrique pour l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-107">You can think of a biometric unit as an abstraction that represents a biometric device to the Framework.</span></span> <span data-ttu-id="1ddc0-108">Les composants logiciels enfichables appelés adaptateurs connectent l’unité biométrique au matériel associé.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-108">Plug-in software components called adapters connect the biometric unit to the associated hardware.</span></span> <span data-ttu-id="1ddc0-109">Il existe trois types d’adaptateurs que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-109">There are three types of adapters that you can create.</span></span> <span data-ttu-id="1ddc0-110">Un adaptateur de moteur génère des modèles biométriques à partir d’exemples capturés, fait correspondre des exemples à des modèles existants et des modèles d’index.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-110">An engine adapter generates biometric templates from captured samples, matches samples to existing templates, and indexes templates.</span></span> <span data-ttu-id="1ddc0-111">Un adaptateur de capteur encapsule un périphérique biométrique et fournit une interface standard pour configurer le capteur, capturer des échantillons et contrôler le workflow de données biométriques pour le moteur de traitement.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-111">A sensor adapter wraps a biometric device and provides a standard interface for configuring the sensor, capturing samples, and controlling the flow of biometric data to the processing engine.</span></span> <span data-ttu-id="1ddc0-112">Un adaptateur de stockage gère les bases de données de modèles.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-112">A storage adapter manages template databases.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1ddc0-113">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1ddc0-113">In this section</span></span>



| <span data-ttu-id="1ddc0-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1ddc0-114">Topic</span></span>                                                                 | <span data-ttu-id="1ddc0-115">Description</span><span class="sxs-lookup"><span data-stu-id="1ddc0-115">Description</span></span>                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ddc0-116">Fonctions de plug-in</span><span class="sxs-lookup"><span data-stu-id="1ddc0-116">Plug-in Functions</span></span>](plug-in-functions.md)<br/>                 | <span data-ttu-id="1ddc0-117">Fonctions que vous pouvez utiliser pour créer les plug-ins d’adaptateur qui composent une unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-117">Functions you can use to create the adapter plug-ins that make up a biometric unit.</span></span><br/>                                                                     |
| [<span data-ttu-id="1ddc0-118">Structures de plug-in</span><span class="sxs-lookup"><span data-stu-id="1ddc0-118">Plug-in Structures</span></span>](plug-in-structures.md)<br/>               | <span data-ttu-id="1ddc0-119">Structures pour le développement d’applications clientes par l’API Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-119">Structures for client application development by the Windows Biometric Framework API.</span></span><br/>                                                                   |
| [<span data-ttu-id="1ddc0-120">Fonctions wrapper de plug-in</span><span class="sxs-lookup"><span data-stu-id="1ddc0-120">Plug-in Wrapper Functions</span></span>](plug-in-wrapper-functions.md)<br/> | <span data-ttu-id="1ddc0-121">Fonctions wrapper qui vous permettent d’appeler une fonction publique sur n’importe quel adaptateur attaché au pipeline sans acquérir manuellement un pointeur vers l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-121">Wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span><br/> |



 

 

 





