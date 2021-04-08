---
title: Prise en main avec ASP pour ADSI
description: ADSI peut être utilisé pour accéder aux données d’annuaire à l’aide d’une page ASP. Cela peut être un moyen pratique d’exécuter des tâches et des requêtes d’administration à partir d’une page Web ou de fournir des informations aux employés sur un intranet.
ms.assetid: 2007257c-6c4e-415e-9ab5-e65d8d9e5dd4
ms.tgt_platform: multiple
keywords:
- ADSI ASP
- ADSI, pages ASP
- ADSI, pages ASP, exemple de code ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5b18093c3817d7a6c3d0224b722f8dd4983c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671146"
---
# <a name="getting-started-with-asp-for-adsi"></a><span data-ttu-id="e7dbb-107">Prise en main avec ASP pour ADSI</span><span class="sxs-lookup"><span data-stu-id="e7dbb-107">Getting Started with ASP for ADSI</span></span>

<span data-ttu-id="e7dbb-108">ADSI peut être utilisé pour accéder aux données d’annuaire à l’aide d’une page ASP.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-108">ADSI can be used to access directory data using an ASP page.</span></span> <span data-ttu-id="e7dbb-109">Cela peut être un moyen pratique d’exécuter des tâches et des requêtes d’administration à partir d’une page Web ou de fournir des informations aux employés sur un intranet.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-109">This can be a convenient way to run administration tasks and queries from a webpage or provide information to employees on an intranet.</span></span>

<span data-ttu-id="e7dbb-110">L’un des avantages de l’utilisation d’ADSI avec ASP est que vous pouvez créer une expérience utilisateur plus riche, car vous pouvez utiliser Visual Basic pour créer une application ADSI et l’offrir à un utilisateur par le biais d’une page Web standard.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-110">One advantage of using ADSI with ASP is that you can create a richer user experience because you can use Visual Basic to create an ADSI application and offer it to a user through a standard webpage.</span></span> <span data-ttu-id="e7dbb-111">Par exemple, vous pouvez créer une page Web qui permet aux employés d’entrer le nom de famille d’un employé et de récupérer un numéro de téléphone pour cet employé, ou de créer un formulaire permettant aux employés de mettre à jour les informations personnelles dans une base de données de ressources humaines de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-111">For example, you could create a webpage that enables employees to enter the last name of an employee and get back a phone number for that employee, or create a form that allows employees to update personal information in a company human resources database.</span></span>

<span data-ttu-id="e7dbb-112">Le code ASP commence par « <% » et se termine par « % > ».</span><span class="sxs-lookup"><span data-stu-id="e7dbb-112">ASP code starts with '<%' and ends with '%>'.</span></span> <span data-ttu-id="e7dbb-113">Vous pouvez ajouter du code ADSI en VBScript ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-113">You can add ADSI code as VBScript or Visual Basic.</span></span>

<span data-ttu-id="e7dbb-114">Pour créer une page ASP, vous pouvez utiliser l’éditeur de page Web, le bloc-notes ou tout autre éditeur de texte ou le système de développement Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-114">To create an ASP page, you can use a webpage editor, Notepad or other text editor, or the Microsoft Visual Studio .NET development system.</span></span>

<span data-ttu-id="e7dbb-115">Avant d’exécuter votre page ASP, configurez votre application ou votre serveur IIS en suivant les instructions figurant dans [problèmes d’authentification pour ADSI avec ASP](authentication-issues-for-adsi-with-asp.md).</span><span class="sxs-lookup"><span data-stu-id="e7dbb-115">Before you run your ASP page, set up your application or IIS server according to the instructions found in [Authentication Issues for ADSI with ASP](authentication-issues-for-adsi-with-asp.md).</span></span>

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a><span data-ttu-id="e7dbb-116">Exemple ASP simple : énumération d’objets dans un conteneur</span><span class="sxs-lookup"><span data-stu-id="e7dbb-116">A Simple ASP Sample: Enumerating Objects in a Container</span></span>

<span data-ttu-id="e7dbb-117">À l’aide d’un éditeur de page Web, créez une nouvelle page HTML qui accepte le nom unique d’un objet conteneur.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-117">Using a webpage editor, create a new html page which accepts the distinguished name of a container object.</span></span> <span data-ttu-id="e7dbb-118">Entrez l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-118">Enter the following code example.</span></span>


```HTML
<html>
<body>

<form method="POST" action="https://localhost/Enum.asp" ID="Form1">
<p>Distinguished name of container:<input type="text" name="inpContainer" size="100" ID="Text2"></p>
<p><input type="SUBMIT" value="GO" ID="Submit1" NAME="Submit1"></p>
</form>

</body>
</html>
```



<span data-ttu-id="e7dbb-119">Cette page peut désormais accepter un nom de conteneur qui lui est transmis et utiliser ADSI pour énumérer des objets dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-119">This page can now accept a container name that is passed to it and use ADSI to enumerate objects in the container.</span></span>

<span data-ttu-id="e7dbb-120">Créez une nouvelle page ASP nommée Enum. asp et entrez l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-120">Create a new ASP page called Enum.asp and enter the following code example.</span></span> <span data-ttu-id="e7dbb-121">Enregistrez cette page à la racine du serveur Web local.</span><span class="sxs-lookup"><span data-stu-id="e7dbb-121">Save this page at the root of the local web server.</span></span>


```VB
<%@ Language=VBScript %>
<%
' Get the inputs.
containerName = Request.Form("inpContainer")
' Validate compName before using.

If Not ("" = containerName) Then
  ' Bind to the object.
  adsPath = "LDAP://" & containerName
  Set comp = GetObject(adsPath)

  ' Write the ADsPath of each of the child objects.
  Response.Write("<p>Enumeration:</p>")
  For Each obj in comp
    Response.Write(obj.ADsPath + "<BR>")
  Next
End If
%>
```



 

 




