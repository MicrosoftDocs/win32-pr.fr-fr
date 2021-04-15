---
title: Balise LST
description: Balise LST
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507222"
---
# <a name="lst-tag"></a><span data-ttu-id="b7f3d-103">Balise LST</span><span class="sxs-lookup"><span data-stu-id="b7f3d-103">Lst Tag</span></span>

<span data-ttu-id="b7f3d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b7f3d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b7f3d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b7f3d-106">Répète la dernière instruction orale pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-106">Repeats last spoken statement for the character.</span></span>

</dd> <dt>

<span data-ttu-id="b7f3d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b7f3d-108">\\**LST**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-108">\\**Lst**</span></span>\\

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="b7f3d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b7f3d-109">Remarks</span></span>

<span data-ttu-id="b7f3d-110">Cette balise permet à un caractère de répéter sa dernière instruction orale.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-110">This tag enables a character to repeat its last spoken statement.</span></span> <span data-ttu-id="b7f3d-111">Cette balise doit apparaître seule dans la méthode [**Speak**](speak-method.md) ; aucun autre texte ou paramètre ne peut être inclus.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-111">This tag must appear by itself in the [**Speak**](speak-method.md) method; no other text or parameters can be included.</span></span> <span data-ttu-id="b7f3d-112">Lorsque le texte parlé est répété, toutes les autres balises incluses dans le texte d’origine sont répétées, à l’exception des signets.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-112">When the spoken text is repeated, any other tags included in the original text are repeated, except for bookmarks.</span></span> <span data-ttu-id="b7f3d-113">Aux. WAV et. Les fichiers LWV inclus dans le texte sont également répétés.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-113">Any .WAV and .LWV files included in the text are also repeated.</span></span>

 

 




