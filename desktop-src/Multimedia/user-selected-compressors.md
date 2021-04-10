---
title: Compresseurs User-Selected
description: Compresseurs User-Selected
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Gestionnaire de compression vidéo (VCM), compresseurs sélectionnés par l’utilisateur
- VCM (gestionnaire de compression vidéo), compresseurs sélectionnés par l’utilisateur
- ICCompressorChoose fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940127"
---
# <a name="user-selected-compressors"></a><span data-ttu-id="4e668-106">Compresseurs User-Selected</span><span class="sxs-lookup"><span data-stu-id="4e668-106">User-Selected Compressors</span></span>

<span data-ttu-id="4e668-107">Lorsque vous compressez des données, votre application peut utiliser la fonction [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) pour créer une boîte de dialogue dans laquelle l’utilisateur peut sélectionner le compresseur.</span><span class="sxs-lookup"><span data-stu-id="4e668-107">When compressing data, your application can use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to create a dialog box in which the user can select the compressor.</span></span> <span data-ttu-id="4e668-108">Vous pouvez spécifier des indicateurs pour cette fonction pour permettre à l’utilisateur de spécifier la fréquence d’image clé et le débit de données, ou d’afficher une fenêtre d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="4e668-108">You can specify flags for this function to allow the user to specify the key-frame frequency and the movie-data rate, or to display a preview window.</span></span>

<span data-ttu-id="4e668-109">Le compresseur sélectionné par l’utilisateur est automatiquement ouvert et son descripteur est retourné dans le membre hic de la structure [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) spécifiée dans **ICCompressorChoose**.</span><span class="sxs-lookup"><span data-stu-id="4e668-109">The compressor selected by the user is automatically opened and its handle is returned in the hic member of the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure specified in **ICCompressorChoose**.</span></span>

<span data-ttu-id="4e668-110">Si vous utilisez **ICCompressorChoose**, utilisez la fonction [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) pour fermer le compresseur et libérer toutes les ressources associées à la structure **COMPVARS** .</span><span class="sxs-lookup"><span data-stu-id="4e668-110">If you use **ICCompressorChoose**, use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function to close the compressor and free any resources associated with the **COMPVARS** structure.</span></span>

 

 




