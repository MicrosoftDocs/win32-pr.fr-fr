---
title: Conversion en JavaScript à partir de JScript
description: Conversion en JavaScript à partir de JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381609"
---
# <a name="translating-to-javascript-from-jscript"></a><span data-ttu-id="6855b-103">Conversion en JavaScript à partir de JScript</span><span class="sxs-lookup"><span data-stu-id="6855b-103">Translating to JavaScript from JScript</span></span>

<span data-ttu-id="6855b-104">JScript est en grande partie compatible avec JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6855b-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="6855b-105">Toutefois, JScript comprend certains objets qui ne sont actuellement pas pris en charge par JavaScript, tels que ActiveXObject, Enumerator, Error, global et VBArray.</span><span class="sxs-lookup"><span data-stu-id="6855b-105">However, JScript includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="6855b-106">JScript version 5,0 prend en charge la gestion des exceptions via **try**... instructions **catch** .</span><span class="sxs-lookup"><span data-stu-id="6855b-106">JScript version 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="6855b-107">JavaScript ne fournit pas actuellement de mécanisme de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="6855b-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="6855b-108">Lors de l’utilisation de JScript ou JavaScript, il existe quelques différences subtiles entre les implémentations de modèle objet prises en charge par différents navigateurs Web.</span><span class="sxs-lookup"><span data-stu-id="6855b-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="6855b-109">Pour écrire un script qui s’exécute à la fois sur Internet Explorer et Netscape Navigator, limitez les fonctionnalités utilisées par vos scripts à celles spécifiées dans la norme World Wide Web Consortium (W3C) [pour HTML version 3,2](https://www.w3.org/tr/rec-html32.html).</span><span class="sxs-lookup"><span data-stu-id="6855b-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) [standard for HTML version 3.2](https://www.w3.org/tr/rec-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6855b-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6855b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6855b-111">Conversion en JavaScript</span><span class="sxs-lookup"><span data-stu-id="6855b-111">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




