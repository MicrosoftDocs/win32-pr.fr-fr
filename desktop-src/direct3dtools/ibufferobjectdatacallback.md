---
description: Rappel pour retourner le contenu d’un objet sous forme de mémoire tampon pour ceux qui le prennent en charge (mémoires tampons, textures).
MS-HAID: vspixengine.IBufferObjectDataCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IBufferObjectDataCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAE4CE9A-B8EB-4ED6-9F48-D00C19B27A2E
api_name:
- IBufferObjectDataCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e5fb7deebd7d1b16d333ae59edab9372b54ad8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108946"
---
# <a name="span-idvspixengineibufferobjectdatacallbackspanibufferobjectdatacallback-interface"></a><span data-ttu-id="02f73-103"><span id="vspixengine.ibufferobjectdatacallback"></span>Interface IBufferObjectDataCallback</span><span class="sxs-lookup"><span data-stu-id="02f73-103"><span id="vspixengine.ibufferobjectdatacallback"></span>IBufferObjectDataCallback interface</span></span>

<span data-ttu-id="02f73-104">Rappel pour retourner le contenu d’un objet sous forme de mémoire tampon pour ceux qui le prennent en charge (mémoires tampons, textures).</span><span class="sxs-lookup"><span data-stu-id="02f73-104">Callback to return the contents of an object in buffer form for those that support it (buffers, textures).</span></span>

## <a name="members"></a><span data-ttu-id="02f73-105">Membres</span><span class="sxs-lookup"><span data-stu-id="02f73-105">Members</span></span>

<span data-ttu-id="02f73-106">L’interface **IBufferObjectDataCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="02f73-106">The **IBufferObjectDataCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="02f73-107">**IBufferObjectDataCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="02f73-107">**IBufferObjectDataCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="02f73-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="02f73-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="02f73-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="02f73-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="02f73-110">L’interface **IBufferObjectDataCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="02f73-110">The **IBufferObjectDataCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="02f73-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="02f73-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="02f73-112">Description</span><span class="sxs-lookup"><span data-stu-id="02f73-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="02f73-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="02f73-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="02f73-114">Rappel qui avertit l’hôte d’informations de mémoire tampon écrites dans un fichier par la demande dans.</span><span class="sxs-lookup"><span data-stu-id="02f73-114">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="02f73-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02f73-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="02f73-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="02f73-116">Header</span></span></p></td><td><span data-ttu-id="02f73-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="02f73-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
