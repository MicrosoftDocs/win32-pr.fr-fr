---
description: Rappel pour retourner les informations du fichier source à partir d’une pile des appels.
MS-HAID: vspixengine.ISourceFileInfoCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ISourceFileInfoCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0430DFF0-F3EA-4645-9B91-E849C0F99609
api_name:
- ISourceFileInfoCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c627d07bfbf455a9c62a922f62adcab945d5741
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747581"
---
# <a name="span-idvspixengineisourcefileinfocallbackspanisourcefileinfocallback-interface"></a><span data-ttu-id="c5bfd-103"><span id="vspixengine.isourcefileinfocallback"></span>Interface ISourceFileInfoCallback</span><span class="sxs-lookup"><span data-stu-id="c5bfd-103"><span id="vspixengine.isourcefileinfocallback"></span>ISourceFileInfoCallback interface</span></span>

<span data-ttu-id="c5bfd-104">Rappel pour retourner les informations du fichier source à partir d’une pile des appels.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-104">Callback to return source file info from a callstack.</span></span>

## <a name="members"></a><span data-ttu-id="c5bfd-105">Membres</span><span class="sxs-lookup"><span data-stu-id="c5bfd-105">Members</span></span>

<span data-ttu-id="c5bfd-106">L’interface **ISourceFileInfoCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c5bfd-106">The **ISourceFileInfoCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c5bfd-107">**ISourceFileInfoCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c5bfd-107">**ISourceFileInfoCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="c5bfd-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c5bfd-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c5bfd-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="c5bfd-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c5bfd-110">L’interface **ISourceFileInfoCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-110">The **ISourceFileInfoCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c5bfd-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="c5bfd-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c5bfd-112">Description</span><span class="sxs-lookup"><span data-stu-id="c5bfd-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c5bfd-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5bfd-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c5bfd-114">Fonction de rappel utilisée pour informer l’hôte d’informations sur les fichiers sources associés à la pile des appels.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-114">A callback function used to notify the host of information about source files associated with the callstack.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c5bfd-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5bfd-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c5bfd-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5bfd-116">Header</span></span></p></td><td><span data-ttu-id="c5bfd-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c5bfd-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
