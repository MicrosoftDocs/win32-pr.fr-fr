---
title: Utilisation d’objets COM dans des pages Active Server
description: Vous pouvez générer des scripts d’objets COM dans des applications ASP (Active Server Pages).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309358"
---
# <a name="using-com-objects-in-active-server-pages"></a><span data-ttu-id="bdfe9-103">Utilisation d’objets COM dans des pages Active Server</span><span class="sxs-lookup"><span data-stu-id="bdfe9-103">Using COM Objects in Active Server Pages</span></span>

<span data-ttu-id="bdfe9-104">Vous pouvez générer des scripts d’objets COM dans des applications ASP (Active Server Pages).</span><span class="sxs-lookup"><span data-stu-id="bdfe9-104">You can script COM objects in Active Server Pages (ASP) applications.</span></span> <span data-ttu-id="bdfe9-105">Pour ce faire, vous devez d’abord créer une instance de l’objet à l’aide de la balise OBJECT ou en appelant la méthode CreateObject de l’objet serveur ASP.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-105">To do so, you must first create an instance of the object either by using the OBJECT tag or by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="bdfe9-106">Une fois qu’un objet COM a été créé, vous pouvez l’utiliser dans les scripts suivants sur la page ASP.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-106">Once a COM object has been created, you can use it in subsequent scripts on the ASP page.</span></span>

<span data-ttu-id="bdfe9-107">À l’aide d’ASP, vous pouvez travailler avec différents types de moteurs de script, chacun prenant en charge un langage de script différent.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-107">Using ASP, you can work with many different types of scripting engines, each of which supports a different scripting language.</span></span> <span data-ttu-id="bdfe9-108">ASP est fourni avec les moteurs de script VBScript et JScript.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-108">ASP comes with VBScript and JScript scripting engines.</span></span> <span data-ttu-id="bdfe9-109">Vous pouvez également intégrer des moteurs de script développés par d’autres entreprises pour prendre en charge des langages tels que PerlScript, PScript, Python et d’autres.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-109">You can also plug in scripting engines developed by other companies to support languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="bdfe9-110">Si vous ne définissez pas le langage de script pour une page ASP, VBScript est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-110">If you do not set the scripting language for an ASP page, VBScript is the default.</span></span> <span data-ttu-id="bdfe9-111">Pour spécifier un langage de script autre que VBScript, ajoutez une ligne telle que la suivante en haut de chaque page ASP :</span><span class="sxs-lookup"><span data-stu-id="bdfe9-111">To specify a scripting language other than VBScript, include a line such as the following at the top of each ASP page:</span></span>

``` syntax
<%@ LANGUAGE=JScript %>
 
```

<span data-ttu-id="bdfe9-112">Pour utiliser un objet COM dans une page ASP, vous devez d’abord créer une instance de cet objet.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-112">To use a COM object in an ASP page, you must first create an instance of that object.</span></span> <span data-ttu-id="bdfe9-113">Pour ce faire, utilisez la balise OBJECT et spécifiez la valeur « SERVER » pour l’attribut RUNAT, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-113">You do this by using the OBJECT tag and specifying the value "SERVER" for the RUNAT attribute, as shown in the following example.</span></span> <span data-ttu-id="bdfe9-114">Par défaut, la balise OBJECT crée une instance de l’objet sur le client.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-114">By default, the OBJECT tag creates an instance of the object on the client.</span></span> <span data-ttu-id="bdfe9-115">L’affectation de la valeur SERVER à l’attribut RUNAT entraîne la création de l’objet sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-115">Setting the RUNAT attribute to SERVER causes the object to be created on the server.</span></span> <span data-ttu-id="bdfe9-116">L’objet doit s’exécuter sur le serveur afin d’être utilisé par ASP.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-116">The object must run on the server in order to be used by ASP.</span></span>

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

<span data-ttu-id="bdfe9-117">Vous pouvez également créer une instance d’un objet COM sur une page ASP en appelant la méthode CreateObject de l’objet serveur ASP.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-117">You can also create an instance of a COM object on an ASP page by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="bdfe9-118">L’utilisation de Server. CreateObject est plus lente que la création de l’objet à l’aide d’une balise OBJECT, mais elle est légèrement plus lisible, car elle spécifie l’identificateur programmatique au lieu de l’identificateur de classe de l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-118">Using Server.CreateObject is slower than creating the object using an OBJECT tag, but it is slightly more readable because it specifies the programmatic identifier instead of the class identifier of the COM object.</span></span> <span data-ttu-id="bdfe9-119">L’objet serveur est exposé par ASP et n’a pas besoin d’être créé.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-119">The Server object is exposed by ASP and does not need to be created.</span></span> <span data-ttu-id="bdfe9-120">L’appel de Server. CreateObject est illustré dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-120">How to call Server.CreateObject is illustrated in the following examples.</span></span> <span data-ttu-id="bdfe9-121">Le premier exemple est VBScript :</span><span class="sxs-lookup"><span data-stu-id="bdfe9-121">The first example is VBScript:</span></span>

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="bdfe9-122">L’exemple suivant est JScript :</span><span class="sxs-lookup"><span data-stu-id="bdfe9-122">The next example is JScript:</span></span>

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="bdfe9-123">L’appel de CreateObject est plus lent que l’utilisation de la balise OBJECT pour créer un objet COM.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-123">Calling CreateObject is slower than using the OBJECT tag to create a COM object.</span></span> <span data-ttu-id="bdfe9-124">Dans les applications où les performances sont critiques, vous devez utiliser la balise OBJECT.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-124">In applications where performance is critical, you should use the OBJECT tag.</span></span>

<span data-ttu-id="bdfe9-125">Une fois que vous avez créé une instance de l’objet COM, vous pouvez l’utiliser dans des scripts.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-125">After you have created an instance of the COM object, you can use it in scripts.</span></span> <span data-ttu-id="bdfe9-126">Cela est illustré dans l’exemple VBScript suivant, qui définit la valeur de la propriété border de l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="bdfe9-126">Doing this is illustrated in the VBScript example following, which sets the value of the COM object's Border property.</span></span>

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a><span data-ttu-id="bdfe9-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdfe9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdfe9-128">Écriture de scripts avec des objets COM</span><span class="sxs-lookup"><span data-stu-id="bdfe9-128">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




