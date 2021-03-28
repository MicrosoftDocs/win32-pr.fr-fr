---
description: Enhanced-Format les sous-fichiers
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Enhanced-Format les sous-fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972686"
---
# <a name="enhanced-format-metafiles"></a><span data-ttu-id="9e9c0-103">Enhanced-Format les sous-fichiers</span><span class="sxs-lookup"><span data-stu-id="9e9c0-103">Enhanced-Format Metafiles</span></span>

<span data-ttu-id="9e9c0-104">Le *métafichier de format amélioré* se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9e9c0-104">The *enhanced-format metafile* consists of the following elements:</span></span>

-   <span data-ttu-id="9e9c0-105">Un en-tête</span><span class="sxs-lookup"><span data-stu-id="9e9c0-105">A header</span></span>
-   <span data-ttu-id="9e9c0-106">Tableau de handles vers des objets GDI</span><span class="sxs-lookup"><span data-stu-id="9e9c0-106">A table of handles to GDI objects</span></span>
-   <span data-ttu-id="9e9c0-107">Une palette privée</span><span class="sxs-lookup"><span data-stu-id="9e9c0-107">A private palette</span></span>
-   <span data-ttu-id="9e9c0-108">Tableau d’enregistrements de métafichier</span><span class="sxs-lookup"><span data-stu-id="9e9c0-108">An array of metafile records</span></span>

<span data-ttu-id="9e9c0-109">Les sous-fichiers améliorés fournissent une véritable indépendance des appareils.</span><span class="sxs-lookup"><span data-stu-id="9e9c0-109">Enhanced metafiles provide true device independence.</span></span> <span data-ttu-id="9e9c0-110">Vous pouvez considérer l’image stockée dans un métafichier amélioré comme un « instantané » de l’affichage vidéo pris à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="9e9c0-110">You can think of the picture stored in an enhanced metafile as a "snapshot" of the video display taken at a particular moment.</span></span> <span data-ttu-id="9e9c0-111">Cet instantané conserve ses dimensions, quel que soit l’endroit où il apparaît sur une imprimante, un traceur, le bureau ou dans la zone cliente d’une application.</span><span class="sxs-lookup"><span data-stu-id="9e9c0-111">This "snapshot" maintains its dimensions no matter where it appears on a printer, a plotter, the desktop, or in the client area of any application.</span></span>

<span data-ttu-id="9e9c0-112">Vous pouvez utiliser des fichiers de base de fichiers améliorés pour stocker une image créée à l’aide des fonctions GDI (y compris les nouvelles fonctions de transformation et de chemin d’accès).</span><span class="sxs-lookup"><span data-stu-id="9e9c0-112">You can use enhanced metafiles to store a picture created by using the GDI functions (including new path and transformation functions).</span></span> <span data-ttu-id="9e9c0-113">Étant donné que le format de métafichier amélioré est standardisé, les images stockées dans ce format peuvent être copiées d’une application à une autre. en effet, étant donné que les images sont véritablement indépendantes des appareils, elles sont assurées de conserver leur forme et leur proportion sur n’importe quel périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="9e9c0-113">Because the enhanced metafile format is standardized, pictures that are stored in this format can be copied from one application to another; and, because the pictures are truly device independent, they are guaranteed to maintain their shape and proportion on any output device.</span></span>

-   [<span data-ttu-id="9e9c0-114">Enregistrements de métafichiers améliorés</span><span class="sxs-lookup"><span data-stu-id="9e9c0-114">Enhanced Metafile Records</span></span>](enhanced-metafile-records.md)
-   [<span data-ttu-id="9e9c0-115">Création de métafichiers améliorée</span><span class="sxs-lookup"><span data-stu-id="9e9c0-115">Enhanced Metafile Creation</span></span>](enhanced-metafile-creation.md)
-   [<span data-ttu-id="9e9c0-116">Opérations de métafichier améliorées</span><span class="sxs-lookup"><span data-stu-id="9e9c0-116">Enhanced Metafile Operations</span></span>](enhanced-metafile-operations.md)

 

 



