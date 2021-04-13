---
title: Découpage automatique
description: Découpage automatique
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310677"
---
# <a name="automatic-clipping"></a><span data-ttu-id="24885-103">Découpage automatique</span><span class="sxs-lookup"><span data-stu-id="24885-103">Automatic Clipping</span></span>

<span data-ttu-id="24885-104">Il est fortement recommandé qu’un conteneur de contrôles ActiveX prenne en charge le découpage automatique de ses contrôles.</span><span class="sxs-lookup"><span data-stu-id="24885-104">It is strongly recommended that an ActiveX control container supports automatic clipping of its controls.</span></span> <span data-ttu-id="24885-105">Cela entraînera une opération plus efficace pour la plupart des contrôles.</span><span class="sxs-lookup"><span data-stu-id="24885-105">This will result in more efficient operation for most controls.</span></span> <span data-ttu-id="24885-106">Si le découpage automatique est pris en charge, la propriété ambiante autoclip doit être prise en charge et avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="24885-106">If automatic clipping is supported, the AutoClip ambient property must be supported and have a value of **TRUE**.</span></span>

<span data-ttu-id="24885-107">Le découpage automatique est la capacité d’un conteneur à s’assurer que la sortie dessinée d’un contrôle passe uniquement à la zone de découpage actuelle du conteneur.</span><span class="sxs-lookup"><span data-stu-id="24885-107">Automatic clipping is the ability of a container to ensure that a control's drawn output goes only to the container's current clipping region.</span></span> <span data-ttu-id="24885-108">Dans un conteneur qui prend en charge le découpage automatique, un contrôle peut peindre sans tenir compte de sa zone de découpage, car le conteneur détourne automatiquement tout dessin qui se produit en dehors de la zone du contrôle.</span><span class="sxs-lookup"><span data-stu-id="24885-108">In a container that supports automatic clipping, a control can paint without regard to its clipping region, because the container will automatically clip any painting that occurs outside the control's area.</span></span> <span data-ttu-id="24885-109">Si un conteneur ne prend pas en charge le découpage automatique, les contrôles générés par le CDK créeront une fenêtre parente supplémentaire si une région de découpage non null est passée.</span><span class="sxs-lookup"><span data-stu-id="24885-109">If a container does not support automatic clipping, then CDK-generated controls will create an extra parent window if a non-null clipping region is passed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24885-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24885-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24885-111">Containers</span><span class="sxs-lookup"><span data-stu-id="24885-111">Containers</span></span>](containers.md)
</dt> </dl>

 

 




