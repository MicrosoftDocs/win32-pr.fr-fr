---
description: Les horodatages sont normalement inclus lorsqu’un fichier est signé à l’aide de SignTool avec l’option-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Ajout d’horodatages à des fichiers précédemment signés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106522560"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a><span data-ttu-id="b8d0c-103">Ajout d’horodatages à des fichiers précédemment signés</span><span class="sxs-lookup"><span data-stu-id="b8d0c-103">Adding Time Stamps to Previously Signed Files</span></span>

<span data-ttu-id="b8d0c-104">Les horodatages sont normalement inclus lorsqu’un fichier est signé à l’aide de SignTool avec l’option **-t** .</span><span class="sxs-lookup"><span data-stu-id="b8d0c-104">Time stamps are normally included when a file is signed using SignTool with the **-t** option.</span></span> <span data-ttu-id="b8d0c-105">En outre, des horodatages peuvent être ajoutés aux fichiers qui ont été signés sans horodatage.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-105">In addition, time stamps can be added to files that were signed without a time stamp.</span></span> <span data-ttu-id="b8d0c-106">La commande suivante ajoute un horodatage à un fichier précédemment signé :</span><span class="sxs-lookup"><span data-stu-id="b8d0c-106">The following command adds a time stamp to a previously signed file:</span></span>

<span data-ttu-id="b8d0c-107">**l’horodateur SignTool-t https : \/ /timestamp.digicert.com *MyControl.exe***</span><span class="sxs-lookup"><span data-stu-id="b8d0c-107">**signtool timestamp -t https:\//timestamp.digicert.com *MyControl.exe***</span></span>

> [!Note]  
> <span data-ttu-id="b8d0c-108">Le fichier à horodatage doit avoir été signé précédemment.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-108">The file to be time stamped must have previously been signed.</span></span>

 

<span data-ttu-id="b8d0c-109">Pour plus d’informations sur SignTool, consultez [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="b8d0c-109">For more information about SignTool, see [SignTool](signtool.md).</span></span>

 

 



