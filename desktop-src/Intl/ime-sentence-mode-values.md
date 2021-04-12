---
description: Ces valeurs sont utilisées avec les fonctions ImmGetConversionStatus et ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valeurs du mode de phrase IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203075"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="1bbd2-103">Valeurs du mode de phrase IME</span><span class="sxs-lookup"><span data-stu-id="1bbd2-103">IME Sentence Mode Values</span></span>

<span data-ttu-id="1bbd2-104">Ces valeurs sont utilisées avec les fonctions [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) et [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="1bbd2-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="1bbd2-105">Constante</span><span class="sxs-lookup"><span data-stu-id="1bbd2-105">Constant</span></span>                  | <span data-ttu-id="1bbd2-106">Définition</span><span class="sxs-lookup"><span data-stu-id="1bbd2-106">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="1bbd2-107">\_SMODE IME \_ automatique</span><span class="sxs-lookup"><span data-stu-id="1bbd2-107">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="1bbd2-108">L’IME effectue le traitement de la conversion en mode automatique.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-108">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="1bbd2-109">\_SMODE IME \_ aucun</span><span class="sxs-lookup"><span data-stu-id="1bbd2-109">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="1bbd2-110">Aucune information pour la phrase.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-110">No information for sentence.</span></span>                                               |
| <span data-ttu-id="1bbd2-111">IME \_ SMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="1bbd2-111">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="1bbd2-112">L’IME utilise les informations d’expression pour prédire le caractère suivant.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-112">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="1bbd2-113">IME \_ SMODE \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="1bbd2-113">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="1bbd2-114">L’IME utilise des informations de clause pluriel pour effectuer le traitement de la conversion.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-114">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="1bbd2-115">IME \_ SMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="1bbd2-115">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="1bbd2-116">L’IME effectue le traitement de la conversion en mode à un seul caractère.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-116">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="1bbd2-117">\_conversation SMODE \_ IME</span><span class="sxs-lookup"><span data-stu-id="1bbd2-117">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="1bbd2-118">L’IME utilise le mode conversation.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-118">The IME uses conversation mode.</span></span> <span data-ttu-id="1bbd2-119">Cela est utile pour les applications de conversation.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-119">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="1bbd2-120">Les bits 16 à 31 sont réservés à l’utilisation de l’IME.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-120">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



