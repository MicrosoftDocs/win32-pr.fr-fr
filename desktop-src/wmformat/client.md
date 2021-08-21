---
title: journalisation du Client (kit de développement logiciel (SDK) Windows Media Format 11)
description: en savoir plus sur la journalisation client pour Windows kit de développement logiciel (SDK) Media Format 11. La journalisation permet au serveur multimédia d’effectuer le suivi de l’activité des clients qui s’y connectent.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK, journalisation du client
- Windows Media Format SDK, journalisation
- ASF (Advanced Systems Format), journalisation du client
- ASF (format des systèmes avancés), journalisation du client
- ASF (Advanced Systems Format), journalisation
- ASF (format des systèmes avancés), journalisation
- journalisation du client
- journalisation des clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460058d6ad4009fab301c6ce322df3144bdd0e5d9bb4732d54126f7675cd9e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028027"
---
# <a name="client-logging-windows-media-format-11-sdk"></a>journalisation du Client (kit de développement logiciel (SDK) Windows Media Format 11)

Lorsque l’objet lecteur lit les données à partir d’un serveur, il envoie les informations de journalisation au serveur. Les fournisseurs de contenu utilisent généralement ces informations pour mesurer la qualité de service, générer des informations de facturation ou suivre la publicité. Les informations de journalisation ne contiennent aucune donnée personnelle.

L’application peut spécifier certaines des informations qui sont journalisées, en appelant la méthode [**IWMReaderAdvanced :: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) sur l’objet lecteur. Par exemple, vous pouvez spécifier la chaîne User-agent, le nom de l’application Player ou la page Web qui héberge le lecteur.

Les informations de journalisation incluent un GUID qui identifie la session. Par défaut, le lecteur génère un ID de session anonyme. Le lecteur peut éventuellement envoyer un ID qui identifie de façon unique l’utilisateur actuel. Pour activer cette fonctionnalité, appelez la méthode [**IWMReaderAdvanced2 :: SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) avec la valeur **true**.

Vous pouvez configurer l’objet lecteur pour envoyer les informations de journalisation à un autre serveur, en plus du serveur d’origine. Pour ce faire, appelez la méthode [**IWMReaderNetworkConfig :: AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) avec l’URL du serveur. Cette URL doit pointer vers un script ou un exécutable qui peut gérer les requêtes HTTP et de publication. Vous pouvez utiliser l’agent de publication de la multidiffusion et de la journalisation (wmsiislog.dll), ou vous pouvez écrire un script ASP ou CGI personnalisé pour recevoir les données du journal.

> [!Note]  
> Vous pouvez obtenir la même fonctionnalité en créant une sélection côté serveur avec un attribut **logURL** .

 

Lorsque l’objet lecteur envoie le journal, il effectue les opérations suivantes :

1.  Envoie une requête d’extraction vide au serveur.
2.  Analyse la réponse du serveur pour l’une des chaînes suivantes :
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   `<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` où « 0.0.0.0 » correspond à un numéro de version valide.
3.  Envoie une demande de publication avec les informations du journal.

Le code suivant montre un exemple de script ASP qui reçoit les informations de journalisation et les écrit dans un fichier :


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



Vous pouvez spécifier plusieurs serveurs pour recevoir les informations de journalisation ; il vous suffit d’appeler **AddLoggingUrl** une fois avec chaque URL. Pour effacer la liste des serveurs qui reçoivent des journaux, appelez la méthode [**IWMReaderNetworkConfig :: ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation des fonctionnalités réseau**](implementing-network-functionality.md)
</dt> <dt>

[**Interface IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




