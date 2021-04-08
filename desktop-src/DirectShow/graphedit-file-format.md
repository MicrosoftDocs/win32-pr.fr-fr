---
description: Format de fichier GraphEdit
ms.assetid: 84c2de05-6c8f-45f1-b789-04a24cfa3ea1
title: Format de fichier GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a75421ff75c9bb26901eddf423448bbd9e4f478
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747629"
---
# <a name="graphedit-file-format"></a><span data-ttu-id="7e587-103">Format de fichier GraphEdit</span><span class="sxs-lookup"><span data-stu-id="7e587-103">GraphEdit File Format</span></span>

<span data-ttu-id="7e587-104">Lorsque l’utilitaire GraphEdit enregistre un graphique de filtre DirectShow, il crée des fichiers de stockage avec une extension. GRF.</span><span class="sxs-lookup"><span data-stu-id="7e587-104">When the GraphEdit utility saves a DirectShow filter graph, it creates a storage files with a .grf extension.</span></span> <span data-ttu-id="7e587-105">Le fichier de stockage contient un seul flux appelé ActiveMovieGraph.</span><span class="sxs-lookup"><span data-stu-id="7e587-105">The storage file contains a single stream called ActiveMovieGraph.</span></span> <span data-ttu-id="7e587-106">Ce flux contient des informations sur tous les filtres, les noms de filtres, les noms de fichiers, les connexions, etc.</span><span class="sxs-lookup"><span data-stu-id="7e587-106">This stream contains information about all of the filters, filter names, file names, connections, and so forth.</span></span>

<span data-ttu-id="7e587-107">La grammaire suivante décrit la syntaxe du graphique dans le flux, à l’aide d’une syntaxe BNF (Backus-Naur Form) modifiée :</span><span class="sxs-lookup"><span data-stu-id="7e587-107">The following grammar describes the syntax of the graph within the stream, using a modified BNF (Backus-Naur Form) syntax:</span></span>


```C++
<graph> ::= 
0003\r\n<filters><connections><clock>
END | 
0002\r\n<filters><connections>
END
<filters> ::= 
FILTERS<b> 
[<filter list><b>
]
<filter list> ::= <filter><b> 
[<filter list>
]
<filter> ::= <filter id><b><name><b><class id><b>
[<file>
]<length><b1><filter data>
<class id> ::= <guid>
<file> ::= 
SOURCE <name><b> | 
SINK <name><b>
<connections> ::= 
CONNECTIONS<b> 
{<connection><b>
}
<connection> ::= <filter id><b><pin id><b><filter id><b><pin id><b><media type>
<filter id> ::= <id>
<pin id> ::= <name>
<media type> ::= <sample size><major type><b><subtype><b><flags><format>
<major type> ::= <guid>
<subtype> ::= <guid>
<flags> ::= <fixed sample size><b><temporal compression><b>
<fixed sample size> ::= 1 
| 0
<temporal compression> ::= 1 
| 0
<format> ::= <length><b1><format type><b><length><b1><format data>
<format type> ::= <guid>
<format data> ::= 
{ binary_data 
}
<clock> ::= 
CLOCK <b><required><b><clockid>
\r\n
<required> ::= 1 
| 0
<clockid> ::= <filter id> 
| <class id>
<name> ::= quote_symbol 
{ any_non_quote_character 
} quote_symbol
<length> ::= unsigned decimal number (as a string), indicating the number 
             of bytes of data in the following token.
<guid> ::= GUID in string format. for example: {CF49D4E0-1115-11CE-B03A-0020AF0BA770}
<b> ::= 
{ space_character 
} 
{ \t 
} 
{ \r 
} 
{ \n 
} { <b> 
}
<b1> ::= space_character
<id> ::= integer (as a string), such as 0001
```



<span data-ttu-id="7e587-108">En sortie, il y aura une nouvelle ligne (« \\ r \\ n ») par filtre, une par connexion et une pour chacun des filtres et des connexions de mots clés.</span><span class="sxs-lookup"><span data-stu-id="7e587-108">On output there will be a new line ("\\r\\n") per filter, one per connection, and one for each of the keywords FILTERS and CONNECTIONS.</span></span> <span data-ttu-id="7e587-109">Chaque autre cas de <b> est un espace unique.</span><span class="sxs-lookup"><span data-stu-id="7e587-109">Each other case of <b> will be a single space.</span></span> <span data-ttu-id="7e587-110">Les mots clés FILTERs, CONNECTions et END ne sont pas localisables.</span><span class="sxs-lookup"><span data-stu-id="7e587-110">The keywords FILTERS, CONNECTIONS, and END are not localizable.</span></span> <span data-ttu-id="7e587-111">Notez également que les données de filtre et les données de format sont binaires, de sorte qu’elles peuvent contenir des sauts de ligne incorrects, des valeurs NULL, etc.</span><span class="sxs-lookup"><span data-stu-id="7e587-111">Note also that the filter data and the format data are binary, so they might contain incorrect line breaks, null values, and so on.</span></span> <span data-ttu-id="7e587-112">Le flux utilise des caractères larges.</span><span class="sxs-lookup"><span data-stu-id="7e587-112">The stream uses wide characters.</span></span>

<span data-ttu-id="7e587-113">L’exemple suivant montre un graphique standard.</span><span class="sxs-lookup"><span data-stu-id="7e587-113">The following shows a typical graph.</span></span> <span data-ttu-id="7e587-114">(Les lignes de connexion ont été interrompues par souci de clarté et les données binaires sont omises.)</span><span class="sxs-lookup"><span data-stu-id="7e587-114">(The connection lines have been broken for clarity, and the binary data omitted.)</span></span>


```C++
003
FILTERS
0001 "C:\SomeFile.avi" {E436EBB5-524F-11CE-9F53-0020AF0BA770} SOURCE "C:\SomeFile.avi" 0000000000 
0002 "AVI Splitter" {1B544C20-FD0B-11CE-8C63-00AA0044B51E} 0000000000 
0003 "AVI Decompressor" {CF49D4E0-1115-11CE-B03A-0020AF0BA770} 0000000000
0004 "Video Renderer" {70E102B0-5556-11CE-97C0-00AA0055595A} 0000000000
CONNECTIONS
0001 "Output" 0002 "input pin" 0000000288 
   {E436EB83-524F-11CE-9F53-0020AF0BA770} 
   {E436EB88-524F-11CE-9F53-0020AF0BA770} 1 0 0000000001 
   {00000000-0000-0000-0000-000000000000} 0000000000  
0002 "Stream 00" 0003 "In" 0000000376 
   {73646976-0000-0010-8000-00AA00389B71} 
   {64697663-0000-0010-8000-00AA00389B71} 0 0 0000000001 
   {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data>
0003 "Out" 0004 "In" 0000000376 
    {73646976-0000-0010-8000-00AA00389B71} 
    {E436EB7D-524F-11CE-9F53-0020AF0BA770} 1 0 0000129600 
    {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data> 
CLOCK 1 0000
END
```



## <a name="related-topics"></a><span data-ttu-id="7e587-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e587-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e587-116">Simulation de la génération de graphiques avec GraphEdit</span><span class="sxs-lookup"><span data-stu-id="7e587-116">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



