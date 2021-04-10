---
title: Élément Curve VML
description: Élément Curve VML
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b9e04086652bf9dde7d7e7f5ebdea0992f774c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199277"
---
# <a name="vml-curve-element"></a><span data-ttu-id="659ab-103">Élément Curve VML</span><span class="sxs-lookup"><span data-stu-id="659ab-103">VML Curve Element</span></span>

<span data-ttu-id="659ab-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="659ab-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="659ab-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="659ab-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="659ab-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="659ab-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="659ab-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="659ab-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="659ab-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="659ab-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="659ab-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="659ab-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="659ab-110">Forme de courbe prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="659ab-110">Predefined curve shape.</span></span>

<span data-ttu-id="659ab-111">La **courbe** utilise les attributs [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [Control1](msdn-online-vml-control1-attribute.md)et [Control2](msdn-online-vml-control2-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="659ab-111">**Curve** uses the [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [control1](msdn-online-vml-control1-attribute.md), and [control2](msdn-online-vml-control2-attribute.md) attributes.</span></span>

<span data-ttu-id="659ab-112">Voici le code minimal nécessaire pour générer une image.</span><span class="sxs-lookup"><span data-stu-id="659ab-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 