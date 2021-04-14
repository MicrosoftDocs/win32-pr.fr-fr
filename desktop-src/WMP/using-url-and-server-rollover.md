---
title: Utilisation de la substitution d’URL et de serveur
description: Utilisation de la substitution d’URL et de serveur
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Sélections de métafichiers Windows Media, substitutions d’URL
- sélections, substitutions d’URL
- sélections de métafichiers, substitutions d’URL
- Sélections de métafichiers Windows Media, substitutions de serveur
- sélections, substitutions de serveur
- sélections de métafichiers, substitutions de serveur
- Sélections de métafichiers Windows Media, substitutions de protocole
- sélections, substitutions de protocole
- sélections de métafichiers, substitutions de protocole
- Lecteur Windows Media, substitutions d’URL
- Windows Media Player, substitutions de serveur
- Lecteur Windows Media, substitutions de protocole
- Substitutions d’URL
- substitutions de serveur
- substitutions de protocole
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310169"
---
# <a name="using-url-and-server-rollover"></a><span data-ttu-id="b84d9-118">Utilisation de la substitution d’URL et de serveur</span><span class="sxs-lookup"><span data-stu-id="b84d9-118">Using URL and Server Rollover</span></span>

<span data-ttu-id="b84d9-119">Vous pouvez utiliser des sélections de métafichiers pour fournir un moyen de basculer automatiquement vers d’autres sources de contenu lorsqu’un flux n’est pas accessible ou lu.</span><span class="sxs-lookup"><span data-stu-id="b84d9-119">You can use metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span> <span data-ttu-id="b84d9-120">Vous pouvez utiliser cette méthode de substitution pour spécifier les sources du même contenu sur différents serveurs ou sur différents types de serveurs.</span><span class="sxs-lookup"><span data-stu-id="b84d9-120">You can use this rollover method to specify sources of the same content on different servers or different types of servers.</span></span> <span data-ttu-id="b84d9-121">Vous pouvez, par exemple, spécifier un premier remplacement sur un autre serveur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b84d9-121">You can, for example, specify a first alternate on a different Windows Media server.</span></span> <span data-ttu-id="b84d9-122">En cas d’échec de lecture de ce contenu, le client peut basculer vers une deuxième alternative sur un serveur Web.</span><span class="sxs-lookup"><span data-stu-id="b84d9-122">If that content fails to play, the client can roll over to a second alternate on a web server.</span></span> <span data-ttu-id="b84d9-123">Le lecteur Windows Media essaie automatiquement de basculer vers différents protocoles selon ses paramètres de propriété Windows Media avant d’essayer les URL de substitution dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="b84d9-123">Windows Media Player automatically tries to roll over to different protocols according to its Windows Media property settings before trying the rollover URLs in the playlist.</span></span>

<span data-ttu-id="b84d9-124">Définissez la substitution de serveur et de protocole en plaçant successivement plusieurs éléments **ref** dans un élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="b84d9-124">Set server and protocol rollover by placing multiple **REF** elements in succession within one **ENTRY** element.</span></span> <span data-ttu-id="b84d9-125">Chaque élément **ref** spécifie un autre emplacement ou protocole pour un fichier multimédia ou un flux.</span><span class="sxs-lookup"><span data-stu-id="b84d9-125">Each **REF** element specifies an alternate location or protocol for a media file or stream.</span></span>

<span data-ttu-id="b84d9-126">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="b84d9-126">Example Code</span></span>


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="b84d9-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b84d9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b84d9-128">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="b84d9-128">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="b84d9-129">**Utilisation des sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="b84d9-129">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




