---
title: Prise en charge d’ID3
description: ID3 est une organisation qui a défini un ensemble de normes pour inclure les métadonnées dans les fichiers audio MPEG Layer-3 (MP3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Media Format SDK, prise en charge d’ID3
- ASF (Advanced Systems Format), prise en charge d’ID3
- ASF (format des systèmes avancés), prise en charge d’ID3
- métadonnées, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675113"
---
# <a name="id3-support"></a><span data-ttu-id="15710-108">Prise en charge d’ID3</span><span class="sxs-lookup"><span data-stu-id="15710-108">ID3 Support</span></span>

<span data-ttu-id="15710-109">ID3 est une organisation qui a défini un ensemble de normes pour inclure les métadonnées dans les fichiers audio MPEG Layer-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="15710-109">ID3 is an organization that has defined a set of standards for including metadata in MPEG Layer-3 (MP3) audio files.</span></span> <span data-ttu-id="15710-110">Les objets du kit de développement logiciel (SDK) du format Windows Media prennent en charge les attributs compatibles ID3.</span><span class="sxs-lookup"><span data-stu-id="15710-110">The objects of the Windows Media Format SDK provide support for ID3 compatible attributes.</span></span> <span data-ttu-id="15710-111">Trois versions de ID3 distinctes sont prises en charge : ID3v1. x, ID3v 2.2 et ID3v 2.3/v2, 4.</span><span class="sxs-lookup"><span data-stu-id="15710-111">Three distinct ID3 versions are supported: ID3v1.x, ID3v2.2, and ID3v2.3/v2,4.</span></span> <span data-ttu-id="15710-112">Pour obtenir la liste des attributs qui correspondent aux frames ID3, consultez [prise en charge des balises ID3](id3-tag-support.md).</span><span class="sxs-lookup"><span data-stu-id="15710-112">For a list of the attributes that equate to ID3 frames, see [ID3 Tag Support](id3-tag-support.md).</span></span>

<span data-ttu-id="15710-113">Sauf indication contraire, aucune validation des données de trame ID3 n’est effectuée par les objets de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="15710-113">Unless otherwise noted, no validation of ID3 frame data is performed by the objects of this SDK.</span></span> <span data-ttu-id="15710-114">Par exemple, l’attribut de métadonnées [**WM/paroles \_ synchronisées**](wm-lyrics-synchronised.md) stocke les paroles des chansons avec les horodatages correspondants.</span><span class="sxs-lookup"><span data-stu-id="15710-114">For example, the metadata attribute [**WM/Lyrics\_Synchronised**](wm-lyrics-synchronised.md) stores the song lyrics with corresponding time stamps.</span></span> <span data-ttu-id="15710-115">Lors de l’écriture d’un attribut **\_ synchronisé WM/paroles** , les objets de ce kit de développement logiciel (SDK) ne vérifient pas si les horodatages sont dans l’ordre chronologique ou s’ils effectuent la validation de tout type.</span><span class="sxs-lookup"><span data-stu-id="15710-115">When writing a **WM/Lyrics\_Synchronised** attribute, the objects of this SDK will not check to ensure that the time stamps are in chronological order or perform validation of any kind.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15710-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15710-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15710-117">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="15710-117">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="15710-118">**Fonctionnalités de métadonnées**</span><span class="sxs-lookup"><span data-stu-id="15710-118">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="15710-119">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="15710-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




