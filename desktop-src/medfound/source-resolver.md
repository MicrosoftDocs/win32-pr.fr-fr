---
description: Résolveur source
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Résolveur source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318729"
---
# <a name="source-resolver"></a><span data-ttu-id="0c59e-103">Résolveur source</span><span class="sxs-lookup"><span data-stu-id="0c59e-103">Source Resolver</span></span>

<span data-ttu-id="0c59e-104">Le résolveur de la source crée la source multimédia appropriée pour un contenu donné à partir d'une URL ou d'un flux d'octets.</span><span class="sxs-lookup"><span data-stu-id="0c59e-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="0c59e-105">Pour créer des sources multimédias dans des applications, la méthode la plus courante est de recourir à un résolveur de source.</span><span class="sxs-lookup"><span data-stu-id="0c59e-105">The source resolver is the standard way for the applications to create media sources.</span></span>

<span data-ttu-id="0c59e-106">En interne, le programme de résolution source utilise des objets *gestionnaires* :</span><span class="sxs-lookup"><span data-stu-id="0c59e-106">Internally, the source resolver uses *handler* objects:</span></span>

-   <span data-ttu-id="0c59e-107">Les *gestionnaires de schéma* prennent une URL et créent une source multimédia ou un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="0c59e-107">*Scheme handlers* take a URL and create a media source or a byte stream.</span></span>
-   <span data-ttu-id="0c59e-108">Les *gestionnaires de flux d’octets* prennent un flux d’octets et créent une source de média.</span><span class="sxs-lookup"><span data-stu-id="0c59e-108">*Byte stream handlers* take a byte stream and create a media source.</span></span>

<span data-ttu-id="0c59e-109">Vous pouvez implémenter un gestionnaire personnalisé et l’ajouter au registre.</span><span class="sxs-lookup"><span data-stu-id="0c59e-109">You can implement a custom handler and add it to the registry.</span></span> <span data-ttu-id="0c59e-110">Les gestionnaires de modèles sont inscrits par le schéma d’URL, et les gestionnaires de flux d’octets sont inscrits par l’extension de nom de fichier ou le type MIME.</span><span class="sxs-lookup"><span data-stu-id="0c59e-110">Scheme handlers are registered by URL scheme, and byte stream handlers are registered by file name extension or MIME type.</span></span>

<span data-ttu-id="0c59e-111">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c59e-111">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="0c59e-112">Utilisation du programme de résolution source</span><span class="sxs-lookup"><span data-stu-id="0c59e-112">Using the Source Resolver</span></span>](using-the-source-resolver.md)
-   [<span data-ttu-id="0c59e-113">Configuration d’une source de média</span><span class="sxs-lookup"><span data-stu-id="0c59e-113">Configuring a Media Source</span></span>](configuring-a-media-source.md)
-   [<span data-ttu-id="0c59e-114">Gestionnaires de schémas et gestionnaires de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="0c59e-114">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="0c59e-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c59e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c59e-116">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="0c59e-116">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



