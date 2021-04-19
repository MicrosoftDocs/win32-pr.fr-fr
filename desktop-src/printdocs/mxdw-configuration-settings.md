---
description: Microsoft XPS document Writer (MXDW) permet aux utilisateurs de créer des fichiers de document XPS en imprimant à partir de n’importe quelle application Windows.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Paramètres de configuration de MXDW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106543553"
---
# <a name="mxdw-configuration-settings"></a><span data-ttu-id="87d45-103">Paramètres de configuration de MXDW</span><span class="sxs-lookup"><span data-stu-id="87d45-103">MXDW Configuration Settings</span></span>

<span data-ttu-id="87d45-104">Microsoft XPS document Writer (MXDW) permet aux utilisateurs de créer des fichiers de document XPS en imprimant à partir de n’importe quelle application Windows.</span><span class="sxs-lookup"><span data-stu-id="87d45-104">The Microsoft XPS Document Writer (MXDW) enables users to create XPS document files by printing from any Windows application.</span></span> <span data-ttu-id="87d45-105">Les développeurs d’applications peuvent contrôler les paramètres de sortie suivants du MXDW à l’aide des parties PrintTicket et PrintCapabilities du [schéma d’impression](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="87d45-105">Applications developers can control the following output settings of the MXDW using the PrintTicket and PrintCapabilities parts of the [Print Schema](./printschema.md).</span></span>

## <a name="jobinterleaving"></a><span data-ttu-id="87d45-106">JobInterleaving</span><span class="sxs-lookup"><span data-stu-id="87d45-106">JobInterleaving</span></span>

<span data-ttu-id="87d45-107">Le paramètre JobInterleaving contrôle l’ordre d’entrelacement du contenu pour les documents XPS.</span><span class="sxs-lookup"><span data-stu-id="87d45-107">The JobInterleaving setting controls the content interleaving order for the XPS Documents.</span></span> <span data-ttu-id="87d45-108">Pour plus d’informations sur l’entrelacement de travaux, consultez la [spécification Paper XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="87d45-108">For information about job interleaving, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span> <span data-ttu-id="87d45-109">MXDW prend en charge les deux options suivantes pour ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="87d45-109">MXDW supports the following two options for this setting:</span></span>

-   <span data-ttu-id="87d45-110">**Off** : cette option désactive l’entrelacement afin que toutes les données de chaque élément de contenu dans le document soient contiguës, ce qui améliore l’efficacité de l’accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="87d45-110">**Off** - This option disables interleaving so that all data for each content element in the document is contiguous, which improves the efficiency of random access.</span></span> <span data-ttu-id="87d45-111">Cette option est idéale pour l’affichage d’un document XPS.</span><span class="sxs-lookup"><span data-stu-id="87d45-111">This option is best for viewing an XPS document.</span></span>
-   <span data-ttu-id="87d45-112">**On** : cette option permet l’entrelacement afin que les données de chaque élément de contenu soient réparties et réorganisées pour un traitement séquentiel plus efficace.</span><span class="sxs-lookup"><span data-stu-id="87d45-112">**On** - This option enables interleaving so that data for each content element is broken up and reordered for more efficient sequential processing.</span></span> <span data-ttu-id="87d45-113">Cette option est idéale pour le téléchargement et l’impression sur le Web.</span><span class="sxs-lookup"><span data-stu-id="87d45-113">This option is best for web download and printing.</span></span>

<span data-ttu-id="87d45-114">L’exemple suivant est un exemple du code XML PrintCapabilities qui comprend le paramètre JobInterleaving.</span><span class="sxs-lookup"><span data-stu-id="87d45-114">The following example is an example of the PrintCapabilities XML that includes the JobInterleaving setting.</span></span>


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="87d45-115">Le code XML PrintTicket est similaire, à ceci près qu’il spécifie une option particulière.</span><span class="sxs-lookup"><span data-stu-id="87d45-115">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="87d45-116">Pour plus d’informations, consultez le [schéma d’impression](./printschema.md) .</span><span class="sxs-lookup"><span data-stu-id="87d45-116">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="87d45-117">Étant donné que JobInterleaving n’est pas l’un des [Mots clés publics du schéma d’impression](./print-schema-public-keywords.md), vous devez inclure une déclaration de l’espace de noms (dans le cas présent « ns0000 » dans la balise **PrintCapabilities** (ou **PrintTicket**) au début du document PrintCapabilities (ou PrintTicket), comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="87d45-117">Since JobInterleaving is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a><span data-ttu-id="87d45-118">JobImageType</span><span class="sxs-lookup"><span data-stu-id="87d45-118">JobImageType</span></span>

<span data-ttu-id="87d45-119">JobImageType contrôle le format de sortie des formats bitmap incorporés.</span><span class="sxs-lookup"><span data-stu-id="87d45-119">JobImageType controls the output format of embedded bitmap formats.</span></span> <span data-ttu-id="87d45-120">MXDW prend en charge les quatre options suivantes pour ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="87d45-120">MXDW supports the following four options for this setting:</span></span>

-   <span data-ttu-id="87d45-121">**JPEGHigh** : cette option spécifie l’image JPEG avec un haut niveau de compression.</span><span class="sxs-lookup"><span data-stu-id="87d45-121">**JPEGHigh** - This option specifies the JPEG image with a high level of compression.</span></span> <span data-ttu-id="87d45-122">Cette option produit la plus petite taille de fichier, mais la qualité d’image la plus faible.</span><span class="sxs-lookup"><span data-stu-id="87d45-122">This option produces the smallest file size, but the lowest image quality.</span></span>
-   <span data-ttu-id="87d45-123">**JPEGMed** : cette option spécifie l’image JPEG avec un niveau de compression moyen.</span><span class="sxs-lookup"><span data-stu-id="87d45-123">**JPEGMed** - This option specifies the JPEG image with a medium level of compression.</span></span> <span data-ttu-id="87d45-124">Cette option fournit le meilleur équilibre entre la taille de fichier et la qualité d’image.</span><span class="sxs-lookup"><span data-stu-id="87d45-124">This option provides the best balance of file size and image quality.</span></span>
-   <span data-ttu-id="87d45-125">**JPEGLow** : cette option spécifie l’image JPEG avec un niveau de compression faible.</span><span class="sxs-lookup"><span data-stu-id="87d45-125">**JPEGLow** - This option specifies the JPEG image with a low level of compression.</span></span> <span data-ttu-id="87d45-126">Cette option produit le moins de réduction de la taille des fichiers et de la qualité d’image élevée.</span><span class="sxs-lookup"><span data-stu-id="87d45-126">This option produces the least reduction in file size and high image quality.</span></span>
-   <span data-ttu-id="87d45-127">**Png** : cette option spécifie le format d’image png avec compression sans perte.</span><span class="sxs-lookup"><span data-stu-id="87d45-127">**PNG** - This option specifies the PNG image format with lossless compression.</span></span> <span data-ttu-id="87d45-128">Cette option produit la taille de fichier la plus grande et la qualité d’image la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="87d45-128">This option produces the largest file size and the highest image quality.</span></span>

<span data-ttu-id="87d45-129">Le code XML PrintCapabilities du paramètre JobImageType apparaît ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="87d45-129">The PrintCapabilities XML of the JobImageType setting appears below:</span></span>


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="87d45-130">Le code XML PrintTicket est similaire, à ceci près qu’il spécifie une option particulière.</span><span class="sxs-lookup"><span data-stu-id="87d45-130">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="87d45-131">Pour plus d’informations, consultez le [schéma d’impression](./printschema.md) .</span><span class="sxs-lookup"><span data-stu-id="87d45-131">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="87d45-132">Étant donné que JobImageType n’est pas l’un des [Mots clés publics du schéma d’impression](./print-schema-public-keywords.md), vous devez inclure une déclaration de l’espace de noms (dans le cas présent « ns0000 » dans la balise **PrintCapabilities** (ou **PrintTicket**) au début du document PrintCapabilities (ou PrintTicket), comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="87d45-132">Since JobImageType is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a><span data-ttu-id="87d45-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87d45-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87d45-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="87d45-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="87d45-135">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="87d45-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="87d45-136">Schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="87d45-136">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="87d45-137">Spécifications XPS et téléchargements de licences</span><span class="sxs-lookup"><span data-stu-id="87d45-137">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
