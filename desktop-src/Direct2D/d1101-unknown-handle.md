---
title: Handle D1101 inconnu
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: Une interface non allouée par cette DLL lui a été passée.
keywords:
- D1101 descripteur Direct2D inconnu
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "106541803"
---
# <a name="d1101-unknown-handle"></a><span data-ttu-id="5244c-104">D1101 : handle inconnu</span><span class="sxs-lookup"><span data-stu-id="5244c-104">D1101: Unknown Handle</span></span>

<span data-ttu-id="5244c-105">Une interface d’interface \[  \] non allouée par cette dll lui a été passée.</span><span class="sxs-lookup"><span data-stu-id="5244c-105">An interface \[*interface*\] not allocated by this DLL was passed to it.</span></span>

## <a name="placeholders"></a><span data-ttu-id="5244c-106">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="5244c-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="5244c-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="5244c-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="5244c-108">Adresse de l’interface.</span><span class="sxs-lookup"><span data-stu-id="5244c-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="5244c-109">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="5244c-109">Possible Causes</span></span>

<span data-ttu-id="5244c-110">Utilisation des ressources non valide.</span><span class="sxs-lookup"><span data-stu-id="5244c-110">Invalid resource usage.</span></span> <span data-ttu-id="5244c-111">La ressource créée en dehors de Direct2D est utilisée avec une fabrique Direct2D, ou les ressources créées sur une fabrique ont été utilisées avec une ressource créée par une autre fabrique.</span><span class="sxs-lookup"><span data-stu-id="5244c-111">The resource created outside of Direct2D is used with a Direct2D factory, or the resources created on one factory was used with a resource created by another factory.</span></span>

 

 




