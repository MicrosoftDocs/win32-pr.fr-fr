---
description: Cette section détaille la version binaire du format de fichier DirectX (. x), telle qu’elle a été introduite dans la version de DirectX 3,0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Encodage Binaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515920"
---
# <a name="binary-encoding"></a><span data-ttu-id="f00d6-103">Encodage Binaire</span><span class="sxs-lookup"><span data-stu-id="f00d6-103">Binary Encoding</span></span>

<span data-ttu-id="f00d6-104">Cette section détaille la version binaire du format de fichier DirectX (. x), telle qu’elle a été introduite dans la version de DirectX 3,0.</span><span class="sxs-lookup"><span data-stu-id="f00d6-104">This section details the binary version of the DirectX (.x) file format as introduced with the release of DirectX 3.0.</span></span>

<span data-ttu-id="f00d6-105">Le format binaire est une représentation sous forme de jeton du format texte.</span><span class="sxs-lookup"><span data-stu-id="f00d6-105">The binary format is a tokenized representation of the text format.</span></span> <span data-ttu-id="f00d6-106">Les jetons peuvent être autonomes ou accompagnés d’enregistrements de données primitifs.</span><span class="sxs-lookup"><span data-stu-id="f00d6-106">Tokens can be stand-alone or accompanied by primitive data records.</span></span> <span data-ttu-id="f00d6-107">Les jetons autonomes donnent une structure grammaticale, et les jetons d’enregistrement fournissent les données nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f00d6-107">Stand-alone tokens give grammatical structure, and record-bearing tokens supply the necessary data.</span></span>

<span data-ttu-id="f00d6-108">Notez que toutes les données sont stockées au format Little endian.</span><span class="sxs-lookup"><span data-stu-id="f00d6-108">Note that all data is stored in little-endian format.</span></span> <span data-ttu-id="f00d6-109">Un flux de données binaires valide se compose d’un en-tête suivi de modèles et/ou d’objets de données.</span><span class="sxs-lookup"><span data-stu-id="f00d6-109">A valid binary data stream consists of a header followed by templates and/or data objects.</span></span>

<span data-ttu-id="f00d6-110">Cette section décrit les composants suivants du format de fichier binaire et fournit un exemple de modèle et d’objet de données binaires.</span><span class="sxs-lookup"><span data-stu-id="f00d6-110">This section discusses the following components of the binary file format and provides an example template and binary data object.</span></span>

-   [<span data-ttu-id="f00d6-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="f00d6-111">Header</span></span>](header.md)
-   [<span data-ttu-id="f00d6-112">Jetons</span><span class="sxs-lookup"><span data-stu-id="f00d6-112">Tokens</span></span>](tokens.md)
-   [<span data-ttu-id="f00d6-113">Enregistrements de jeton</span><span class="sxs-lookup"><span data-stu-id="f00d6-113">Token Records</span></span>](token-records.md)
-   [<span data-ttu-id="f00d6-114">Modèles</span><span class="sxs-lookup"><span data-stu-id="f00d6-114">Templates</span></span>](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [<span data-ttu-id="f00d6-115">Données</span><span class="sxs-lookup"><span data-stu-id="f00d6-115">Data</span></span>](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [<span data-ttu-id="f00d6-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="f00d6-116">Examples</span></span>](examples.md)

## <a name="related-topics"></a><span data-ttu-id="f00d6-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f00d6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f00d6-118">Référence de format de fichier X</span><span class="sxs-lookup"><span data-stu-id="f00d6-118">X File Format Reference</span></span>](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



