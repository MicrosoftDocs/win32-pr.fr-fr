---
title: Attribut SRC (VMLFrame) (VML)
description: Attribut SRC (VMLFrame) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315492"
---
# <a name="src-attribute-vmlframevml"></a><span data-ttu-id="5d1ab-103">Attribut SRC (VMLFrame) (VML)</span><span class="sxs-lookup"><span data-stu-id="5d1ab-103">Src Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="5d1ab-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5d1ab-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5d1ab-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5d1ab-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5d1ab-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5d1ab-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5d1ab-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5d1ab-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5d1ab-110">Définit la source de données pour le frame.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-110">Defines the source of data for the frame.</span></span> <span data-ttu-id="5d1ab-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-111">Read/write.</span></span> <span data-ttu-id="5d1ab-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-112">**String**.</span></span>

<span data-ttu-id="5d1ab-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5d1ab-113">**Applies To**</span></span>

[<span data-ttu-id="5d1ab-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="5d1ab-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="5d1ab-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="5d1ab-115">**Tag Syntax**</span></span>

<span data-ttu-id="5d1ab-116"><v : *Element* SRC = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5d1ab-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="5d1ab-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="5d1ab-117">**Script Syntax**</span></span>

<span data-ttu-id="5d1ab-118">*Element* . src = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="5d1ab-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="5d1ab-119">*expression* = *élément*. SRC</span><span class="sxs-lookup"><span data-stu-id="5d1ab-119">*expression*=*element*.src</span></span>

<span data-ttu-id="5d1ab-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="5d1ab-120">**Remarks**</span></span>

<span data-ttu-id="5d1ab-121">L’attribut **src** peut impliquer les syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d1ab-121">The **Src** attribute can involve the following syntaxes:</span></span>

-   <span data-ttu-id="5d1ab-122">URL vers un fichier externe.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-122">URL to external file.</span></span> <span data-ttu-id="5d1ab-123">Le fichier doit être un fichier XML au format suivant :</span><span class="sxs-lookup"><span data-stu-id="5d1ab-123">The file must be an XML file with the following format:</span></span>
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   <span data-ttu-id="5d1ab-124">Dans le fichier, vous devez avoir une ou plusieurs formes VML avec des ID valides qui peuvent être référencées à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="5d1ab-124">Inside the file you must have one or more VML shapes with valid IDs that can be referenced by using this syntax:</span></span>
    ```HTML
       filename#shapename
    ```

    

-   <span data-ttu-id="5d1ab-125">Dans la référence suivante, les fichiers externes ont l’extension. Vml, mais vous pouvez utiliser n’importe quelle extension :</span><span class="sxs-lookup"><span data-stu-id="5d1ab-125">In the following reference, external files have the .vml extension, but any extension can be used:</span></span>
    ```HTML
       external.vml#image01
    ```

    

-   <span data-ttu-id="5d1ab-126">Vous pouvez référencer une forme dans le même fichier à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="5d1ab-126">You can reference a shape within the same file by using the following syntax:</span></span>
    ```HTML
       #shapename
    ```

    

<span data-ttu-id="5d1ab-127">Si **clip** a la **valeur false**, la forme est mise à l’échelle pour s’ajuster au cadre.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-127">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="5d1ab-128">Si la **valeur est true**, toutes les parties de la forme qui sont en dehors du frame ne seront pas affichées.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-128">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="5d1ab-129">Notez que [origin](origin-attribute--vmlframe--vml.md) et [Size](size-attribute--vmlframe.md) ne sont pas utilisés, sauf si **clip** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-129">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="5d1ab-130">**Attribut standard VML**</span><span class="sxs-lookup"><span data-stu-id="5d1ab-130">**VML Standard Attribute**</span></span>

<span data-ttu-id="5d1ab-131">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="5d1ab-131">**Example**</span></span>

<span data-ttu-id="5d1ab-132">L’image définie dans le fichier externe sera découpée.</span><span class="sxs-lookup"><span data-stu-id="5d1ab-132">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 