---
description: Les fonctions suivantes vous permettent d’énumérer les ressources protégées.
ms.assetid: 6806c320-6071-4075-9003-2469089a9cc4
title: Fonctions WRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966e25d0c9c78e384c38098b43826f1e6342c9b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953054"
---
# <a name="wrp-functions"></a><span data-ttu-id="7abb5-103">Fonctions WRP</span><span class="sxs-lookup"><span data-stu-id="7abb5-103">WRP Functions</span></span>

<span data-ttu-id="7abb5-104">Les fonctions suivantes vous permettent d’énumérer les ressources protégées.</span><span class="sxs-lookup"><span data-stu-id="7abb5-104">The following functions allow you to enumerate protected resources.</span></span>



| <span data-ttu-id="7abb5-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="7abb5-105">Function</span></span>                                         | <span data-ttu-id="7abb5-106">Description</span><span class="sxs-lookup"><span data-stu-id="7abb5-106">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="7abb5-107">**SfcIsFileProtected**</span><span class="sxs-lookup"><span data-stu-id="7abb5-107">**SfcIsFileProtected**</span></span>](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) | <span data-ttu-id="7abb5-108">Détermine si le fichier spécifié est protégé.</span><span class="sxs-lookup"><span data-stu-id="7abb5-108">Determines whether the specified file is protected.</span></span>         |
| [<span data-ttu-id="7abb5-109">**SfcIsKeyProtected**</span><span class="sxs-lookup"><span data-stu-id="7abb5-109">**SfcIsKeyProtected**</span></span>](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected)   | <span data-ttu-id="7abb5-110">Détermine si la clé de Registre spécifiée est protégée.</span><span class="sxs-lookup"><span data-stu-id="7abb5-110">Determines whether the specified registry key is protected.</span></span> |



 

<span data-ttu-id="7abb5-111">S’il est disponible pour le système d’exploitation, les fonctions de cette table doivent être utilisées à la place des fonctions déconseillées : [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) et [**SfcGetFiles**](sfcgetfiles.md).</span><span class="sxs-lookup"><span data-stu-id="7abb5-111">If available for the operating system, the functions in this table should be used rather than the deprecated functions: [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) and [**SfcGetFiles**](sfcgetfiles.md).</span></span>

 

 



