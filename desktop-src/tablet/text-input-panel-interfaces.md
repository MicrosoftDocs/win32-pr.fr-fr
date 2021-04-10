---
description: Cette section contient des informations sur les interfaces utilisées pour contrôler l’apparence et le comportement du panneau de saisie Tablet PC.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Interfaces du panneau de saisie de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210600"
---
# <a name="text-input-panel-interfaces"></a><span data-ttu-id="600f6-103">Interfaces du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="600f6-103">Text Input Panel Interfaces</span></span>

<span data-ttu-id="600f6-104">Cette section contient des informations sur les interfaces utilisées pour contrôler l’apparence et le comportement du panneau de saisie Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="600f6-104">This section contains information about the interfaces used to control the appearance and behavior of the Tablet PC Input Panel.</span></span>

> [!Note]  
> <span data-ttu-id="600f6-105">Les interfaces du panneau de saisie de texte ne sont pas compatibles avec Automation.</span><span class="sxs-lookup"><span data-stu-id="600f6-105">The Text Input Panel interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="600f6-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="600f6-106">In This Section</span></span>



| <span data-ttu-id="600f6-107">Interface</span><span class="sxs-lookup"><span data-stu-id="600f6-107">Interface</span></span>                                                                | <span data-ttu-id="600f6-108">Description</span><span class="sxs-lookup"><span data-stu-id="600f6-108">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="600f6-109">**Interface IHandWrittenTextInsertion**</span><span class="sxs-lookup"><span data-stu-id="600f6-109">**IHandWrittenTextInsertion Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | <span data-ttu-id="600f6-110">Utilisé par le code d’entrée de texte personnalisé de l’application pour insérer le texte dans le champ de texte et dans le magasin de stockage des services de texte.</span><span class="sxs-lookup"><span data-stu-id="600f6-110">Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store.</span></span><br/> |
| [<span data-ttu-id="600f6-111">**Interface ITextInputPanel**</span><span class="sxs-lookup"><span data-stu-id="600f6-111">**ITextInputPanel Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | <span data-ttu-id="600f6-112">Permet de contrôler le panneau de saisie Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="600f6-112">Provides control over the Tablet PC Input Panel.</span></span><br/>                                                                                  |
| [<span data-ttu-id="600f6-113">**Interface ITextInputPanelEventSink**</span><span class="sxs-lookup"><span data-stu-id="600f6-113">**ITextInputPanelEventSink Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | <span data-ttu-id="600f6-114">Définit des méthodes qui gèrent les événements de l' [**interface ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .</span><span class="sxs-lookup"><span data-stu-id="600f6-114">Defines methods that handle the [**ITextInputPanel Interface**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) events.</span></span><br/>                                      |
| [<span data-ttu-id="600f6-115">**Interface ITextInputPanelRunInfo**</span><span class="sxs-lookup"><span data-stu-id="600f6-115">**ITextInputPanelRunInfo Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | <span data-ttu-id="600f6-116">Fournit une méthode pour déterminer si le panneau de saisie de texte est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="600f6-116">Provides a method to determine if the Text Input Panel is currently running.</span></span><br/>                                                      |
| [<span data-ttu-id="600f6-117">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="600f6-117">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)       | <span data-ttu-id="600f6-118">Permet au client d’appeler l’objet fournisseur de saisie semi-automatique du panneau de saisie du texte de l’application.</span><span class="sxs-lookup"><span data-stu-id="600f6-118">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="600f6-119">**Interface ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="600f6-119">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)   | <span data-ttu-id="600f6-120">Gère le côté de l’application de l’intégration de la saisie semi-automatique du panneau de saisie de texte.</span><span class="sxs-lookup"><span data-stu-id="600f6-120">Manages the application's side of the Text Input Panel auto complete integration.</span></span><br/>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="600f6-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="600f6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="600f6-122">Référence du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="600f6-122">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




