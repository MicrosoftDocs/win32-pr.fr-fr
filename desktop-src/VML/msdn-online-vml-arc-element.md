---
title: Élément d’arc VML
description: Élément d’arc VML
ms.assetid: 46b5b78a-9a69-432b-9008-0ce7a658b9dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd35d59349e10f38495807ceb3f08dc254c117e2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316296"
---
# <a name="vml-arc-element"></a><span data-ttu-id="42e21-103">Élément d’arc VML</span><span class="sxs-lookup"><span data-stu-id="42e21-103">VML Arc Element</span></span>

<span data-ttu-id="42e21-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="42e21-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="42e21-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="42e21-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="42e21-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="42e21-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="42e21-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="42e21-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="42e21-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="42e21-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="42e21-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="42e21-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="42e21-110">Forme d’arc prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="42e21-110">Predefined arc shape.</span></span>

<span data-ttu-id="42e21-111">L' **arc** utilise les attributs [startAngle](msdn-online-vml-startangle-attribute.md) et [endAngle](msdn-online-vml-endangle-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="42e21-111">**Arc** uses the [startangle](msdn-online-vml-startangle-attribute.md) and [endangle](msdn-online-vml-endangle-attribute.md) attributes.</span></span>

<span data-ttu-id="42e21-112">Voici le code minimal nécessaire pour générer une image.</span><span class="sxs-lookup"><span data-stu-id="42e21-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:arc
   style="top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```





 

 