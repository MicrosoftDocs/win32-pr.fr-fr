---
description: En interne, un métafichier est un tableau de structures de longueur variable appelées enregistrements de métafichier.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: À propos des sous-fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753596"
---
# <a name="about-metafiles"></a><span data-ttu-id="a5595-103">À propos des sous-fichiers</span><span class="sxs-lookup"><span data-stu-id="a5595-103">About Metafiles</span></span>

<span data-ttu-id="a5595-104">En interne, un métafichier est un tableau de structures de longueur variable appelées *enregistrements de métafichier*.</span><span class="sxs-lookup"><span data-stu-id="a5595-104">Internally, a metafile is an array of variable-length structures called *metafile records*.</span></span> <span data-ttu-id="a5595-105">Les premiers enregistrements du métafichier spécifient des informations générales, telles que la résolution de l’appareil sur lequel l’image a été créée, les dimensions de l’image, etc.</span><span class="sxs-lookup"><span data-stu-id="a5595-105">The first records in the metafile specify general information such as the resolution of the device on which the picture was created, the dimensions of the picture, and so on.</span></span> <span data-ttu-id="a5595-106">Les enregistrements restants, qui constituent le bloc de tout métafichier, correspondent aux fonctions GDI (Graphics Device Interface) requises pour dessiner l’image.</span><span class="sxs-lookup"><span data-stu-id="a5595-106">The remaining records, which constitute the bulk of any metafile, correspond to the graphics device interface (GDI) functions required to draw the picture.</span></span> <span data-ttu-id="a5595-107">Ces enregistrements sont stockés dans le métafichier après la création d’un contexte de périphérique de métafichier spécial.</span><span class="sxs-lookup"><span data-stu-id="a5595-107">These records are stored in the metafile after a special metafile device context is created.</span></span> <span data-ttu-id="a5595-108">Ce contexte de périphérique de métafichier est ensuite utilisé pour toutes les opérations de dessin nécessaires à la création de l’image.</span><span class="sxs-lookup"><span data-stu-id="a5595-108">This metafile device context is then used for all drawing operations required to create the picture.</span></span> <span data-ttu-id="a5595-109">Lorsque le système traite une fonction GDI associée à un contexte de périphérique de métafichier, il convertit la fonction en données appropriées et stocke ces données dans un enregistrement ajouté au métafichier.</span><span class="sxs-lookup"><span data-stu-id="a5595-109">When the system processes a GDI function associated with a metafile DC, it converts the function into the appropriate data and stores this data in a record appended to the metafile.</span></span>

<span data-ttu-id="a5595-110">Une fois qu’une image est terminée et que le dernier enregistrement est stocké dans le métafichier, vous pouvez transmettre le métafichier à une autre application en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="a5595-110">After a picture is complete and the last record is stored in the metafile, you can pass the metafile to another application by:</span></span>

-   <span data-ttu-id="a5595-111">Utilisation du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a5595-111">Using the clipboard</span></span>
-   <span data-ttu-id="a5595-112">Incorporation dans un autre fichier</span><span class="sxs-lookup"><span data-stu-id="a5595-112">Embedding it within another file</span></span>
-   <span data-ttu-id="a5595-113">Stockage sur disque</span><span class="sxs-lookup"><span data-stu-id="a5595-113">Storing it on disk</span></span>
-   <span data-ttu-id="a5595-114">Sa lecture à plusieurs reprises</span><span class="sxs-lookup"><span data-stu-id="a5595-114">Playing it repeatedly</span></span>

<span data-ttu-id="a5595-115">Un métafichier est *lu* lorsque ses enregistrements sont convertis en commandes de périphérique et traités par l’appareil approprié.</span><span class="sxs-lookup"><span data-stu-id="a5595-115">A metafile is *played* when its records are converted to device commands and processed by the appropriate device.</span></span>

<span data-ttu-id="a5595-116">Il existe deux types de fichiers :</span><span class="sxs-lookup"><span data-stu-id="a5595-116">There are two types of metafiles:</span></span>

-   [<span data-ttu-id="a5595-117">Fichiers de format amélioré</span><span class="sxs-lookup"><span data-stu-id="a5595-117">Enhanced-format metafiles</span></span>](enhanced-format-metafiles.md)
-   [<span data-ttu-id="a5595-118">Fichiers de format Windows</span><span class="sxs-lookup"><span data-stu-id="a5595-118">Windows-format metafiles</span></span>](windows-format-metafiles.md)

 

 



