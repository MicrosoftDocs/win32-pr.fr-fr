---
title: Utilisation d’objets COM dans Windows Script Host
description: Microsoft Windows Script Host est un utilitaire de script que vous pouvez utiliser pour exécuter des scripts dans le système d’exploitation de base.
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761587"
---
# <a name="using-com-objects-in-windows-script-host"></a><span data-ttu-id="e76f2-103">Utilisation d’objets COM dans Windows Script Host</span><span class="sxs-lookup"><span data-stu-id="e76f2-103">Using COM Objects in Windows Script Host</span></span>

<span data-ttu-id="e76f2-104">Microsoft Windows Script Host est un utilitaire de script que vous pouvez utiliser pour exécuter des scripts dans le système d’exploitation de base.</span><span class="sxs-lookup"><span data-stu-id="e76f2-104">Microsoft Windows Script Host is a scripting utility you can use to run scripts within the base operating system.</span></span> <span data-ttu-id="e76f2-105">Vous pouvez utiliser Windows Script Host pour automatiser les tâches courantes et créer des macros et des scripts d’ouverture de session performants.</span><span class="sxs-lookup"><span data-stu-id="e76f2-105">You can use Windows Script Host to automate common tasks and to create powerful macros and logon scripts.</span></span> <span data-ttu-id="e76f2-106">Windows Script Host est fourni avec les moteurs de script ActiveX VBScript et JScript.</span><span class="sxs-lookup"><span data-stu-id="e76f2-106">Windows Script Host comes with VBScript and JScript ActiveX scripting engines.</span></span> <span data-ttu-id="e76f2-107">D’autres éditeurs de logiciels fournissent des moteurs de script ActiveX pour les langages tels que PerlScript, PScript, Python, etc.</span><span class="sxs-lookup"><span data-stu-id="e76f2-107">Other software companies provide ActiveX scripting engines for languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="e76f2-108">Pour utiliser un objet COM dans un script exécuté par Windows Script Host, vous devez d’abord créer une instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e76f2-108">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="e76f2-109">Après avoir créé un objet COM, vous pouvez l’utiliser dans des scripts.</span><span class="sxs-lookup"><span data-stu-id="e76f2-109">After a COM object has been created, you can then use it in scripts.</span></span>

<span data-ttu-id="e76f2-110">Windows Script Host se compose de deux applications.</span><span class="sxs-lookup"><span data-stu-id="e76f2-110">Windows Script Host consists of two applications.</span></span> <span data-ttu-id="e76f2-111">L’une exécute des scripts à partir du bureau Windows ( `WScript.exe` ); l’autre exécute des scripts à partir de l’invite de commandes ( `CScript.exe` ).</span><span class="sxs-lookup"><span data-stu-id="e76f2-111">One runs scripts from the Windows desktop (`WScript.exe`); the other runs scripts from the command prompt (`CScript.exe`).</span></span>

<span data-ttu-id="e76f2-112">Pour exécuter un script à partir du bureau, double-cliquez simplement sur un fichier de script.</span><span class="sxs-lookup"><span data-stu-id="e76f2-112">To run a script from the desktop, simply double-click a script file.</span></span> <span data-ttu-id="e76f2-113">Les fichiers de script sont des fichiers texte.</span><span class="sxs-lookup"><span data-stu-id="e76f2-113">Script files are text files.</span></span> <span data-ttu-id="e76f2-114">Par Convention, les fichiers VBScript ont l’extension `.vbs` et les fichiers JScript `.js` .</span><span class="sxs-lookup"><span data-stu-id="e76f2-114">By convention, VBScript files have the extension `.vbs` and JScript files `.js`.</span></span>

<span data-ttu-id="e76f2-115">Pour exécuter un script à partir de l’invite de commandes, exécutez l' `Cscript.exe` application avec une ligne de commande telle que la suivante :</span><span class="sxs-lookup"><span data-stu-id="e76f2-115">To run a script from the command prompt, run the `Cscript.exe` application with a command line such as the following:</span></span>

```console
cscript "c:\\sample scripts\\chart.vbs"
```

<span data-ttu-id="e76f2-116">où `c:\\sample scripts\\chart.vbs` est le chemin d’accès au fichier contenant le script.</span><span class="sxs-lookup"><span data-stu-id="e76f2-116">where `c:\\sample scripts\\chart.vbs` is the path to the file containing the script.</span></span>

<span data-ttu-id="e76f2-117">Vous pouvez imprimer une liste des paramètres pris en charge par Cscript.exe en entrant la ligne de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e76f2-117">You can print out a list of the parameters supported by Cscript.exe by entering the following command line:</span></span>

```console
call cscript //?
```

<span data-ttu-id="e76f2-118">Pour utiliser un objet COM dans un script exécuté par Windows Script Host, vous devez d’abord créer une instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e76f2-118">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="e76f2-119">Dans VBScript, vous pouvez effectuer cette opération en appelant la `CreateObject()` méthode.</span><span class="sxs-lookup"><span data-stu-id="e76f2-119">In VBScript you can do this by calling the `CreateObject()` method.</span></span> <span data-ttu-id="e76f2-120">En JScript, il est possible d’utiliser l' `ActiveXObject` objet ou la `WScript.CreateObject()` méthode.</span><span class="sxs-lookup"><span data-stu-id="e76f2-120">In JScript one can use either the `ActiveXObject` object or the `WScript.CreateObject()` method.</span></span> <span data-ttu-id="e76f2-121">L’exemple suivant illustre l’appel `CreateObject()` à l’aide de VBScript :</span><span class="sxs-lookup"><span data-stu-id="e76f2-121">The following example illustrates calling `CreateObject()` using VBScript:</span></span>


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



<span data-ttu-id="e76f2-122">L’exemple suivant illustre la création d’un `ActiveXObject` objet à l’aide de JScript :</span><span class="sxs-lookup"><span data-stu-id="e76f2-122">The following example illustrates creating an `ActiveXObject` object using JScript:</span></span>


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
<span data-ttu-id="e76f2-123">Vous pouvez également utiliser la `WScript.CreateObject()` méthode dans JScript :</span><span class="sxs-lookup"><span data-stu-id="e76f2-123">Alternatively using `WScript.CreateObject()` method inside JScript:</span></span>

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


<span data-ttu-id="e76f2-124">Après avoir créé une instance de l’objet COM, vous pouvez écrire un script qui utilise l’objet, par exemple :</span><span class="sxs-lookup"><span data-stu-id="e76f2-124">After you have created an instance of the COM object, you can write script that uses the object, for example:</span></span>


```VB
objXL.Visible = true;
 
```



<span data-ttu-id="e76f2-125">En plus de la méthode CreateObject et de l’objet ActiveXObject, VBScript et JScript fournissent la méthode GetObject, qui retourne une instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="e76f2-125">In addition to the CreateObject method and ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e76f2-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e76f2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e76f2-127">Écriture de scripts avec des objets COM</span><span class="sxs-lookup"><span data-stu-id="e76f2-127">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




