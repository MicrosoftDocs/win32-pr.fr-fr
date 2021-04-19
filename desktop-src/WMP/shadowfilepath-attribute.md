---
title: Attribut ShadowFilePath
description: L’attribut ShadowFilePath est le chemin d’accès complet à un fichier caché.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Attribut ShadowFilePath lecteur Windows Media
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537474"
---
# <a name="shadowfilepath-attribute"></a><span data-ttu-id="345e0-104">Attribut ShadowFilePath</span><span class="sxs-lookup"><span data-stu-id="345e0-104">ShadowFilePath Attribute</span></span>

<span data-ttu-id="345e0-105">L’attribut **ShadowFilePath** est le chemin d’accès complet à un fichier caché.</span><span class="sxs-lookup"><span data-stu-id="345e0-105">The **ShadowFilePath** attribute is the fully qualified path to a shadow file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="345e0-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="345e0-106">Applies To</span></span>

-   [<span data-ttu-id="345e0-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="345e0-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="345e0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="345e0-108">Remarks</span></span>

<span data-ttu-id="345e0-109">Un *fichier caché* est créé dans le cadre d’une conversion de format de fichier.</span><span class="sxs-lookup"><span data-stu-id="345e0-109">A *shadow file* is created as part of a file format conversion.</span></span> <span data-ttu-id="345e0-110">Il s’agit de la copie d’un fichier que le lecteur utilise lorsque l’utilisateur synchronise le contenu de l’ordinateur sur un appareil qui requiert que le contenu soit au format de fichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="345e0-110">It is the copy of a file that the Player uses when the user syncs content from the computer to a device that requires the content to be in the original file format.</span></span> <span data-ttu-id="345e0-111">Cet attribut est défini pour que le fichier converti pointe vers l’emplacement du fichier caché.</span><span class="sxs-lookup"><span data-stu-id="345e0-111">This attribute is set for the converted file to point to the location of the shadow file.</span></span>

<span data-ttu-id="345e0-112">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="345e0-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="345e0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="345e0-113">Requirements</span></span>



| <span data-ttu-id="345e0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="345e0-114">Requirement</span></span> | <span data-ttu-id="345e0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="345e0-115">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="345e0-116">Version</span><span class="sxs-lookup"><span data-stu-id="345e0-116">Version</span></span><br/> | <span data-ttu-id="345e0-117">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="345e0-117">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="345e0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="345e0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345e0-119">**À propos du processus de conversion**</span><span class="sxs-lookup"><span data-stu-id="345e0-119">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="345e0-120">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="345e0-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





