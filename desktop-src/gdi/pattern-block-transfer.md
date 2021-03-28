---
description: Le nom de la fonction PatBlt (abréviation pour le transfert de bloc de modèle) implique que cette fonction réplique simplement le pinceau (ou le modèle) jusqu’à ce qu’elle remplisse un rectangle spécifié.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Transfert de bloc de modèle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991189"
---
# <a name="pattern-block-transfer"></a><span data-ttu-id="f916e-103">Transfert de bloc de modèle</span><span class="sxs-lookup"><span data-stu-id="f916e-103">Pattern Block Transfer</span></span>

<span data-ttu-id="f916e-104">Le nom de la fonction [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (abréviation pour le transfert de bloc de modèle) implique que cette fonction réplique simplement le pinceau (ou le modèle) jusqu’à ce qu’elle remplisse un rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="f916e-104">The name of the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function (an abbreviation for pattern block transfer) implies that this function simply replicates the brush (or pattern) until it fills a specified rectangle.</span></span> <span data-ttu-id="f916e-105">Toutefois, la fonction est en fait bien plus puissante.</span><span class="sxs-lookup"><span data-stu-id="f916e-105">However, the function is actually much more powerful.</span></span> <span data-ttu-id="f916e-106">Avant de répliquer le pinceau, il combine les données de couleur du modèle avec les données de couleur des pixels existants sur l’affichage vidéo à l’aide d’une opération de pixellisation (ROP).</span><span class="sxs-lookup"><span data-stu-id="f916e-106">Before replicating the brush, it combines the color data for the pattern with the color data for the existing pixels on the video display by using a raster operation (ROP).</span></span> <span data-ttu-id="f916e-107">Une ROP est une opération au niveau du bit qui est appliquée aux bits des données de couleur pour le pinceau répliqué et les bits des données de couleur du rectangle cible sur le périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f916e-107">An ROP is a bitwise operation that is applied to the bits of color data for the replicated brush and the bits of color data for the target rectangle on the display device.</span></span> <span data-ttu-id="f916e-108">Il y a 256 trames ; Toutefois, la fonction **PatBlt** ne reconnaît que ceux qui nécessitent un modèle et une destination (pas ceux qui requièrent une source).</span><span class="sxs-lookup"><span data-stu-id="f916e-108">There are 256 ROPs; however, the **PatBlt** function recognizes only those that require a pattern and a destination (not those that require a source).</span></span> <span data-ttu-id="f916e-109">Le tableau suivant identifie les opérations de tramage les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="f916e-109">The following table identifies the most common ROPs.</span></span>



| <span data-ttu-id="f916e-110">ROP</span><span class="sxs-lookup"><span data-stu-id="f916e-110">ROP</span></span>       | <span data-ttu-id="f916e-111">Description</span><span class="sxs-lookup"><span data-stu-id="f916e-111">Description</span></span>                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f916e-112">PATCOPY</span><span class="sxs-lookup"><span data-stu-id="f916e-112">PATCOPY</span></span>   | <span data-ttu-id="f916e-113">Copie le modèle dans le bitmap de destination.</span><span class="sxs-lookup"><span data-stu-id="f916e-113">Copies the pattern to the destination bitmap.</span></span>                                       |
| <span data-ttu-id="f916e-114">PATINVERT</span><span class="sxs-lookup"><span data-stu-id="f916e-114">PATINVERT</span></span> | <span data-ttu-id="f916e-115">Associe le bitmap de destination au modèle à l’aide de l’opérateur booléen XOR.</span><span class="sxs-lookup"><span data-stu-id="f916e-115">Combines the destination bitmap with the pattern by using the Boolean XOR operator.</span></span> |
| <span data-ttu-id="f916e-116">DSTINVERT</span><span class="sxs-lookup"><span data-stu-id="f916e-116">DSTINVERT</span></span> | <span data-ttu-id="f916e-117">Inverse le bitmap de destination.</span><span class="sxs-lookup"><span data-stu-id="f916e-117">Inverts the destination bitmap.</span></span>                                                     |
| <span data-ttu-id="f916e-118">NOIRCEUR</span><span class="sxs-lookup"><span data-stu-id="f916e-118">BLACKNESS</span></span> | <span data-ttu-id="f916e-119">Transforme toutes les sorties en zéros binaires.</span><span class="sxs-lookup"><span data-stu-id="f916e-119">Turns all output to binary zeros.</span></span>                                                   |
| <span data-ttu-id="f916e-120">BLANCHEté</span><span class="sxs-lookup"><span data-stu-id="f916e-120">WHITENESS</span></span> | <span data-ttu-id="f916e-121">Transforme toutes les sorties en fichiers binaires.</span><span class="sxs-lookup"><span data-stu-id="f916e-121">Turns all output to binary ones.</span></span>                                                    |



 

<span data-ttu-id="f916e-122">Pour plus d’informations, consultez [codes d’opération Raster](raster-operation-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f916e-122">For more information, see [Raster Operation Codes](raster-operation-codes.md).</span></span>

 

 



