---
title: Conversion en JScript à partir de JavaScript
description: Conversion en JScript à partir de JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104507818"
---
# <a name="translating-to-jscript-from-javascript"></a><span data-ttu-id="32c2e-103">Conversion en JScript à partir de JavaScript</span><span class="sxs-lookup"><span data-stu-id="32c2e-103">Translating to JScript from JavaScript</span></span>

<span data-ttu-id="32c2e-104">JScript est en grande partie compatible avec JavaScript.</span><span class="sxs-lookup"><span data-stu-id="32c2e-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="32c2e-105">Toutefois, JScript version 5,0 comprend certains objets qui ne sont actuellement pas pris en charge par JavaScript, tels que ActiveXObject, Enumerator, Error, global et VBArray.</span><span class="sxs-lookup"><span data-stu-id="32c2e-105">However, JScript version 5.0 includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="32c2e-106">JScript 5,0 prend en charge la gestion des exceptions via **try**... instructions **catch** .</span><span class="sxs-lookup"><span data-stu-id="32c2e-106">JScript 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="32c2e-107">JavaScript ne fournit pas actuellement de mécanisme de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="32c2e-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="32c2e-108">Lors de l’utilisation de JScript ou JavaScript, il existe quelques différences subtiles entre les implémentations de modèle objet prises en charge par différents navigateurs Web.</span><span class="sxs-lookup"><span data-stu-id="32c2e-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="32c2e-109">Pour écrire un script qui s’exécute à la fois sur Internet Explorer et Netscape Navigator, limitez les fonctionnalités utilisées par vos scripts à celles spécifiées dans la norme World Wide Web Consortium (W3C) pour HTML version 3,2.</span><span class="sxs-lookup"><span data-stu-id="32c2e-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) standard for HTML version 3.2.</span></span> <span data-ttu-id="32c2e-110">Pour plus d’informations sur cette norme, consultez [spécification de référence HTML 3,2](https://www.w3.org/TR/REC-html32.html).</span><span class="sxs-lookup"><span data-stu-id="32c2e-110">For more information about this standard, see [HTML 3.2 Reference Specification](https://www.w3.org/TR/REC-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="32c2e-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32c2e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32c2e-112">Traduire en JScript</span><span class="sxs-lookup"><span data-stu-id="32c2e-112">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




