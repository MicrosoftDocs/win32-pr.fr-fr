---
title: Interfaces IAVIStream et IAVIFile
description: Interfaces IAVIStream et IAVIFile
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Interface IAVIStream
- Interface IAVIFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840242"
---
# <a name="iavistream-and-iavifile-interfaces"></a><span data-ttu-id="eb735-105">Interfaces IAVIStream et IAVIFile</span><span class="sxs-lookup"><span data-stu-id="eb735-105">IAVIStream and IAVIFile Interfaces</span></span>

<span data-ttu-id="eb735-106">Les interfaces [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) et [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) contiennent les méthodes utilisées par les gestionnaires de fichiers et de flux.</span><span class="sxs-lookup"><span data-stu-id="eb735-106">The [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) and [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) interfaces contain the methods used by file and stream handlers.</span></span> <span data-ttu-id="eb735-107">Le type de données **PAVISTREAM** est un pointeur vers un objet de flux AVI (via l’interface **IAVIStream** ) et le type de données **PAVIFILE** est un pointeur vers un objet fichier AVI (via l’interface **IAVIFile** ).</span><span class="sxs-lookup"><span data-stu-id="eb735-107">The **PAVISTREAM** data type is a pointer to an AVI stream object (through the **IAVIStream** interface) and the **PAVIFILE** data type is a pointer to an AVI file object (through the **IAVIFile** interface).</span></span>

<span data-ttu-id="eb735-108">Pour créer un pointeur d’objet en C, commencez par allouer de l’espace pour une structure suffisamment grande pour contenir le pointeur vers la table de fonctions virtuelles et les autres membres de données.</span><span class="sxs-lookup"><span data-stu-id="eb735-108">To create an object pointer in C, first allocate space for a structure that is large enough to contain the pointer to the virtual function table and the other data members.</span></span> <span data-ttu-id="eb735-109">Créez une table de fonctions virtuelles pour les méthodes de votre type de flux, puis définissez le pointeur vers la table de fonctions virtuelles sur l’adresse de la table de fonctions virtuelles.</span><span class="sxs-lookup"><span data-stu-id="eb735-109">Create a virtual function table for the methods for your type of stream, then set the pointer to the virtual function table to the address of the virtual function table.</span></span>

 

 




