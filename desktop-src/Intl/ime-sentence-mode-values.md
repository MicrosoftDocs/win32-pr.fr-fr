---
description: Passez en revue la liste des valeurs du mode phrase de l’éditeur de méthode d’entrée (IME). Ces valeurs sont utilisées avec les fonctions ImmGetConversionStatus et ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valeurs du mode de phrase IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406762"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="e1c06-104">Valeurs du mode de phrase IME</span><span class="sxs-lookup"><span data-stu-id="e1c06-104">IME Sentence Mode Values</span></span>

<span data-ttu-id="e1c06-105">Ces valeurs sont utilisées avec les fonctions [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) et [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="e1c06-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="e1c06-106">Constante</span><span class="sxs-lookup"><span data-stu-id="e1c06-106">Constant</span></span>                  | <span data-ttu-id="e1c06-107">Définition</span><span class="sxs-lookup"><span data-stu-id="e1c06-107">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="e1c06-108">\_SMODE IME \_ automatique</span><span class="sxs-lookup"><span data-stu-id="e1c06-108">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="e1c06-109">L’IME effectue le traitement de la conversion en mode automatique.</span><span class="sxs-lookup"><span data-stu-id="e1c06-109">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="e1c06-110">\_SMODE IME \_ aucun</span><span class="sxs-lookup"><span data-stu-id="e1c06-110">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="e1c06-111">Aucune information pour la phrase.</span><span class="sxs-lookup"><span data-stu-id="e1c06-111">No information for sentence.</span></span>                                               |
| <span data-ttu-id="e1c06-112">IME \_ SMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="e1c06-112">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="e1c06-113">L’IME utilise les informations d’expression pour prédire le caractère suivant.</span><span class="sxs-lookup"><span data-stu-id="e1c06-113">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="e1c06-114">IME \_ SMODE \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="e1c06-114">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="e1c06-115">L’IME utilise des informations de clause pluriel pour effectuer le traitement de la conversion.</span><span class="sxs-lookup"><span data-stu-id="e1c06-115">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="e1c06-116">IME \_ SMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="e1c06-116">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="e1c06-117">L’IME effectue le traitement de la conversion en mode à un seul caractère.</span><span class="sxs-lookup"><span data-stu-id="e1c06-117">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="e1c06-118">\_conversation SMODE \_ IME</span><span class="sxs-lookup"><span data-stu-id="e1c06-118">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="e1c06-119">L’IME utilise le mode conversation.</span><span class="sxs-lookup"><span data-stu-id="e1c06-119">The IME uses conversation mode.</span></span> <span data-ttu-id="e1c06-120">Cela est utile pour les applications de conversation.</span><span class="sxs-lookup"><span data-stu-id="e1c06-120">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="e1c06-121">Les bits 16 à 31 sont réservés à l’utilisation de l’IME.</span><span class="sxs-lookup"><span data-stu-id="e1c06-121">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



