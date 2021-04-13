---
title: Indicateurs de création de stockage
description: Les indicateurs de création de stockage spécifient ce que COM doit faire si un objet de stockage, de flux ou de LockBytes existant a le même nom qu’un nouvel objet de stockage ou de flux que vous créez.
ms.assetid: 5e079716-9f68-4f1d-9c76-9199e32d78ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0532e8dd817a7f442c26490cbdd37bf3cb34d0ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309310"
---
# <a name="storage-creation-flags"></a><span data-ttu-id="c6aee-103">Indicateurs de création de stockage</span><span class="sxs-lookup"><span data-stu-id="c6aee-103">Storage Creation Flags</span></span>

<span data-ttu-id="c6aee-104">Les indicateurs de création de stockage spécifient ce que COM doit faire si un objet de stockage, de flux ou de LockBytes existant a le même nom qu’un nouvel objet de stockage ou de flux que vous créez.</span><span class="sxs-lookup"><span data-stu-id="c6aee-104">Storage creation flags specify what COM should do if an existing storage, stream, or lockbytes object has the same name as a new storage or stream object that you are creating.</span></span> <span data-ttu-id="c6aee-105">La valeur par défaut consiste à retourner un message d’erreur et à ne pas créer le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="c6aee-105">The default is to return an error message and not create the new object.</span></span> <span data-ttu-id="c6aee-106">Vous ne pouvez utiliser qu’un seul de ces indicateurs dans un appel de création donné.</span><span class="sxs-lookup"><span data-stu-id="c6aee-106">You can use only one of these flags in a given creation call.</span></span>

 

 




