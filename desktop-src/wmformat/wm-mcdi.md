---
title: WM/MCDI
description: L’attribut WM/MCDI contient l’identificateur de CD de musique. Il s’agit d’un vidage binaire de la table des matières à partir du CD qui est utilisé pour identifier de manière unique le CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Format Windows Media WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106522631"
---
# <a name="wmmcdi"></a><span data-ttu-id="d7583-105">WM/MCDI</span><span class="sxs-lookup"><span data-stu-id="d7583-105">WM/MCDI</span></span>

<span data-ttu-id="d7583-106">L’attribut **WM/MCDI** contient l’identificateur de CD de musique.</span><span class="sxs-lookup"><span data-stu-id="d7583-106">The **WM/MCDI** attribute contains the music CD identifier.</span></span> <span data-ttu-id="d7583-107">Il s’agit d’un vidage binaire de la table des matières à partir du CD qui est utilisé pour identifier de manière unique le CD.</span><span class="sxs-lookup"><span data-stu-id="d7583-107">This is a binary dump of the table of contents from the CD that is used to uniquely identify the CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d7583-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="d7583-108">Global Constant</span></span>

<span data-ttu-id="d7583-109">\_wszWMMCDI g</span><span class="sxs-lookup"><span data-stu-id="d7583-109">g\_wszWMMCDI</span></span>

## <a name="data-type"></a><span data-ttu-id="d7583-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="d7583-110">Data Type</span></span>

<span data-ttu-id="d7583-111">**\_binaire de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d7583-111">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="d7583-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d7583-112">Remarks</span></span>

<span data-ttu-id="d7583-113">Cet attribut est compatible avec le frame ID3, MCDI.</span><span class="sxs-lookup"><span data-stu-id="d7583-113">This attribute is compatible with the ID3 frame, MCDI.</span></span> <span data-ttu-id="d7583-114">La spécification ID3 du frame MCDI nécessite qu’une seule trame de ce type existe pour chaque fichier et qu’une trame TRCK valide existe.</span><span class="sxs-lookup"><span data-stu-id="d7583-114">The ID3 specification for the MCDI frame requires that only one such frame exist per file and that a valid TRCK frame exist.</span></span> <span data-ttu-id="d7583-115">L’éditeur de métadonnées n’effectue aucune validation pour ces règles.</span><span class="sxs-lookup"><span data-stu-id="d7583-115">The metadata editor does not perform any validation for these rules.</span></span> <span data-ttu-id="d7583-116">En outre, la taille de WM/MCDI n’est pas limitée à 804 octets, tout comme le cadre MCDI ID3.</span><span class="sxs-lookup"><span data-stu-id="d7583-116">Also, the size of WM/MCDI is not limited to 804 bytes, as is the MCDI ID3 frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7583-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7583-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7583-118">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="d7583-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




