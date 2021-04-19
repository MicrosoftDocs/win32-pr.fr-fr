---
title: Interface IDWriteLocalFontFileLoader
description: Implémentation intégrée de l’interface IDWriteFontFileLoader, qui opère sur des fichiers de polices locales et expose des informations de fichier de police locale à partir de la clé de référence du fichier de police.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Écriture directe de l’interface IDWriteLocalFontFileLoader
- Écriture directe de l’interface IDWriteLocalFontFileLoader, décrite
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535257"
---
# <a name="idwritelocalfontfileloader-interface"></a><span data-ttu-id="b0b05-105">Interface IDWriteLocalFontFileLoader</span><span class="sxs-lookup"><span data-stu-id="b0b05-105">IDWriteLocalFontFileLoader interface</span></span>

<span data-ttu-id="b0b05-106">Implémentation intégrée de l’interface [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , qui opère sur des fichiers de polices locales et expose des informations de fichier de police locale à partir de la clé de référence du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="b0b05-106">A built-in implementation of the [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) interface, that operates on local font files and exposes local font file information from the font file reference key.</span></span> <span data-ttu-id="b0b05-107">Les références de fichiers de polices créées à l’aide de [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) utilisent ce chargeur de fichier de police.</span><span class="sxs-lookup"><span data-stu-id="b0b05-107">Font file references created using [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) use this font file loader.</span></span>

## <a name="members"></a><span data-ttu-id="b0b05-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b0b05-108">Members</span></span>

<span data-ttu-id="b0b05-109">L’interface **IDWriteLocalFontFileLoader** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b0b05-109">The **IDWriteLocalFontFileLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b0b05-110">**IDWriteLocalFontFileLoader** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b0b05-110">**IDWriteLocalFontFileLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="b0b05-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b0b05-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b0b05-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b0b05-112">Methods</span></span>

<span data-ttu-id="b0b05-113">L’interface **IDWriteLocalFontFileLoader** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b0b05-113">The **IDWriteLocalFontFileLoader** interface has these methods.</span></span>



| <span data-ttu-id="b0b05-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="b0b05-114">Method</span></span>                                                                                  | <span data-ttu-id="b0b05-115">Description</span><span class="sxs-lookup"><span data-stu-id="b0b05-115">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0b05-116">**GetFilePathFromKey**</span><span class="sxs-lookup"><span data-stu-id="b0b05-116">**GetFilePathFromKey**</span></span>](idwritelocalfontfileloader-getfilepathfromkey.md)             | <span data-ttu-id="b0b05-117">Obtient le chemin d’accès absolu au fichier de polices à partir de la clé de référence du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="b0b05-117">Obtains the absolute font file path from the font file reference key.</span></span><br/>          |
| [<span data-ttu-id="b0b05-118">**GetFilePathLengthFromKey**</span><span class="sxs-lookup"><span data-stu-id="b0b05-118">**GetFilePathLengthFromKey**</span></span>](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | <span data-ttu-id="b0b05-119">Obtient la longueur du chemin d’accès absolu du fichier à partir de la clé de référence du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="b0b05-119">Obtains the length of the absolute file path from the font file reference key.</span></span><br/> |
| [<span data-ttu-id="b0b05-120">**GetLastWriteTimeFromKey**</span><span class="sxs-lookup"><span data-stu-id="b0b05-120">**GetLastWriteTimeFromKey**</span></span>](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | <span data-ttu-id="b0b05-121">Obtient l’heure de la dernière écriture du fichier à partir de la clé de référence du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="b0b05-121">Obtains the last write time of the file from the font file reference key.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="b0b05-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0b05-122">Requirements</span></span>



| <span data-ttu-id="b0b05-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0b05-123">Requirement</span></span> | <span data-ttu-id="b0b05-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0b05-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b05-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0b05-125">Library</span></span><br/> | <dl> <span data-ttu-id="b0b05-126"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0b05-126"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0b05-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b0b05-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="b0b05-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0b05-128"><dt>Dwrite.dll</dt></span></span> </dl> |



 

