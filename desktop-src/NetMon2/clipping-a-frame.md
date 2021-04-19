---
description: Vous pouvez spécifier que le pilote découpe les frames.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Découpage d’un frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517829"
---
# <a name="clipping-a-frame"></a><span data-ttu-id="383eb-103">Découpage d’un frame</span><span class="sxs-lookup"><span data-stu-id="383eb-103">Clipping a Frame</span></span>

<span data-ttu-id="383eb-104">Vous pouvez spécifier que le pilote découpe les frames.</span><span class="sxs-lookup"><span data-stu-id="383eb-104">You can specify that the driver clip the frames.</span></span> <span data-ttu-id="383eb-105">(Si les autres sections de filtre de capture sont omises, il peut s’agir de la seule fonction de votre filtre de capture).</span><span class="sxs-lookup"><span data-stu-id="383eb-105">(If the other capture filter sections are omitted, this may be the only function of your capture filter).</span></span> <span data-ttu-id="383eb-106">Si le champ **nFrameBytesToCopy** n’est pas égal à zéro (0), sa valeur spécifie le nombre d’octets de chaque trame reçus à conserver.</span><span class="sxs-lookup"><span data-stu-id="383eb-106">If the **nFrameBytesToCopy** field is not zero (0), its value specifies how many bytes of each frame received to retain.</span></span> <span data-ttu-id="383eb-107">Si le champ est égal à zéro, le frame entier est conservé.</span><span class="sxs-lookup"><span data-stu-id="383eb-107">If the field is zero, then the whole frame is retained.</span></span>

> [!Note]  
> <span data-ttu-id="383eb-108">Vous pouvez découper n’importe quel frame qui transmet les autres parties de votre filtre de capture en définissant **nFrameBytesToCopy**.</span><span class="sxs-lookup"><span data-stu-id="383eb-108">You may clip any frame that passes the other portions of your capture filter by setting **nFrameBytesToCopy**.</span></span>

 

 

 



