---
title: Utilisation de pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media
description: Utilisation de pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Sélections de métafichiers Windows Media, création
- sélections de métafichiers, création
- sélections, création
- Sélections de métafichiers Windows Media, création dynamique
- sélections de métafichiers, création dynamique
- sélections, création dynamique
- Sélections de métafichiers Windows Media, pages ASP
- sélections de métafichiers, pages ASP
- sélections, pages ASP
- création de sélections de métafichiers Windows Media
- création dynamique de sélections de métafichiers Windows Media
- pages ASP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507182"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>Utilisation de pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media

Vous pouvez utiliser les pages de Active Server (fichiers ASP ou. asp) pour générer dynamiquement des sélections en fonction des informations fournies par les utilisateurs. Une page ASP est une page Web dynamique utilisée conjointement avec Microsoft Internet Information Services (IIS). ASP est un environnement dans lequel vous pouvez combiner du code HTML, des scripts et des composants serveur ActiveX réutilisables pour créer des solutions métier dynamiques et puissantes basées sur le Web. Les pages ASP activent les scripts côté serveur pour IIS avec la prise en charge native pour Microsoft Visual Basic Scripting Edition (VBScript) et Microsoft JScript. Cette discussion part du principe que vous êtes familiarisé avec ASP et en définissant des variables.

Toutes les informations d’en-tête doivent être contenues sur la première ligne de la chaîne de page ASP retournée au lecteur Windows Media.

Lorsque vous utilisez des pages ASP pour générer des sélections, vous devez spécifier des valeurs pour les propriétés **ContentType** et **Expires** de l’objet de **réponse** dans la page ASP en raison de problèmes de latence avec le lecteur Windows Media. La valeur **Response. ContentType** doit être une extension de nom de fichier valide pour les fichiers Windows Media. Les valeurs acceptables sont WMA, Wax, WMV, wvx, ASF et asx.

La propriété **Response. Expires** spécifie la durée, en secondes, pendant laquelle le lecteur Windows Media met en cache le fichier de sélection. Si vous spécifiez la valeur zéro, le lecteur Windows Media demande une nouvelle sélection à partir du serveur chaque fois que l’utilisateur actualise la page.

Pour plus d’informations sur l’utilisation de l’objet de **réponse** dans Active Server pages, consultez le kit de développement Platform SDK.

Le code suivant est un exemple de page ASP utilisée pour générer une sélection de métafichiers Windows Media.


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> </dl>

 

 




