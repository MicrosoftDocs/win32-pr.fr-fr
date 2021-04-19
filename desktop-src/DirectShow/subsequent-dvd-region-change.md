---
description: Modification de la région du DVD suivante
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Modification de la région du DVD suivante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a28982d6807fa5d90356d15cbf5365a595c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534104"
---
# <a name="subsequent-dvd-region-change"></a><span data-ttu-id="caf0d-103">Modification de la région du DVD suivante</span><span class="sxs-lookup"><span data-stu-id="caf0d-103">Subsequent DVD Region Change</span></span>

<span data-ttu-id="caf0d-104">Dans Windows 2000 et versions ultérieures, le navigateur DVD appelle une page de propriétés sur le lecteur de DVD-ROM dans le Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="caf0d-104">In Windows 2000 and later, the DVD Navigator invokes a property page on the DVD-ROM drive device in the Device Manager.</span></span> <span data-ttu-id="caf0d-105">Cette page de propriétés est également mise en place par l’application DVDPlay.exe lorsqu’une région doit être modifiée.</span><span class="sxs-lookup"><span data-stu-id="caf0d-105">This property page is also brought up by the DVDPlay.exe application when a region needs to be changed.</span></span> <span data-ttu-id="caf0d-106">L’interface utilisateur de cette page de propriétés est très similaire à celle de DVDRgn.exe et elle est régionale dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="caf0d-106">The UI of this property page is very similar to that of DVDRgn.exe and it is regionalized in the operating system.</span></span>

<span data-ttu-id="caf0d-107">Pour les lecteurs RPC1, les composants du système d’exploitation Windows gèrent les modifications de région.</span><span class="sxs-lookup"><span data-stu-id="caf0d-107">For RPC1 drives, the Windows Operating System components manage region changes.</span></span> <span data-ttu-id="caf0d-108">Les lecteurs RPC2 maintiennent le paramètre de région dans leur propre matériel.</span><span class="sxs-lookup"><span data-stu-id="caf0d-108">RPC2 drives maintain the region setting in their own hardware.</span></span> <span data-ttu-id="caf0d-109">Lorsque le nombre de modifications autorisées est épuisé sur un lecteur RPC2, le lecteur échouera en cas d’échec de l’appel pour modifier la région et le composant Region-change dans le système d’exploitation indiquera qu’à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="caf0d-109">When the number of allowed changes are exhausted on a RPC2 drive, the drive will fail the call to change the region and the region-change component in the operating system will indicate that to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="caf0d-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="caf0d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caf0d-111">Prise en charge des modifications de région de DVD dans Windows</span><span class="sxs-lookup"><span data-stu-id="caf0d-111">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



