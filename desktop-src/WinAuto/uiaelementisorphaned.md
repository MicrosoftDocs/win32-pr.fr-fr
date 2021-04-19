---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510412"
---
# <a name="uiaelementisorphaned"></a><span data-ttu-id="67b65-103">UiaElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="67b65-103">UiaElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="67b65-104">Texte</span><span class="sxs-lookup"><span data-stu-id="67b65-104">Text</span></span>

<span data-ttu-id="67b65-105">L’élément est un AutomationElement orphelin dans l’arborescence</span><span class="sxs-lookup"><span data-stu-id="67b65-105">Element is an orphaned AutomationElement in the tree</span></span>

## <a name="type"></a><span data-ttu-id="67b65-106">Type</span><span class="sxs-lookup"><span data-stu-id="67b65-106">Type</span></span>

<span data-ttu-id="67b65-107">Error</span><span class="sxs-lookup"><span data-stu-id="67b65-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="67b65-108">Description</span><span class="sxs-lookup"><span data-stu-id="67b65-108">Description</span></span>

<span data-ttu-id="67b65-109">L’adresse de l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de l’objet obtenue pour les coordonnées données est une référence à un élément orphelin dans l’arborescence d’éléments.</span><span class="sxs-lookup"><span data-stu-id="67b65-109">The address of the object's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="67b65-110">Ce problème est un problème pour les personnes qui s’appuient sur un lecteur d’écran et un clavier pour la navigation, car les éléments sont traités comme invisibles et ne sont pas annoncés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67b65-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="67b65-111">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="67b65-111">Possible causes</span></span>

-   <span data-ttu-id="67b65-112">L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.</span><span class="sxs-lookup"><span data-stu-id="67b65-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="67b65-113">Implémentation d’UI Automation incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="67b65-113">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67b65-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67b65-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67b65-115">**IUIAutomationElement.ElementFromPoint**</span><span class="sxs-lookup"><span data-stu-id="67b65-115">**IUIAutomationElement.ElementFromPoint**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




