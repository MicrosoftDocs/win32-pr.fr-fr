---
title: Incorporation d’objets COM dans des pages Web
description: Vous pouvez utiliser des objets COM dans des pages Web. Pour ce faire, commencez par créer une instance de cet objet COM. Une fois qu’une instance d’objet est créée, vous pouvez l’utiliser dans les scripts suivants sur cette page Web.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4762dd01d4bc07aab5c0b146c56cdb1aec3cb28f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309729"
---
# <a name="embedding-com-objects-in-web-pages"></a><span data-ttu-id="af44f-105">Incorporation d’objets COM dans des pages Web</span><span class="sxs-lookup"><span data-stu-id="af44f-105">Embedding COM Objects in Web Pages</span></span>

<span data-ttu-id="af44f-106">Vous pouvez utiliser des objets COM dans des pages Web.</span><span class="sxs-lookup"><span data-stu-id="af44f-106">You can use COM objects in webpages.</span></span> <span data-ttu-id="af44f-107">Pour ce faire, commencez par créer une instance de cet objet COM.</span><span class="sxs-lookup"><span data-stu-id="af44f-107">To do this, first create an instance of that COM object.</span></span> <span data-ttu-id="af44f-108">Une fois qu’une instance d’objet est créée, vous pouvez l’utiliser dans les scripts suivants sur cette page Web.</span><span class="sxs-lookup"><span data-stu-id="af44f-108">After an object instance is created, you can use it in subsequent scripts on that webpage.</span></span>

<span data-ttu-id="af44f-109">Pour créer une instance d’objet COM dans une page Web, vous pouvez utiliser une balise d’objet.</span><span class="sxs-lookup"><span data-stu-id="af44f-109">To create a COM object instance in a webpage, you can use an OBJECT tag.</span></span> <span data-ttu-id="af44f-110">Si votre langage de script fournit une méthode native pour créer des objets COM, vous pouvez également créer une instance d’objet à l’aide d’un script.</span><span class="sxs-lookup"><span data-stu-id="af44f-110">Alternatively, if your scripting language provides a native way to create COM objects, you can create an object instance using script.</span></span>

<span data-ttu-id="af44f-111">Notez que l’incorporation d’objets COM dans des pages Web fonctionne uniquement avec les navigateurs qui prennent en charge ActiveX et COM, par exemple Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="af44f-111">Note that embedding COM objects in webpages only works with browsers that support ActiveX and COM, for example Internet Explorer.</span></span>

<span data-ttu-id="af44f-112">L’exemple suivant illustre l’utilisation de la balise OBJECT pour incorporer un objet COM dans une page Web :</span><span class="sxs-lookup"><span data-stu-id="af44f-112">The following example illustrates using the OBJECT tag to embed a COM object in a webpage:</span></span>

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

<span data-ttu-id="af44f-113">Vous pouvez également créer une instance d’objet COM dans un script, si votre langage de script permet de créer des objets COM.</span><span class="sxs-lookup"><span data-stu-id="af44f-113">You can also create a COM object instance in script, if your scripting language provides a way to create COM objects.</span></span> <span data-ttu-id="af44f-114">Par exemple, VBScript fournit la méthode CreateObject et JScript fournit l’objet ActiveXObject.</span><span class="sxs-lookup"><span data-stu-id="af44f-114">For example, VBScript provides the CreateObject method and JScript provides the ActiveXObject object.</span></span> <span data-ttu-id="af44f-115">La création d’objets dans le script est illustrée dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="af44f-115">Creating objects in script is illustrated in the following examples.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

<span data-ttu-id="af44f-116">Outre la méthode CreateObject et l’objet ActiveXObject, VBScript et JScript fournissent la méthode GetObject, qui retourne une instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="af44f-116">In addition to the CreateObject method and the ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

<span data-ttu-id="af44f-117">Une fois qu’un objet COM a été créé, vous pouvez le référencer dans les scripts suivants à l’aide de l’identificateur spécifié dans l’attribut ID de la balise d’objet.</span><span class="sxs-lookup"><span data-stu-id="af44f-117">After a COM object has been created, you can reference it in subsequent scripts by using the identifier specified in the OBJECT tag's ID attribute.</span></span> <span data-ttu-id="af44f-118">Dans l’exemple précédent, cet identificateur a été spécifié en tant que « vid ».</span><span class="sxs-lookup"><span data-stu-id="af44f-118">In the preceding example, this identifier was specified as "vid."</span></span> <span data-ttu-id="af44f-119">Notez que le script qui utilise l’objet COM doit apparaître après la balise d’objet ou le script qui crée l’instance d’objet ; dans le cas contraire, l’identificateur d’objet n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="af44f-119">Note that the script that uses the COM object must appear after the OBJECT tag or script that creates the object instance; otherwise, the object identifier is undefined.</span></span> <span data-ttu-id="af44f-120">Le script suivant utilise l’objet objXL pour afficher les informations de version de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="af44f-120">The following script uses the objXL object to display the version information for Microsoft Excel.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

<span data-ttu-id="af44f-121">Si vous écrivez des scripts incorporés dans une page Web, le navigateur expose également un modèle objet auquel vos scripts peuvent accéder.</span><span class="sxs-lookup"><span data-stu-id="af44f-121">If you are writing scripts embedded in a webpage, the browser also exposes an object model that your scripts can access.</span></span> <span data-ttu-id="af44f-122">Le modèle utilisé par Internet Explorer est conforme au Document Object Model (DOM) proposé par le World Wide Web Consortium (W3C).</span><span class="sxs-lookup"><span data-stu-id="af44f-122">The model used by Internet Explorer conforms to the Document Object Model (DOM) proposed by the World Wide Web Consortium (W3C).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af44f-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af44f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af44f-124">Écriture de scripts avec des objets COM</span><span class="sxs-lookup"><span data-stu-id="af44f-124">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




