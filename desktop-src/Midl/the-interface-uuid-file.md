---
title: Fichier UUID de l’interface
description: Le fichier UUID de l’interface collecte les définitions des identificateurs d’interface à partir de toutes les interfaces dans le fichier IDL traité.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL et COM MIDL, interfaces, fichiers UUID de proxy
- MIDL du fichier UUID de l’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675170"
---
# <a name="the-interface-uuid-file"></a><span data-ttu-id="3b134-105">Fichier UUID de l’interface</span><span class="sxs-lookup"><span data-stu-id="3b134-105">The Interface UUID File</span></span>

<span data-ttu-id="3b134-106">Le fichier UUID de l’interface collecte les définitions des identificateurs d’interface à partir de toutes les interfaces dans le fichier IDL traité.</span><span class="sxs-lookup"><span data-stu-id="3b134-106">The interface UUID file collects the definitions of the interface identifiers from all interfaces in the processed IDL file.</span></span> <span data-ttu-id="3b134-107">À l’instar du fichier stub et du fichier d’en-tête, la fermeture du flux d’entrée est définie par le fichier IDL actuel et les fichiers inclus.</span><span class="sxs-lookup"><span data-stu-id="3b134-107">Similar to the stub file and the header file, the input stream closure is defined by the current IDL file and the included files.</span></span> <span data-ttu-id="3b134-108">Par exemple, pour l’interface IFace, le compilateur génère une IFace IID constante \_ et l’initialise à l’UUID de l’interface spécifié dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="3b134-108">For example, for Interface IFace, the compiler generates a constant IID\_IFace and initializes it to the interface's UUID specified in the IDL file.</span></span> <span data-ttu-id="3b134-109">Les applications clientes et la DLL de proxy utilisent cette constante pour identifier l’interface.</span><span class="sxs-lookup"><span data-stu-id="3b134-109">Client applications and the proxy DLL use this constant to identify the interface.</span></span>

<span data-ttu-id="3b134-110">Le nom par défaut d’un fichier d’IID d’interface généré à partir d’un fichier. idl est file \_ i.c.</span><span class="sxs-lookup"><span data-stu-id="3b134-110">The default name for an interface IID file generated from a file.idl is File\_i.c.</span></span> <span data-ttu-id="3b134-111">Le commutateur du compilateur [**/IID**](-iid.md) MIDL remplace le nom par défaut du fichier UUID de l’interface.</span><span class="sxs-lookup"><span data-stu-id="3b134-111">The [**/iid**](-iid.md) MIDL compiler switch overrides the default name of the interface UUID file.</span></span>

 

 




