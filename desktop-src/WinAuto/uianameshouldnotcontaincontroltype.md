---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839722"
---
# <a name="uianameshouldnotcontaincontroltype"></a><span data-ttu-id="9a55b-103">UiaNameShouldNotContainControlType</span><span class="sxs-lookup"><span data-stu-id="9a55b-103">UiaNameShouldNotContainControlType</span></span>

## <a name="text"></a><span data-ttu-id="9a55b-104">Texte</span><span class="sxs-lookup"><span data-stu-id="9a55b-104">Text</span></span>

<span data-ttu-id="9a55b-105">Le nom de l’élément ( {0} ) ne doit pas contenir le texte du ControlType ( {1} )</span><span class="sxs-lookup"><span data-stu-id="9a55b-105">Element's Name ({0}) should not contain the text of the ControlType ({1})</span></span>

## <a name="type"></a><span data-ttu-id="9a55b-106">Type</span><span class="sxs-lookup"><span data-stu-id="9a55b-106">Type</span></span>

<span data-ttu-id="9a55b-107">Avertissement</span><span class="sxs-lookup"><span data-stu-id="9a55b-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="9a55b-108">Description</span><span class="sxs-lookup"><span data-stu-id="9a55b-108">Description</span></span>

<span data-ttu-id="9a55b-109">Le nom d’un élément intègre son type de contrôle UIA.</span><span class="sxs-lookup"><span data-stu-id="9a55b-109">The name of an element incorporates its UIA control type.</span></span> <span data-ttu-id="9a55b-110">Par exemple, cet avertissement peut se produire si la propriété de nom UIA pour un élément avec le type de contrôle Button est définie sur « My Button ».</span><span class="sxs-lookup"><span data-stu-id="9a55b-110">For example, this warning can occur if the UIA Name property for an element with the Button control type is set to "My Button".</span></span>

<span data-ttu-id="9a55b-111">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car le type de contrôle est lu deux fois, ou il peut être non significatif ou non intuitif pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9a55b-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the control type will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9a55b-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="9a55b-112">Possible causes</span></span>

-   <span data-ttu-id="9a55b-113">Un nom ou une étiquette n’est pas assigné à l’élément ou à son parent.</span><span class="sxs-lookup"><span data-stu-id="9a55b-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="9a55b-114">L’élément ou son parent a un nom par défaut qui n’a pas été révisé à un nom convivial.</span><span class="sxs-lookup"><span data-stu-id="9a55b-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="9a55b-115">Par exemple, bouton 1.</span><span class="sxs-lookup"><span data-stu-id="9a55b-115">For example, button1.</span></span>
-   <span data-ttu-id="9a55b-116">Un développeur ne sait pas que les lecteurs d’écran lisent les noms et les types de contrôle.</span><span class="sxs-lookup"><span data-stu-id="9a55b-116">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a55b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a55b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a55b-118">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a55b-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="9a55b-119">**IUIAutomationElement::CurrentName**</span><span class="sxs-lookup"><span data-stu-id="9a55b-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




