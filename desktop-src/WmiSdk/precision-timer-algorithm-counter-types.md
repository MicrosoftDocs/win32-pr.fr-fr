---
description: Les types de compteurs de l’algorithme du minuteur de précision obtiennent des lectures plus précises que les minuteries du système.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Types de compteurs de l’algorithme du minuteur de précision
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759771"
---
# <a name="precision-timer-algorithm-counter-types"></a><span data-ttu-id="49aa3-103">Types de compteurs de l’algorithme du minuteur de précision</span><span class="sxs-lookup"><span data-stu-id="49aa3-103">Precision Timer Algorithm Counter Types</span></span>

<span data-ttu-id="49aa3-104">Les types de compteurs de l’algorithme du minuteur de précision obtiennent des lectures plus précises que les minuteries du système.</span><span class="sxs-lookup"><span data-stu-id="49aa3-104">The precision timer algorithm counter types obtain more accurate readings than system timers.</span></span> <span data-ttu-id="49aa3-105">Le service qui fournit les données fournit également un horodatage, qui élimine les erreurs qui peuvent se produire en raison de la durée de petite et de variable qui s’écoule entre la capture de l’horodateur système et la collecte des données à partir de la DLL de performance.</span><span class="sxs-lookup"><span data-stu-id="49aa3-105">The service that provides the data also provides a timestamp, which eliminates the errors that can occur because of the small and variable time that elapses between capture of the system timestamp and collection of the data from the performance DLL.</span></span> <span data-ttu-id="49aa3-106">Cet horodateur de base pour les timers de précision est une \_ propriété Timestamp de précision de performance \_ , qui doit suivre immédiatement la \_ propriété Timer de précision de performance \_ .</span><span class="sxs-lookup"><span data-stu-id="49aa3-106">This base timestamp for precision timers is a PERF\_PRECISION\_TIMESTAMP property, which must immediately follow the PERF\_PRECISION\_TIMER property.</span></span>



| <span data-ttu-id="49aa3-107">@, Constante</span><span class="sxs-lookup"><span data-stu-id="49aa3-107">CounterType Constant</span></span>                                                                                         | <span data-ttu-id="49aa3-108">Description</span><span class="sxs-lookup"><span data-stu-id="49aa3-108">Description</span></span>                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49aa3-109">[Performances \_ \_ \_ Minuteur système de précision](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 541525248</span><span class="sxs-lookup"><span data-stu-id="49aa3-109">[PERF\_PRECISION\_SYSTEM\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248</span></span><br/> | <span data-ttu-id="49aa3-110">Similaire au \_ minuteur de compteur de performances \_ , sauf qu’il utilise une base de temps définie par compteur au lieu de l’horodateur système.</span><span class="sxs-lookup"><span data-stu-id="49aa3-110">Similar to PERF\_COUNTER\_TIMER except that it uses a counter defined time base instead of the system timestamp.</span></span>             |
| <span data-ttu-id="49aa3-111">[Performances \_ \_ \_ Minuteur de précision 100](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))% décimal 542573824</span><span class="sxs-lookup"><span data-stu-id="49aa3-111">[PERF\_PRECISION\_100NS\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824</span></span><br/>  | <span data-ttu-id="49aa3-112">Semblable au \_ \_ minuteur 100NSEC perf, sauf qu’il utilise une base de temps définie par le compteur de 100 ns au lieu de l’horodateur de la 100 ns du système.</span><span class="sxs-lookup"><span data-stu-id="49aa3-112">Similar to PERF\_100NSEC\_TIMER except that it uses a 100ns counter defined time base instead of the system 100ns timestamp.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="49aa3-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49aa3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49aa3-114">Types de compteurs de performance WMI</span><span class="sxs-lookup"><span data-stu-id="49aa3-114">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

