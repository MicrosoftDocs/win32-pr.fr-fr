---
title: Structures (messages d’entrée de pointeur et notifications)
description: Les rubriques de cette section fournissent les spécifications de référence pour les messages d’entrée de pointeur et les structures de notifications.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106540113"
---
# <a name="pointer-input-messages-and-notifications-structures"></a><span data-ttu-id="3f3a8-103">Messages d’entrée de pointeur et structures de notifications</span><span class="sxs-lookup"><span data-stu-id="3f3a8-103">Pointer Input Messages and Notifications structures</span></span>

<span data-ttu-id="3f3a8-104">Les rubriques de cette section fournissent les spécifications de référence pour les [messages d’entrée de pointeur et](messages-and-notifications-portal.md) les structures de notifications.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3f3a8-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3f3a8-105">In this section</span></span>



| <span data-ttu-id="3f3a8-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3f3a8-106">Topic</span></span>                                                                            | <span data-ttu-id="3f3a8-107">Description</span><span class="sxs-lookup"><span data-stu-id="3f3a8-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f3a8-108">**INPUT_TRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="3f3a8-108">**INPUT_TRANSFORM**</span></span>](/previous-versions/windows/desktop/api)<br/>                           | <span data-ttu-id="3f3a8-109">Définit la matrice qui représente une transformation sur un consommateur de messages.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-109">Defines the matrix that represents a transform on a message consumer.</span></span> <span data-ttu-id="3f3a8-110">Cette matrice peut être utilisée pour transformer des données d’entrée de pointeur de coordonnées clientes en coordonnées d’écran, tandis que l’inverse peut être utilisé pour transformer des données d’entrée de pointeur de coordonnées d’écran en coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-110">This matrix can be used to transform pointer input data from client coordinates to screen coordinates, while the inverse can be used to transform pointer input data from screen coordinates to client coordinates.</span></span> <br/>                                                                 |
| [<span data-ttu-id="3f3a8-111">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="3f3a8-111">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                          | <span data-ttu-id="3f3a8-112">Contient les informations de pointeur de base communes à tous les types pointeur.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-112">Contains basic pointer information common to all pointer types.</span></span> <span data-ttu-id="3f3a8-113">Les applications peuvent récupérer ces informations à l’aide des fonctions [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) et [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="3f3a8-113">Applications can retrieve this information using the [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) and [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) functions.</span></span> <br/> |
| [<span data-ttu-id="3f3a8-114">**POINTER_PEN_INFO**</span><span class="sxs-lookup"><span data-stu-id="3f3a8-114">**POINTER_PEN_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                 | <span data-ttu-id="3f3a8-115">Définit les informations de stylet de base communes à tous les types pointeur.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-115">Defines basic pen information common to all pointer types.</span></span> <br/>                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="3f3a8-116">**POINTER_TOUCH_INFO**</span><span class="sxs-lookup"><span data-stu-id="3f3a8-116">**POINTER_TOUCH_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>             | <span data-ttu-id="3f3a8-117">Définit les informations tactiles de base communes à tous les types pointeur.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-117">Defines basic touch information common to all pointer types.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="3f3a8-118">**TOUCHPREDICTIONPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="3f3a8-118">**TOUCHPREDICTIONPARAMETERS**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="3f3a8-119">Contient des détails d’entrée de matériel qui peuvent être utilisés pour prédire des cibles tactiles et aider à compenser la latence matérielle lors du traitement des entrées tactiles et de mouvement qui contiennent des données de distance et de vélocité.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-119">Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.</span></span><br/>                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="3f3a8-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f3a8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f3a8-121">Référence de message d’entrée de pointeur</span><span class="sxs-lookup"><span data-stu-id="3f3a8-121">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





