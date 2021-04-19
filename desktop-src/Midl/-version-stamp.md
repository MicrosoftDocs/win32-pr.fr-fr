---
title: commutateur/version_stamp
description: Le \_ commutateur d’horodatage/version supprime la génération de macros qui spécifient le numéro de version minimal requis du fichier d’en-tête RPC, Rpcndr. h.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /commutateur version_stamp MIDL
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511054"
---
# <a name="version_stamp-switch"></a><span data-ttu-id="082ba-104">\_commutateur de tampon/version</span><span class="sxs-lookup"><span data-stu-id="082ba-104">/version\_stamp switch</span></span>

<span data-ttu-id="082ba-105">Le commutateur d' **\_ horodatage/version** supprime la génération de macros qui spécifient le numéro de version minimal requis du fichier d’en-tête RPC, Rpcndr. h.</span><span class="sxs-lookup"><span data-stu-id="082ba-105">The **/version\_stamp** switch suppresses the generation of macros that specify the minimum required version number of the RPC header file, Rpcndr.h.</span></span>

<span data-ttu-id="082ba-106">Les nouvelles fonctionnalités MIDL peuvent nécessiter des définitions supplémentaires pour compiler correctement le stub, de sorte que le stub possède des macros qui vérifient la compatibilité entre les fichiers binaires MIDL et l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="082ba-106">New MIDL features might require additional definitions to compile the stub correctly, so the stub has macros that check compatibility between MIDL binary files and the build environment.</span></span> <span data-ttu-id="082ba-107">Vous devrez peut-être utiliser ce commutateur si vous déplacez MIDL vers un environnement de génération différent de celui dans lequel vous avez installé les fichiers binaires MIDL pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="082ba-107">You might need to use this switch if you move MIDL to a different build environment than the one in which you first installed the MIDL binary files.</span></span>

<span data-ttu-id="082ba-108">Notez que le mélange d’environnements de génération n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="082ba-108">Note that mixing build environments is not supported.</span></span>

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a><span data-ttu-id="082ba-109">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="082ba-109">Switch Options</span></span>

<span data-ttu-id="082ba-110">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="082ba-110">This switch has no parameters.</span></span>

 

 




