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
ms.openlocfilehash: f17c5d32fea196d77b8fb54463231e1bc1bc165c6bd48e49dffb351a9d6d45dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082563"
---
# <a name="getting-started-with-asp-for-adsi"></a>Prise en main avec ASP pour ADSI

ADSI peut être utilisé pour accéder aux données d’annuaire à l’aide d’une page ASP. Cela peut être un moyen pratique d’exécuter des tâches et des requêtes d’administration à partir d’une page Web ou de fournir des informations aux employés sur un intranet.

l’un des avantages de l’utilisation d’ADSI avec ASP est que vous pouvez créer une expérience utilisateur plus riche, car vous pouvez utiliser Visual Basic pour créer une application ADSI et l’offrir à un utilisateur par le biais d’une page web standard. Par exemple, vous pouvez créer une page Web qui permet aux employés d’entrer le nom de famille d’un employé et de récupérer un numéro de téléphone pour cet employé, ou de créer un formulaire permettant aux employés de mettre à jour les informations personnelles dans une base de données de ressources humaines de l’entreprise.

Le code ASP commence par « <% » et se termine par « % > ». Vous pouvez ajouter du code ADSI en VBScript ou Visual Basic.

pour créer une page ASP, vous pouvez utiliser un éditeur de page web, Bloc-notes ou un autre éditeur de texte ou le système de développement Microsoft Visual Studio .net.

Avant d’exécuter votre page ASP, configurez votre application ou votre serveur IIS en suivant les instructions figurant dans [problèmes d’authentification pour ADSI avec ASP](authentication-issues-for-adsi-with-asp.md).

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a>Exemple ASP simple : énumération d’objets dans un conteneur

À l’aide d’un éditeur de page Web, créez une nouvelle page HTML qui accepte le nom unique d’un objet conteneur. Entrez l’exemple de code suivant.


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



Cette page peut désormais accepter un nom de conteneur qui lui est transmis et utiliser ADSI pour énumérer des objets dans le conteneur.

Créez une nouvelle page ASP nommée Enum. asp et entrez l’exemple de code suivant. Enregistrez cette page à la racine du serveur Web local.


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



 

 




