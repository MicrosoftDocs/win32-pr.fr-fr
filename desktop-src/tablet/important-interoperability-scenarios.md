---
description: 'Pour qu’une application Tablet PC fonctionne avec l’encre de manière efficace, cette application doit être en mesure d’effectuer les opérations suivantes :'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Scénarios d’interopérabilité importants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515981"
---
# <a name="important-interoperability-scenarios"></a><span data-ttu-id="9e206-103">Scénarios d’interopérabilité importants</span><span class="sxs-lookup"><span data-stu-id="9e206-103">Important Interoperability Scenarios</span></span>

<span data-ttu-id="9e206-104">Pour qu’une application Tablet PC fonctionne avec l’encre de manière efficace, cette application doit être en mesure d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e206-104">For a Tablet PC application to operate with ink effectively, that application should be able to:</span></span>

-   <span data-ttu-id="9e206-105">Enregistrez un document au format binaire natif de l’application sans perdre l’encre du document.</span><span class="sxs-lookup"><span data-stu-id="9e206-105">Save a document in the application's native binary format without losing the document's ink.</span></span>
-   <span data-ttu-id="9e206-106">Enregistrez un document dans n’importe quel format que l’application prend normalement en charge (par exemple, au format HTML ou RTF) sans perdre l’encre du document.</span><span class="sxs-lookup"><span data-stu-id="9e206-106">Save a document in any format the application normally supports (for example, HTML or Rich Text Format (RTF)) without losing the document's ink.</span></span>
-   <span data-ttu-id="9e206-107">Copiez l’encre d’une application vers une autre à l’aide du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="9e206-107">Copy ink from one application to another by using the Clipboard.</span></span> <span data-ttu-id="9e206-108">Cela fonctionne si l’autre application reconnaît uniquement un format spécifique, tel que HTML, RTF ou bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="9e206-108">This works if the other application only recognizes a specific format, such as HTML, RTF, or bitmap (BMP).</span></span> <span data-ttu-id="9e206-109">Il fonctionne également si l’application de destination reconnaît l’encre.</span><span class="sxs-lookup"><span data-stu-id="9e206-109">It also works whether the destination application recognizes ink.</span></span> <span data-ttu-id="9e206-110">S’il reconnaît l’encre, l’application de destination est en mesure d’interpréter l’encre qui a été copiée en tant qu’entrée manuscrite, et pas seulement comme une image.</span><span class="sxs-lookup"><span data-stu-id="9e206-110">If it does recognize ink, the destination application is able to interpret the ink that has been copied as ink and not just as an image.</span></span>
-   <span data-ttu-id="9e206-111">Copiez l’encre, avec du texte, entre deux applications qui reconnaissent l’encre, chacune ayant plusieurs objets [**Ink**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="9e206-111">Copy ink, along with text, between two applications that recognize ink, each of which has more than one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="9e206-112">Cela requiert HTML, RTF ou un format similaire.</span><span class="sxs-lookup"><span data-stu-id="9e206-112">This requires HTML, RTF, or a similar format.</span></span>
-   <span data-ttu-id="9e206-113">Copiez l’encre entre deux applications, chacune ayant un objet [**Ink**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="9e206-113">Copy ink between two applications, each of which has one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="9e206-114">Le format ISF (Ink Serialized Format) est suffisant pour cela.</span><span class="sxs-lookup"><span data-stu-id="9e206-114">Ink Serialized Format (ISF) is sufficient for this.</span></span>
-   <span data-ttu-id="9e206-115">Copiez l’encre d’une application qui a plusieurs objets [**Ink**](inkdisp-class.md) vers une application qui n’a qu’un seul objet **Ink** .</span><span class="sxs-lookup"><span data-stu-id="9e206-115">Copy ink from an application that has more than one [**Ink**](inkdisp-class.md) object to an application that has only one **Ink** object.</span></span> <span data-ttu-id="9e206-116">Dans ce cas, l’application qui possède plusieurs objets **Ink** doit pouvoir produire du format ISF (Ink Serialized Format).</span><span class="sxs-lookup"><span data-stu-id="9e206-116">In this case, the application that has more than one **Ink** object must be able to produce Ink Serialized Format (ISF).</span></span>
-   <span data-ttu-id="9e206-117">Copiez l’encre d’une application qui a un objet [**Ink**](inkdisp-class.md) vers une application qui a plusieurs objets **Ink** .</span><span class="sxs-lookup"><span data-stu-id="9e206-117">Copy ink from an application that has one [**Ink**](inkdisp-class.md) object to an application that has more than one **Ink** object.</span></span> <span data-ttu-id="9e206-118">Dans ce cas, l’application qui a plusieurs objets **Ink** doit pouvoir reconnaître ISF.</span><span class="sxs-lookup"><span data-stu-id="9e206-118">In this case, the application that has more than one **Ink** object must be able to recognize ISF.</span></span>

 

 



