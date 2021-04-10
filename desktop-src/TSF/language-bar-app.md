---
title: Barre de langue (applications TSF)
description: Une application ne peut pas ajouter d’éléments à la barre de langue ; seul un service de texte peut ajouter des éléments à la barre de langue.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Text Services Framework (TSF), barre de langue
- TSF (Text Services Framework), barre de langue
- Applications compatibles TSF, barre de langue
- barre de langue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103843021"
---
# <a name="language-bar-tsf-applications"></a><span data-ttu-id="91e46-107">Barre de langue (applications TSF)</span><span class="sxs-lookup"><span data-stu-id="91e46-107">Language Bar (TSF Applications)</span></span>

<span data-ttu-id="91e46-108">Une application ne peut pas ajouter d’éléments à la barre de langue ; seul un service de texte peut ajouter des éléments à la barre de langue.</span><span class="sxs-lookup"><span data-stu-id="91e46-108">An application cannot add items to the language bar; only a text service can add items to the language bar.</span></span> <span data-ttu-id="91e46-109">Une application peut avoir un impact sur l’affichage de certains éléments de la barre de langue.</span><span class="sxs-lookup"><span data-stu-id="91e46-109">An application can affect how certain items on the language bar appear.</span></span>

<span data-ttu-id="91e46-110">Le [compartiment \_ \_ \_ DICTATIONSTAT de reconnaissance vocale des compartiments GUID](predefined-compartments.md) est utilisé pour indiquer le type d’entrée vocale que l’application peut accepter : entrée de texte directe (dictée) et/ou commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="91e46-110">The [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment is used to indicate the type of speech input that the application can accept: direct text input (dictation) and/or voice commands.</span></span> <span data-ttu-id="91e46-111">Par défaut, la dictée est activée et la commande vocale est désactivée.</span><span class="sxs-lookup"><span data-stu-id="91e46-111">By default, dictation is enabled and voice command is disabled.</span></span> <span data-ttu-id="91e46-112">Si l’application peut accepter des commandes vocales, elle doit définir la valeur d' [ \_ \_ activation](speech-recognition-constants.md) des commandes TF dans le \_ \_ compartiment DICTATIONSTAT de la reconnaissance vocale des GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="91e46-112">If the application can accept voice commands, it should set the [TF\_COMMANDING\_ENABLED](speech-recognition-constants.md) value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="91e46-113">Si l’application peut accepter la dictée, elle doit définir la \_ valeur de la dictée TF \_ activée dans le \_ \_ \_ compartiment DICTATIONSTAT.</span><span class="sxs-lookup"><span data-stu-id="91e46-113">If the application can accept dictation, it should set the TF\_DICTATION\_ENABLED value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="91e46-114">La \_ dictée TF \_ on ou TF \_ \_ sur la valeur de ce compartiment détermine l’entrée vocale en mode (dictée ou commande) en cours.</span><span class="sxs-lookup"><span data-stu-id="91e46-114">The TF\_DICTATION\_ON or TF\_COMMANDING\_ON value of this compartment determines which mode (dictation or command) speech input is currently in.</span></span>

<span data-ttu-id="91e46-115">Si l’application prend en charge le stockage persistant des données de propriété, elle doit définir le compartiment [ \_ \_ PERSISTMENUENABLED du compartiment GUID](predefined-compartments.md) sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="91e46-115">If the application supports persistent storage of property data, it should set the [GUID\_COMPARTMENT\_PERSISTMENUENABLED](predefined-compartments.md) compartment to a nonzero value.</span></span> <span data-ttu-id="91e46-116">Le service de texte vocal active alors l’élément de menu **enregistrer les données vocales** .</span><span class="sxs-lookup"><span data-stu-id="91e46-116">This causes the speech text service to enable the **Save Speech Data** menu item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91e46-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91e46-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91e46-118">Comment configurer Text Services Framework</span><span class="sxs-lookup"><span data-stu-id="91e46-118">How To Set Up Text Services Framework</span></span>](how-to-set-up-tsf.md)
</dt> <dt>

[<span data-ttu-id="91e46-119">Barre de langue (services de texte)</span><span class="sxs-lookup"><span data-stu-id="91e46-119">Language Bar (Text Services)</span></span>](language-bar.md)
</dt> </dl>

 

 




