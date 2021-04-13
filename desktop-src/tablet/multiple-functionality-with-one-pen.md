---
description: Le stylet d’un Tablet PC peut avoir plusieurs extrémités pouvant interagir avec le digitaliseur.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Fonctionnalités multiples avec un stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320929"
---
# <a name="multiple-functionality-with-one-pen"></a><span data-ttu-id="379b2-103">Fonctionnalités multiples avec un stylet</span><span class="sxs-lookup"><span data-stu-id="379b2-103">Multiple Functionality with One Pen</span></span>

<span data-ttu-id="379b2-104">Le stylet d’un Tablet PC peut avoir plusieurs extrémités pouvant interagir avec le digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="379b2-104">A Tablet PC pen may have more than one end that can interact with the digitizer.</span></span> <span data-ttu-id="379b2-105">Si les deux extrémités du stylet peuvent générer des événements, une extrémité peut être utilisée pour définir l’encre, sélectionner et pointer, et l’autre extrémité peut être utilisée pour d’autres fonctions telles que l’effacement.</span><span class="sxs-lookup"><span data-stu-id="379b2-105">If both ends of the pen can generate events, one end may be used to lay down ink, select, and point, and the other end may be used for other functions such as erasing.</span></span>

<span data-ttu-id="379b2-106">Pour implémenter cette fonctionnalité, votre application doit être en mesure de déterminer la fin du stylet qui est utilisée et, par conséquent, de modifier l’apparence du curseur.</span><span class="sxs-lookup"><span data-stu-id="379b2-106">To implement such functionality, your application must be able to determine which end of the pen is being used and hence when to change the appearance of the cursor.</span></span> <span data-ttu-id="379b2-107">Pour ce faire, il peut Rechercher l’état de la propriété [**inversée**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) sur l’objet [**curseur**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="379b2-107">It can do this by looking for the state of the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

<span data-ttu-id="379b2-108">Pour plus d’informations sur l’utilisation de l’arrière du stylet pour l’effacement, consultez [effacement de l’encre avec le stylet](erasing-ink-with-the-pen.md).</span><span class="sxs-lookup"><span data-stu-id="379b2-108">For specific details about using the back of the pen for erasing, see [Erasing Ink with the Pen](erasing-ink-with-the-pen.md).</span></span> <span data-ttu-id="379b2-109">En outre, l' [exemple d’effacement d’encre](ink-erasing-sample.md) montre comment utiliser l’arrière du stylet pour effacer l’encre.</span><span class="sxs-lookup"><span data-stu-id="379b2-109">In addition, the [Ink Erasing Sample](ink-erasing-sample.md) demonstrates how to use the back of the pen to erase ink.</span></span>

 

 



