---
title: Balise CTX
description: Balise CTX
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029450"
---
# <a name="ctx-tag"></a><span data-ttu-id="cfaa6-103">Balise CTX</span><span class="sxs-lookup"><span data-stu-id="cfaa6-103">Ctx Tag</span></span>

<span data-ttu-id="cfaa6-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cfaa6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="cfaa6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="cfaa6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="cfaa6-106">Définit le contexte du texte de sortie.</span><span class="sxs-lookup"><span data-stu-id="cfaa6-106">Sets the context of the output text.</span></span>

</dd> <dt>

<span data-ttu-id="cfaa6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="cfaa6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="cfaa6-108">\\**CTX** = *chaîne*</span><span class="sxs-lookup"><span data-stu-id="cfaa6-108">\\**Ctx**=*string*</span></span>\\



| <span data-ttu-id="cfaa6-109">Partie</span><span class="sxs-lookup"><span data-stu-id="cfaa6-109">Part</span></span>     | <span data-ttu-id="cfaa6-110">Description</span><span class="sxs-lookup"><span data-stu-id="cfaa6-110">Description</span></span>                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfaa6-111">*string*</span><span class="sxs-lookup"><span data-stu-id="cfaa6-111">*string*</span></span> | <span data-ttu-id="cfaa6-112">Chaîne spécifiant le contexte du texte qui suit, qui détermine la façon dont les symboles ou les abréviations sont prononcés.</span><span class="sxs-lookup"><span data-stu-id="cfaa6-112">A string specifying the context of the text that follows, which determines how symbols or abbreviations are spoken.</span></span><br/> <span data-ttu-id="cfaa6-113">**« Address »**    Adresses et/ou numéros de téléphone.</span><span class="sxs-lookup"><span data-stu-id="cfaa6-113">**"Address"**    Addresses and/or phone numbers.</span></span><br/> <span data-ttu-id="cfaa6-114">**« E-mail »**    Courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="cfaa6-114">**"E-mail"**    Electronic mail.</span></span><br/> <span data-ttu-id="cfaa6-115">Le contexte **« inconnu »** (par défaut) est inconnu.</span><span class="sxs-lookup"><span data-stu-id="cfaa6-115">**"Unknown"**    (Default) Context is unknown.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="cfaa6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cfaa6-116">Remarks</span></span>

<span data-ttu-id="cfaa6-117">Cette balise est prise en charge uniquement pour la sortie générée par TTS.</span><span class="sxs-lookup"><span data-stu-id="cfaa6-117">This tag is supported only for TTS-generated output.</span></span> <span data-ttu-id="cfaa6-118">La plage de valeurs du paramètre peut varier selon le moteur TTS installé.</span><span class="sxs-lookup"><span data-stu-id="cfaa6-118">The range of values for the parameter may vary depending on the installed TTS engine.</span></span>

 

 





