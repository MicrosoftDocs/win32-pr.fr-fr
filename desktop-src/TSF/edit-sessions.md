---
title: Sessions de modification
description: Lorsqu’un service de texte doit obtenir, modifier ou définir du texte dans un contexte, il doit demander une session d’édition.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- Text Services Framework (TSF), modifier la session
- TSF (Text Services Framework), modifier la session
- services de texte, modifier la session
- session d'édition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507423"
---
# <a name="edit-sessions"></a><span data-ttu-id="40a04-107">Sessions de modification</span><span class="sxs-lookup"><span data-stu-id="40a04-107">Edit Sessions</span></span>

<span data-ttu-id="40a04-108">Lorsqu’un service de texte doit obtenir, modifier ou définir du texte dans un contexte, il doit demander une *session d’édition*.</span><span class="sxs-lookup"><span data-stu-id="40a04-108">When a text service must obtain, modify, or set text in a context, it must request an *edit session*.</span></span> <span data-ttu-id="40a04-109">Lorsqu’une session d’édition est demandée, le gestionnaire TSF négocie avec le propriétaire du contexte cible pour un verrou de document du type demandé.</span><span class="sxs-lookup"><span data-stu-id="40a04-109">When an edit session is requested, the TSF manager negotiates with the owner of the target context for a document lock of the requested type.</span></span> <span data-ttu-id="40a04-110">Lorsque le verrou de document est accordé, le gestionnaire de TSF permet au service de texte de lire et/ou d’écrire du texte dans le contexte.</span><span class="sxs-lookup"><span data-stu-id="40a04-110">When the document lock is granted, the TSF manager enables the text service to read and/or write text to or from the context.</span></span>

 

 




