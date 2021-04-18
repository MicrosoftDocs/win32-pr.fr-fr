---
title: Plug-ins sources
description: Plug-ins sources
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Kit de développement logiciel (SDK) Windows Media format, plug-ins source
- ASF (Advanced Systems Format), plug-ins source
- ASF (Advanced Systems Format), plug-ins source
- plug-ins sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106522633"
---
# <a name="source-plug-ins"></a><span data-ttu-id="f077c-107">Plug-ins sources</span><span class="sxs-lookup"><span data-stu-id="f077c-107">Source Plug-ins</span></span>

<span data-ttu-id="f077c-108">Un plug-in source est une option disponible pour les développeurs qui souhaitent implémenter leur propre système de stockage pour les fichiers® Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f077c-108">A source plug-in is an option available to developers who wish to implement their own storage system for Windows Media® files.</span></span> <span data-ttu-id="f077c-109">Un plug-in source le permet via l’implémentation d’une interface COM appelée **IStream**, qui est une interface standard pour fournir des données.</span><span class="sxs-lookup"><span data-stu-id="f077c-109">A source plug-in enables this through the implementation of a COM interface called **IStream**, which is a standard interface for providing data.</span></span>

<span data-ttu-id="f077c-110">Le plug-in source doit être écrit en tant que dll et sa présence est connue du kit de développement logiciel (SDK) par le biais d’une entrée de registre.</span><span class="sxs-lookup"><span data-stu-id="f077c-110">The source plug-in should be written as a dll, and its presence is made known to the SDK through a registry entry.</span></span> <span data-ttu-id="f077c-111">Plusieurs plug-ins sources peuvent être implémentés de cette façon.</span><span class="sxs-lookup"><span data-stu-id="f077c-111">There can be any number of source plug-ins implemented this way.</span></span> <span data-ttu-id="f077c-112">Le plug-in source doit exporter la fonction [**WMCreateStreamForURL**](wmcreatestreamforurl.md) .</span><span class="sxs-lookup"><span data-stu-id="f077c-112">The source plug-in must export the [**WMCreateStreamForURL**](wmcreatestreamforurl.md) function.</span></span>

<span data-ttu-id="f077c-113">Pour inscrire un plug-in source, l’entrée de Registre suivante doit être ajoutée :</span><span class="sxs-lookup"><span data-stu-id="f077c-113">To register a source plug-in, the following registry entry should be added:</span></span>

<span data-ttu-id="f077c-114">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows Media \\ WMSDK \\ sources</span><span class="sxs-lookup"><span data-stu-id="f077c-114">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Media\\WMSDK\\sources</span></span>

<span data-ttu-id="f077c-115">Name = « n’importe quel nom unique »</span><span class="sxs-lookup"><span data-stu-id="f077c-115">Name = "any unique name"</span></span>

<span data-ttu-id="f077c-116">Valeur = chemin d’accès de la dll du plug-in source</span><span class="sxs-lookup"><span data-stu-id="f077c-116">Value = pathname of the source plug-in dll</span></span>

<span data-ttu-id="f077c-117">Une fois la dll inscrite, l’application peut utiliser la méthode **IWMReader :: Open** (avec l’URL appropriée comme paramètre) pour accéder aux données de flux, qui peuvent être stockées dans des fichiers ou des conteneurs de données définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f077c-117">Once the dll has been registered, the application can use the **IWMReader::Open** method (with the appropriate URL as a parameter) to access stream data, which can be stored in files or user-defined data containers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f077c-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f077c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f077c-119">**IWMReader :: Open**</span><span class="sxs-lookup"><span data-stu-id="f077c-119">**IWMReader::Open**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[<span data-ttu-id="f077c-120">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="f077c-120">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="f077c-121">**WMCreateStreamForURL**</span><span class="sxs-lookup"><span data-stu-id="f077c-121">**WMCreateStreamForURL**</span></span>](wmcreatestreamforurl.md)
</dt> </dl>

 

 




