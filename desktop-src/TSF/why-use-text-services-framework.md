---
title: Pourquoi utiliser Text Services Framework
description: Pourquoi utiliser Text Services Framework
ms.assetid: 64b3b0a1-7740-49fa-b0a6-f80040147280
keywords:
- Text Services Framework (TSF), à propos de
- TSF (Text Services Framework), à propos de
- services de texte, à propos de
- Applications compatibles TSF, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6647981b890bd1fcdf488b18bffad587f49ed9b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106537747"
---
# <a name="why-use-text-services-framework"></a><span data-ttu-id="8156f-107">Pourquoi utiliser Text Services Framework ?</span><span class="sxs-lookup"><span data-stu-id="8156f-107">Why Use Text Services Framework?</span></span>

<span data-ttu-id="8156f-108">Text Services Framework (TSF) permet à une application compatible TSF de recevoir l’entrée de texte à partir d’un nombre quelconque d’appareils ou de sources.</span><span class="sxs-lookup"><span data-stu-id="8156f-108">Text Services Framework (TSF) enables a TSF-enabled application to receive text input from any number of devices or sources.</span></span> <span data-ttu-id="8156f-109">Étant donné que TSF est extensible, l’application peut recevoir des entrées de texte de sources de texte supplémentaires avec peu ou pas de modifications.</span><span class="sxs-lookup"><span data-stu-id="8156f-109">Because TSF is extensible, the application can receive text input from additional text sources with little or no modification.</span></span>

<span data-ttu-id="8156f-110">Un service de texte obtient du texte à partir de, et fournit du texte à, toute application compatible TSF sans avoir besoin de connaître l’application.</span><span class="sxs-lookup"><span data-stu-id="8156f-110">A text service obtains text from, and provides text to, any TSF-enabled application without requiring any knowledge about the application.</span></span> <span data-ttu-id="8156f-111">Cette structure permet au service de texte d’être disponible pour n’importe quelle application compatible avec TSF.</span><span class="sxs-lookup"><span data-stu-id="8156f-111">This structure enables the text service to be available to any TSF-enabled application.</span></span> <span data-ttu-id="8156f-112">Le service de texte peut être installé ou mis à jour en tant que module distinct et indépendant de toute application spécifique.</span><span class="sxs-lookup"><span data-stu-id="8156f-112">The text service can be installed or updated as a separate module and is independent of any specific application.</span></span> <span data-ttu-id="8156f-113">TSF permet également à un service de texte de stocker des métadonnées avec un document, un morceau de texte ou un objet dans le document.</span><span class="sxs-lookup"><span data-stu-id="8156f-113">TSF also enables a text service to store metadata with a document, a piece of text, or an object within the document.</span></span> <span data-ttu-id="8156f-114">Par exemple, un service de texte d’entrée vocale peut stocker des informations audio associées à un bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="8156f-114">For example, a speech input text service can store sound information associated with a block of text.</span></span>

<span data-ttu-id="8156f-115">TSF permet aux services de texte de fournir une conversion de texte exacte et complète, avec un accès continu à la mémoire tampon de document.</span><span class="sxs-lookup"><span data-stu-id="8156f-115">TSF enables text services to provide accurate and complete text conversion, with continuous access to the document buffer.</span></span> <span data-ttu-id="8156f-116">Les services de texte utilisant TSF peuvent éviter de séparer leurs fonctionnalités en modes d’entrée et de mode de modification.</span><span class="sxs-lookup"><span data-stu-id="8156f-116">Text services using TSF can avoid separating their functionality into modes for input and modes for editing.</span></span> <span data-ttu-id="8156f-117">Cette architecture d’entrée permet à la mise en mémoire tampon et à l’accumulation du flux de texte de changer de manière dynamique, ce qui permet une entrée de clavier plus efficace et une modification de texte.</span><span class="sxs-lookup"><span data-stu-id="8156f-117">This input architecture enables the buffered and accumulating text stream to change dynamically, thereby enabling more efficient keyboard input and text editing.</span></span>

<span data-ttu-id="8156f-118">TSF est indépendant des appareils et active les services de texte pour plusieurs périphériques d’entrée, y compris le clavier, le stylet et le microphone.</span><span class="sxs-lookup"><span data-stu-id="8156f-118">TSF is device-independent and enables text services for multiple input devices including keyboard, pen, and microphone.</span></span>

 

 




