---
description: Une alternative est une correspondance de mot potentielle pour un segment de reconnaissance. Un module de reconnaissance génère des alternatives et les base sur des correspondances acceptables de l’entrée d’encre ou audio par rapport à un dictionnaire ou un Factoid.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350c9ac97f0af1451a0ded6445cf658dad4ee4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513335"
---
# <a name="alternates"></a><span data-ttu-id="2d3b0-104">Alternatives</span><span class="sxs-lookup"><span data-stu-id="2d3b0-104">Alternates</span></span>

<span data-ttu-id="2d3b0-105">Une alternative est une correspondance de mot potentielle pour un segment de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-105">An alternate is a potential word match for a recognition segment.</span></span> <span data-ttu-id="2d3b0-106">Un module de reconnaissance génère des alternatives et les base sur des correspondances acceptables de l’entrée d’encre ou audio par rapport à un dictionnaire ou un Factoid.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-106">A recognizer generates alternates and bases them on acceptable matches of the ink or audio input against a dictionary or factoid.</span></span>

> [!Note]  
> <span data-ttu-id="2d3b0-107">La version d’évaluation de la confiance est actuellement disponible uniquement pour l’anglais Microsoft (États-Unis) et les module de reconnaissance de mouvement.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-107">Confidence evaluation is currently available only for the Microsoft English (United States) and gesture recognizers.</span></span>

 

<span data-ttu-id="2d3b0-108">Parfois, l’encre peut avoir des distinctions ambiguës entre les segments.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-108">Sometimes the ink may have ambiguous distinctions between segments.</span></span> <span data-ttu-id="2d3b0-109">Le module de reconnaissance compare ces segments à un dictionnaire de reconnaissance pour déterminer les correspondances possibles.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-109">The recognizer compares these segments to a recognizer dictionary to determine possible matches.</span></span> <span data-ttu-id="2d3b0-110">Lorsque le module de reconnaissance compare les segments, il gère une liste de correspondances alternatives possibles et attribue un niveau de confiance à chacun d’eux, en choisissant un niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-110">When the recognizer compares the segments, it maintains a list of possible alternate matches and assigns a confidence level to each one, picking a top choice.</span></span>

> [!Note]  
> <span data-ttu-id="2d3b0-111">Le module de reconnaissance ne peut pas fournir de remplacements pour une partie de l’encre inférieure à un segment de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-111">The recognizer cannot provide alternates for a portion of ink that is smaller than a recognition segment.</span></span>

 

 

 



