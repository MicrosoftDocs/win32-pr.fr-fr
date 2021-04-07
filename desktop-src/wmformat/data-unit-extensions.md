---
title: Extensions d’unité de données
description: Extensions d’unité de données
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media Format SDK, Data Unit extensions
- ASF (Advanced Systems Format), extensions d’unité de données
- ASF (format de systèmes avancés), extensions d’unité de données
- SDK Windows Media format, systèmes d’extension de charge utile
- ASF (Advanced Systems Format), systèmes d’extension de charge utile
- ASF (format de systèmes avancés), systèmes d’extension de charge utile
- extensions d’unité de données, à propos de
- extensions d’unité de charge utile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723498"
---
# <a name="data-unit-extensions"></a><span data-ttu-id="56fe7-111">Extensions d’unité de données</span><span class="sxs-lookup"><span data-stu-id="56fe7-111">Data Unit Extensions</span></span>

<span data-ttu-id="56fe7-112">Le kit de développement logiciel (SDK) Windows Media format vous permet de compléter des données dans des exemples avec des *extensions d’unité de données*, également appelées systèmes d’extension de charge utile.</span><span class="sxs-lookup"><span data-stu-id="56fe7-112">The Windows Media Format SDK enables you to supplement data in samples with *data unit extensions*, also called payload extension systems.</span></span> <span data-ttu-id="56fe7-113">Cette documentation utilise le terme « extensions d’unité de données » afin de rester cohérent avec les noms de méthode tels que [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="56fe7-113">This documentation uses the term "data unit extensions" in order to remain consistent with method names such as [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span> <span data-ttu-id="56fe7-114">Une extension d’unité de données est une paire nom/valeur attachée à l’exemple dans la section de données du fichier.</span><span class="sxs-lookup"><span data-stu-id="56fe7-114">A data unit extension is a name/value pair that is attached to the sample in the data section of the file.</span></span> <span data-ttu-id="56fe7-115">Vous pouvez accéder aux données étendues à l’aide des méthodes de l’objet buffer lorsque l’exemple est récupéré par le lecteur.</span><span class="sxs-lookup"><span data-stu-id="56fe7-115">You can access the extended data using methods of the buffer object when the sample is retrieved by the reader.</span></span>

<span data-ttu-id="56fe7-116">Vous pouvez créer des extensions d’unité de données dans vos propres spécifications, mais plusieurs types sont prédéfinis et pris en charge par les objets de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="56fe7-116">You can create data unit extensions to your own specifications, but several types are predefined and supported by the objects of this SDK.</span></span> <span data-ttu-id="56fe7-117">Ces extensions standard sont utilisées pour fournir des données supplémentaires pour les noms de fichiers (dans les flux de script et Web), les données de code temporel SMPTE, les proportions de pixels non carrés, la durée et le type d’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="56fe7-117">These standard extensions are used to provide additional data for file names (in script and Web streams), SMPTE time code data, non-square pixel aspect ratio, duration, and type of interlacing.</span></span>

<span data-ttu-id="56fe7-118">Pour utiliser les extensions d’unité de données, vous devez configurer le flux pour les accepter, puis ajouter des extensions à chaque exemple pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="56fe7-118">To use data unit extensions, you must configure the stream to accept them, and then add extensions to each sample for that stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56fe7-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56fe7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56fe7-120">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="56fe7-120">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="56fe7-121">**Configuration d’extensions d’unité de données**</span><span class="sxs-lookup"><span data-stu-id="56fe7-121">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="56fe7-122">**Définition des extensions d’unité de données**</span><span class="sxs-lookup"><span data-stu-id="56fe7-122">**Setting Data Unit Extensions**</span></span>](setting-data-unit-extensions.md)
</dt> </dl>

 

 




