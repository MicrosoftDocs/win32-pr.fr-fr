---
title: Métadonnées personnalisées
description: Métadonnées personnalisées
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- Windows Media Format SDK, métadonnées personnalisées
- ASF (Advanced Systems Format), métadonnées personnalisées
- ASF (format de systèmes avancés), métadonnées personnalisées
- Windows Media Format SDK, interface IWMHeaderInfo3
- ASF (Advanced Systems Format), interface IWMHeaderInfo3
- ASF (format des systèmes avancés), interface IWMHeaderInfo3
- métadonnées, personnalisation
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a795ab184e5bd6120278f61c0d3654679fd79c28
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724026"
---
# <a name="custom-metadata"></a><span data-ttu-id="a8c8f-111">Métadonnées personnalisées</span><span class="sxs-lookup"><span data-stu-id="a8c8f-111">Custom Metadata</span></span>

<span data-ttu-id="a8c8f-112">Outre les nombreux attributs pris en charge fournis avec le kit de développement logiciel (SDK) Windows Media format, vous pouvez créer des attributs de métadonnées pour vos propres spécifications.</span><span class="sxs-lookup"><span data-stu-id="a8c8f-112">In addition to the many supported attributes provided with the Windows Media Format SDK, you can create metadata attributes to your own specifications.</span></span> <span data-ttu-id="a8c8f-113">Lorsque vous créez des attributs de métadonnées personnalisés, vous devez utiliser une convention d’affectation de noms facilement identifiable pour éviter tout conflit possible avec les attributs créés par d’autres.</span><span class="sxs-lookup"><span data-stu-id="a8c8f-113">When creating custom metadata attributes, you should use an easily identifiable naming convention to avoid possible conflict with attributes created by others.</span></span>

<span data-ttu-id="a8c8f-114">Il est recommandé d’utiliser les méthodes de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) pour créer vos métadonnées en raison de la flexibilité ajoutée qu’elles offrent sur les méthodes de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="a8c8f-114">It is recommended that you use the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) to create your metadata because of the added flexibility they provide over the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8c8f-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8c8f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8c8f-116">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="a8c8f-116">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="a8c8f-117">**Fonctionnalités de métadonnées**</span><span class="sxs-lookup"><span data-stu-id="a8c8f-117">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="a8c8f-118">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="a8c8f-118">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




