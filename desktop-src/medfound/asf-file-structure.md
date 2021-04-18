---
description: Cette rubrique décrit la structure d’un fichier ASF (Advanced Systems Format).
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Structure de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524671"
---
# <a name="asf-file-structure"></a><span data-ttu-id="ffbd1-103">Structure de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="ffbd1-103">ASF File Structure</span></span>

<span data-ttu-id="ffbd1-104">Cette rubrique décrit la structure d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="ffbd1-104">This topic describes the structure of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="ffbd1-105">Pour plus d’informations sur les fichiers ASF, téléchargez la [spécification ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="ffbd1-105">For detailed information about ASF files, download the [ASF Specification](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span> <span data-ttu-id="ffbd1-106">Vous pouvez également utiliser l’outil [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) pour voir la structure d’un fichier ASF existant.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-106">You can also use the [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) tool to see the structure of an existing ASF file.</span></span>

<span data-ttu-id="ffbd1-107">L’unité de base de l’Organisation pour les fichiers ASF est appelée un *objet*.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-107">The base unit of organization for ASF files is called an *object*.</span></span> <span data-ttu-id="ffbd1-108">Un objet fichier ASF contient les données suivantes.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-108">An ASF file object contains the following data.</span></span>



| <span data-ttu-id="ffbd1-109">Données</span><span class="sxs-lookup"><span data-stu-id="ffbd1-109">Data</span></span>                                                        | <span data-ttu-id="ffbd1-110">Taille</span><span class="sxs-lookup"><span data-stu-id="ffbd1-110">Size</span></span>     |
|-------------------------------------------------------------|----------|
| <span data-ttu-id="ffbd1-111">GUID qui identifie l’objet.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-111">A GUID that identifies the object.</span></span>                          | <span data-ttu-id="ffbd1-112">128 bits</span><span class="sxs-lookup"><span data-stu-id="ffbd1-112">128 bits</span></span> |
| <span data-ttu-id="ffbd1-113">Taille de l'objet.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-113">The size of the object.</span></span>                                     | <span data-ttu-id="ffbd1-114">64-bits.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-114">64-bits.</span></span> |
| <span data-ttu-id="ffbd1-115">Données d’objet.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-115">Object data.</span></span> <span data-ttu-id="ffbd1-116">Les données d’objet peuvent contenir d’autres objets ASF.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-116">The object data can contain other ASF objects.</span></span> | <span data-ttu-id="ffbd1-117">Varie.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-117">Varies.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="ffbd1-118">Un objet fichier ASF est simplement un bloc de données.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-118">An ASF file object is simply a chunk of data.</span></span> <span data-ttu-id="ffbd1-119">Il ne s’agit pas d’un objet dans le sens de la programmation informatique.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-119">It is not an object in the computer programming sense.</span></span>

 

<span data-ttu-id="ffbd1-120">Un fichier ASF contient trois types d’objets de fichier de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-120">An ASF file contains three types of top-level file objects.</span></span>



| <span data-ttu-id="ffbd1-121">Objet fichier ASF</span><span class="sxs-lookup"><span data-stu-id="ffbd1-121">ASF File Object</span></span>                                                                                                                      | <span data-ttu-id="ffbd1-122">Description</span><span class="sxs-lookup"><span data-stu-id="ffbd1-122">Description</span></span>                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ffbd1-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Objet d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ffbd1-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header Object</span></span><br/>         | <span data-ttu-id="ffbd1-124">Contient des informations sur le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-124">Contains information about the ASF file.</span></span><br/>  |
| <span data-ttu-id="ffbd1-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Objet de données</span><span class="sxs-lookup"><span data-stu-id="ffbd1-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Data Object</span></span><br/>                     | <span data-ttu-id="ffbd1-126">Contient des paquets de données multimédias.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-126">Contains packets of media data.</span></span><br/>           |
| <span data-ttu-id="ffbd1-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Objet (s) d’index</span><span class="sxs-lookup"><span data-stu-id="ffbd1-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Index Object(s)</span></span><br/> | <span data-ttu-id="ffbd1-128">Contient un ou plusieurs index.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-128">Contains one or more indexes.</span></span> <span data-ttu-id="ffbd1-129">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="ffbd1-129">(Optional.)</span></span><br/> |



 

<span data-ttu-id="ffbd1-130">Le diagramme suivant illustre la structure de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-130">The following diagram shows the ASF file structure.</span></span>

![Diagramme montrant la structure des fichiers ASF, y compris les éléments contenus dans l’en-tête, les données et l’index](images/asf-components04.png)

<span data-ttu-id="ffbd1-132">Ce diagramme n’est pas dessiné pour être mis à l’échelle ; en général, l’objet de données comprend la plus grande partie du fichier.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-132">This diagram is not drawn to scale; typically the Data Object comprises most of the file.</span></span>

### <a name="header-object"></a><span data-ttu-id="ffbd1-133">Objet d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ffbd1-133">Header Object</span></span>

<span data-ttu-id="ffbd1-134">L’objet d’en-tête est obligatoire et apparaît au début de chaque fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-134">The Header Object is mandatory and appears at the beginning of every ASF file.</span></span> <span data-ttu-id="ffbd1-135">Il contient des attributs de fichier globaux et des informations sur les flux dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-135">It contains global file attributes and information about the streams in the ASF file.</span></span> <span data-ttu-id="ffbd1-136">Ces informations permettent d’interpréter et de lire les données contenues dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-136">This information is used to interpret and play the data in the file.</span></span>

<span data-ttu-id="ffbd1-137">L’objet Header contient plusieurs sous-objets madatory :</span><span class="sxs-lookup"><span data-stu-id="ffbd1-137">The Header Object contains several madatory sub-objects:</span></span>

-   <span data-ttu-id="ffbd1-138">L’objet de propriétés de fichier décrit les attributs globaux du fichier, tels que la taille de fichier, la durée de lecture, le nombre de paquets de données, la taille de paquet minimale et maximale et la vitesse de transmission maximale.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-138">The File Properties Object describes global attributes of the file, such as the file size, play duration, number of data packets, minimum and maximum packet size, and maximum bit rate.</span></span>
-   <span data-ttu-id="ffbd1-139">L’objet d’extension d’en-tête permet d’ajouter des fonctionnalités supplémentaires à un fichier ASF tout en conservant la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-139">The Header Extension Object enables additional functionality to be added to an ASF file while maintaining backward compatibility.</span></span>
-   <span data-ttu-id="ffbd1-140">L’objet de propriétés de flux décrit un flux dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-140">The Stream Properties Object describes one stream in the file.</span></span> <span data-ttu-id="ffbd1-141">Un fichier ASF doit contenir au moins un flux et, par conséquent, au moins un objet de propriétés de flux.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-141">An ASF file must contain at least one stream, and therefore at least one Stream Properties Object.</span></span>

<span data-ttu-id="ffbd1-142">L’objet d’en-tête peut contenir des informations facultatives supplémentaires, y compris des métadonnées sur le fichier (par exemple, titre et auteur), une liste des codecs utilisés pour encoder le fichier et des informations de protection du contenu.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-142">The Header Object can contain additional optional information, including metadata about the file (such as title and author), a list of the codecs used to encode the file, and content protection information.</span></span>

### <a name="data-object"></a><span data-ttu-id="ffbd1-143">Objet de données</span><span class="sxs-lookup"><span data-stu-id="ffbd1-143">Data Object</span></span>

<span data-ttu-id="ffbd1-144">L’objet de données ASF contient toutes les données multimédias du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-144">The ASF Data Object contains all of the media data for the ASF file.</span></span> <span data-ttu-id="ffbd1-145">Cet objet est obligatoire et doit suivre l’objet d’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-145">This object is mandatory and must follow the ASF Header Object.</span></span>

<span data-ttu-id="ffbd1-146">L’objet de données est divisé en *paquets* de données.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-146">The Data Object is divided into data *packets*.</span></span> <span data-ttu-id="ffbd1-147">Chaque paquet contient des données pour un ou plusieurs flux dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-147">Each packet contains data for one or several streams in the file.</span></span> <span data-ttu-id="ffbd1-148">Un paquet de données contient un en-tête de paquet de données qui fournit des informations d’analyse de paquets, suivies des données de charge utile des données de support numérique réelles.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-148">A data packet contains a data packet header that provides packet parsing information, followed by the payload data the actual digital media data.</span></span> <span data-ttu-id="ffbd1-149">L’heure de la présentation est associée à tous les paquets de données et elles sont organisées dans l’ordre de réception.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-149">All of the data packets have a presentation time associated with it and are arranged in the order received.</span></span>

<span data-ttu-id="ffbd1-150">Les informations sur le contenu de l’objet de données, telles que la taille du paquet et le nombre de paquets, sont stockées dans l’objet d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-150">Information about the contents of the Data Object, such as the packet size and packet count, is stored in the Header Object.</span></span>

### <a name="index-object"></a><span data-ttu-id="ffbd1-151">Index (objet)</span><span class="sxs-lookup"><span data-stu-id="ffbd1-151">Index Object</span></span>

<span data-ttu-id="ffbd1-152">L’objet index est facultatif et est le dernier objet du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-152">The Index Object is optional and is the last object in the ASF file.</span></span> <span data-ttu-id="ffbd1-153">Un fichier ASF peut contenir plusieurs objets index.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-153">An ASF file can contain more than one Index Object.</span></span> <span data-ttu-id="ffbd1-154">L’objet index fournit un accès aléatoire basé sur le temps à l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-154">The Index Object provides time-based random access into the ASF Data Object.</span></span>

<span data-ttu-id="ffbd1-155">Un objet index simple est un autre type d’index.</span><span class="sxs-lookup"><span data-stu-id="ffbd1-155">A Simple Index Object is another type of index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffbd1-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffbd1-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffbd1-157">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ffbd1-157">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




