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
# <a name="creating-active-server-pages-for-wmi"></a><span data-ttu-id="51a08-103">Création de pages de Active Server pour WMI</span><span class="sxs-lookup"><span data-stu-id="51a08-103">Creating Active Server Pages for WMI</span></span>

<span data-ttu-id="51a08-104">Les pages ASP (Microsoft Active Server Pages) peuvent créer des pages Web dynamiques en incluant des scripts côté serveur et côté client.</span><span class="sxs-lookup"><span data-stu-id="51a08-104">Microsoft Active Server Pages (ASP) can create dynamic webpages by including both server-side and client-side scripts.</span></span> <span data-ttu-id="51a08-105">Les pages ASP peuvent être beaucoup plus rapides que les pages HTML du client, car la majeure partie du travail est effectuée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="51a08-105">ASP pages can be much faster than client HTML pages because most of the work is done on the server.</span></span> <span data-ttu-id="51a08-106">Vous pouvez également utiliser des pages ASP pour afficher des informations sur les ordinateurs distants sur d’autres ordinateurs sur lesquels Windows Management Instrumentation (WMI) n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="51a08-106">You can also use ASP pages to display information about remote computers to other computers that do not have Windows Management Instrumentation (WMI) installed.</span></span>

<span data-ttu-id="51a08-107">La procédure suivante décrit comment utiliser WMI avec ASP.</span><span class="sxs-lookup"><span data-stu-id="51a08-107">The following procedure describes how to use WMI with ASP.</span></span>

<span data-ttu-id="51a08-108">**Pour utiliser WMI avec ASP**</span><span class="sxs-lookup"><span data-stu-id="51a08-108">**To use WMI with ASP**</span></span>

1.  <span data-ttu-id="51a08-109">Écrivez une page ASP (. asp) qui utilise WMI et placez-la dans un répertoire accessible à votre serveur Web.</span><span class="sxs-lookup"><span data-stu-id="51a08-109">Write an ASP page (.asp) that uses WMI, and place it in a directory accessible to your web server.</span></span>

    <span data-ttu-id="51a08-110">Les scripts ASP pour WMI peuvent être développés avec plusieurs langages de script, y compris VBScript.</span><span class="sxs-lookup"><span data-stu-id="51a08-110">ASP scripts for WMI can be developed with several scripting languages, including VBScript.</span></span> <span data-ttu-id="51a08-111">Vous pouvez construire la partie script WMI d’une page ASP exactement comme vous construisez tout autre script qui utilise WMI, avec une restriction importante : vous ne pouvez pas utiliser de méthodes WMI asynchrones dans les pages ASP.</span><span class="sxs-lookup"><span data-stu-id="51a08-111">You can construct the WMI script part of an ASP page exactly as you construct any other script that uses WMI, with one important restriction: you cannot use asynchronous WMI methods within ASP pages.</span></span> <span data-ttu-id="51a08-112">Notez également que tous les appels à **GetObject** ou **CreateObject** doivent se trouver dans le code côté serveur.</span><span class="sxs-lookup"><span data-stu-id="51a08-112">Note also that any calls to **GetObject** or **CreateObject** must be in the server-side code.</span></span> <span data-ttu-id="51a08-113">Pour plus d’informations, consultez [API de script pour WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="51a08-113">For more information, see [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="51a08-114">Configurez la configuration de l’authentification pour Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="51a08-114">Set up authentication configuration for Internet Information Services (IIS).</span></span> <span data-ttu-id="51a08-115">Pour plus d’informations, consultez [configuration d’IIS 5 et versions ultérieures pour les scripts ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="51a08-115">For more information, see [Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>
3.  <span data-ttu-id="51a08-116">Désactivez l’accès anonyme, puis activez l’authentification intégrée de Windows pour le fichier ASP.</span><span class="sxs-lookup"><span data-stu-id="51a08-116">Disable anonymous access, and enable Windows Integrated Authentication for the ASP file.</span></span> <span data-ttu-id="51a08-117">Vous pouvez configurer ces paramètres pour votre page ASP en utilisant le composant logiciel enfichable IIS situé dans le dossier **Outils d’administration** du **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="51a08-117">You can configure these settings for your ASP page by using the IIS snap-in located in the **Administrative Tools** folder of the **Control Panel**.</span></span>

## <a name="wmi-asp-page-example"></a><span data-ttu-id="51a08-118">Exemple de page ASP WMI</span><span class="sxs-lookup"><span data-stu-id="51a08-118">WMI ASP Page Example</span></span>

<span data-ttu-id="51a08-119">L’exemple suivant utilise Windows Management Instrumentation (WMI) dans une page de Active Server (ASP) pour afficher les paramètres adresse IP et passerelle IP par défaut pour le serveur à partir duquel ce script est exécuté.</span><span class="sxs-lookup"><span data-stu-id="51a08-119">The following example uses Windows Management Instrumentation (WMI) within an Active Server Page (ASP) to display the IP address and default IP gateway settings for the server from which this script is executed.</span></span>


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



 

 



