---
description: Décrit comment créer des pages ASP (Microsoft Active Server Pages) qui affichent des informations sur les ordinateurs distants sur des ordinateurs sur lesquels WMI n’est pas installé.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Création de pages de Active Server pour WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 52143284be54868d36b55a6dd86e0b49c82d863d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522231"
---
# <a name="creating-active-server-pages-for-wmi"></a>Création de pages de Active Server pour WMI

Les pages ASP (Microsoft Active Server Pages) peuvent créer des pages Web dynamiques en incluant des scripts côté serveur et côté client. Les pages ASP peuvent être beaucoup plus rapides que les pages HTML du client, car la majeure partie du travail est effectuée sur le serveur. Vous pouvez également utiliser des pages ASP pour afficher des informations sur les ordinateurs distants sur d’autres ordinateurs sur lesquels Windows Management Instrumentation (WMI) n’est pas installé.

La procédure suivante décrit comment utiliser WMI avec ASP.

**Pour utiliser WMI avec ASP**

1.  Écrivez une page ASP (. asp) qui utilise WMI et placez-la dans un répertoire accessible à votre serveur Web.

    Les scripts ASP pour WMI peuvent être développés avec plusieurs langages de script, y compris VBScript. Vous pouvez construire la partie script WMI d’une page ASP exactement comme vous construisez tout autre script qui utilise WMI, avec une restriction importante : vous ne pouvez pas utiliser de méthodes WMI asynchrones dans les pages ASP. Notez également que tous les appels à **GetObject** ou **CreateObject** doivent se trouver dans le code côté serveur. Pour plus d’informations, consultez [API de script pour WMI](scripting-api-for-wmi.md).

2.  Configurez la configuration de l’authentification pour Internet Information Services (IIS). Pour plus d’informations, consultez [configuration d’IIS 5 et versions ultérieures pour les scripts ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).
3.  Désactivez l’accès anonyme, puis activez l’authentification intégrée de Windows pour le fichier ASP. Vous pouvez configurer ces paramètres pour votre page ASP en utilisant le composant logiciel enfichable IIS situé dans le dossier **Outils d’administration** du **panneau de configuration**.

## <a name="wmi-asp-page-example"></a>Exemple de page ASP WMI

L’exemple suivant utilise Windows Management Instrumentation (WMI) dans une page de Active Server (ASP) pour afficher les paramètres adresse IP et passerelle IP par défaut pour le serveur à partir duquel ce script est exécuté.


```VB
<%@ LANGUAGE="VBSCRIPT"%>
<HTML>
<HEAD>
<TITLE>WMI ASP Example:
    Read Default Gateway and IP Address information </TITLE>
</HEAD>

<BODY>

<%
On Error Resume Next
set IPConfigSet = GetObject("winmgmts:" _
   & "{impersonationLevel=impersonate}!root\cimv2").ExecQuery" _
    & "("SELECT IPAddress, DefaultIPGateway "" _ 
    & " FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=TRUE")
%>

<%If Err <> 0 Then %>
    <%if err.number = -2147217405 then%>
        <p>Error 0x80041003: Access Denied: 
           Check permissions and file security for this ASP file.</p>
    <%else%>
        <p>Error description: <%=Err.description%> 
           error number <%=Err.number%></p>
    <%end if%>

<%end if %>

<%for each IPConfig in IPConfigSet%>

    <%if Not IsNull(IPConfig.IPAddress) then %>
        <%for i=LBound(IPConfig.IPAddress) 
            to UBound(IPConfig.IPAddress)%>
            <p>IP Address: <%=IPConfig.IPAddress(i)%></p>
        <%next%>
    <%end if%>
    

    <%if Not IsNull(IPConfig.DefaultIPGateway) then %>
        <%for i=LBound(IPConfig.DefaultIPGateway) 
            to UBound(IPConfig.DefaultIPGateway)%>
            <p>Default IP Gateway: 
                <%=IPConfig.DefaultIPGateway(i)%></p>
        <%next%>
    <%end if%>
<%next%>

<%If Err <> 0 Then %>
    <p>error description: <%=Err.description%> 
       error number <%=Err.number%></p>
<%end if %>

</BODY>
</HTML>
```



 

 



