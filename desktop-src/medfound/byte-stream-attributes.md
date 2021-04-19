---
description: Attributs de flux d’octets
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Attributs de flux d’octets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515805"
---
# <a name="byte-stream-attributes"></a><span data-ttu-id="03426-103">Attributs de flux d’octets</span><span class="sxs-lookup"><span data-stu-id="03426-103">Byte Stream Attributes</span></span>

<span data-ttu-id="03426-104">Les attributs suivants s’appliquent à certains flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="03426-104">The following attributes apply to some byte streams.</span></span> <span data-ttu-id="03426-105">Pour déterminer si un flux d’octets prend en charge les attributs, interrogez l’objet de flux d’octets pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="03426-105">To find out whether a byte stream supports attributes, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>



| <span data-ttu-id="03426-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="03426-106">Attribute</span></span>                                                                                  | <span data-ttu-id="03426-107">Description</span><span class="sxs-lookup"><span data-stu-id="03426-107">Description</span></span>                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="03426-108">**\_type de \_ contenu \_ BYTESTREAM MF**</span><span class="sxs-lookup"><span data-stu-id="03426-108">**MF\_BYTESTREAM\_CONTENT\_TYPE**</span></span>](mf-bytestream-content-type-attribute.md)              | <span data-ttu-id="03426-109">Spécifie le type MIME d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="03426-109">Specifies the MIME type of a byte stream.</span></span>                         |
| [<span data-ttu-id="03426-110">**\_durée BYTESTREAM \_ MF**</span><span class="sxs-lookup"><span data-stu-id="03426-110">**MF\_BYTESTREAM\_DURATION**</span></span>](mf-bytestream-duration-attribute.md)                       | <span data-ttu-id="03426-111">Spécifie la durée d’un flux d’octets, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="03426-111">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="03426-112">\_URI du \_ \_ fichier IFO BYTESTREAM MF \_</span><span class="sxs-lookup"><span data-stu-id="03426-112">MF\_BYTESTREAM\_IFO\_FILE\_URI</span></span>](mf-bytestream-ifo-file-uri.md)                           | <span data-ttu-id="03426-113">Spécifie l’URL d’un fichier IFO associé.</span><span class="sxs-lookup"><span data-stu-id="03426-113">Specifies the URL of an associated IFO file.</span></span>                      |
| [<span data-ttu-id="03426-114">**\_heure de \_ dernière \_ modification de BYTESTREAM \_ MF**</span><span class="sxs-lookup"><span data-stu-id="03426-114">**MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME**</span></span>](mf-bytestream-last-modified-time-attribute.md) | <span data-ttu-id="03426-115">Spécifie la date de la dernière modification d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="03426-115">Specifies when a byte stream was last modified.</span></span>                   |
| [<span data-ttu-id="03426-116">**\_nom d' \_ origine MF BYTESTREAM \_**</span><span class="sxs-lookup"><span data-stu-id="03426-116">**MF\_BYTESTREAM\_ORIGIN\_NAME**</span></span>](mf-bytestream-origin-name-attribute.md)                | <span data-ttu-id="03426-117">Spécifie l’URL d’origine d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="03426-117">Specifies the original URL for a byte stream.</span></span>                     |



 

<span data-ttu-id="03426-118">Les attributs suivants s’appliquent aux gestionnaires de flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="03426-118">The following attributes apply to byte-stream handlers.</span></span>



| <span data-ttu-id="03426-119">Attribut</span><span class="sxs-lookup"><span data-stu-id="03426-119">Attribute</span></span>                                                                                    | <span data-ttu-id="03426-120">Description</span><span class="sxs-lookup"><span data-stu-id="03426-120">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03426-121">MF \_ BYTESTREAMHANDLER \_ accepte \_ l' \_ écriture de partage</span><span class="sxs-lookup"><span data-stu-id="03426-121">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE</span></span>](mf-bytestreamhandler-accepts-share-write.md) | <span data-ttu-id="03426-122">Spécifie si un gestionnaire de flux d’octets peut utiliser un flux d’octets ouvert pour l’écriture par un autre thread</span><span class="sxs-lookup"><span data-stu-id="03426-122">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="03426-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03426-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03426-124">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="03426-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[<span data-ttu-id="03426-125">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03426-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



