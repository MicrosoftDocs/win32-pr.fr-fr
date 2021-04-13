---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- Identificateur UIA_NamePropertyId AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380285"
---
# <a name="uianamelengthtoolong"></a><span data-ttu-id="09f22-104">UiaNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="09f22-104">UiaNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="09f22-105">Texte</span><span class="sxs-lookup"><span data-stu-id="09f22-105">Text</span></span>

<span data-ttu-id="09f22-106">Le nom de l’élément ne doit pas retourner une chaîne de plus de {0} caractères</span><span class="sxs-lookup"><span data-stu-id="09f22-106">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="09f22-107">Type</span><span class="sxs-lookup"><span data-stu-id="09f22-107">Type</span></span>

<span data-ttu-id="09f22-108">Error</span><span class="sxs-lookup"><span data-stu-id="09f22-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="09f22-109">Description</span><span class="sxs-lookup"><span data-stu-id="09f22-109">Description</span></span>

<span data-ttu-id="09f22-110">Le nom d’un élément contient trop de caractères.</span><span class="sxs-lookup"><span data-stu-id="09f22-110">The name of an element contains too many characters.</span></span> <span data-ttu-id="09f22-111">Par exemple, la méthode [**IUIAutomationElement :: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) utilisée pour récupérer le nom UIA d’un élément retourne une chaîne supérieure à la limite.</span><span class="sxs-lookup"><span data-stu-id="09f22-111">For example, the [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) method used to retrieve the UIA name of an element returns a string greater than the limit.</span></span>

<span data-ttu-id="09f22-112">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un élément peut avoir un nom non significatif et non intuitif.</span><span class="sxs-lookup"><span data-stu-id="09f22-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="09f22-113">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="09f22-113">Possible causes</span></span>

<span data-ttu-id="09f22-114">Un nom ou une étiquette n’est pas assigné à l’élément ou à son parent.</span><span class="sxs-lookup"><span data-stu-id="09f22-114">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09f22-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09f22-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09f22-116">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="09f22-116">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="09f22-117">**IUIAutomationElement::CurrentName**</span><span class="sxs-lookup"><span data-stu-id="09f22-117">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




