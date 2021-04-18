---
title: Reference, élément (déconseillé)
description: Reference, élément (déconseillé)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Fichiers Windows Media, élément Reference
- fichiers de rapport, élément de référence
- Reference, élément
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512056"
---
# <a name="reference-element-deprecated"></a><span data-ttu-id="f5630-106">Reference, élément (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="f5630-106">reference Element (deprecated)</span></span>

<span data-ttu-id="f5630-107">Cette rubrique documente une fonctionnalité qui n’est plus utilisée dans la version actuelle des fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f5630-107">This topic documents a feature that is no longer used in the current version of Windows Media Metafiles.</span></span>

<span data-ttu-id="f5630-108">L’élément **Reference** contient une liste de références aux URL.</span><span class="sxs-lookup"><span data-stu-id="f5630-108">The **reference** element contains a list of references to URLs.</span></span> <span data-ttu-id="f5630-109">Chaque élément de la liste a le formulaire Ref *XX*  =  *URL*, où *XX* est un entier et *URL* est l’URL d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="f5630-109">Each item in the list has the form Ref *XX* = *URL*, where *XX* is an integer and *URL* is the URL of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="f5630-110">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="f5630-110">**Syntax**</span></span>


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



<span data-ttu-id="f5630-111">Les entiers représentés par *XX* doivent être dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="f5630-111">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="f5630-112">Autrement dit, l’entier de chaque ligne doit être supérieur à l’entier de la ligne précédente.</span><span class="sxs-lookup"><span data-stu-id="f5630-112">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="f5630-113">Lorsqu’un programme client lit un élément de référence, il tente de se connecter au fichier multimédia représenté par la première URL de la liste.</span><span class="sxs-lookup"><span data-stu-id="f5630-113">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="f5630-114">En cas d’échec, le programme client tente de se connecter au fichier représenté par l’URL suivante dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f5630-114">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="f5630-115">Le programme client continue la liste jusqu’à ce qu’il établisse une connexion réussie ou qu’il atteigne la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="f5630-115">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="f5630-116">Notez que si le programme client effectue une connexion réussie, il ne lit aucune des URL suivantes dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f5630-116">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

<span data-ttu-id="f5630-117">**Exemple de code**</span><span class="sxs-lookup"><span data-stu-id="f5630-117">**Example Code**</span></span>

<span data-ttu-id="f5630-118">Dans l’exemple suivant, le programme client tente d’abord de se connecter au fichier représenté par l’URL MMS.</span><span class="sxs-lookup"><span data-stu-id="f5630-118">In the following example, the client program would first attempt to connect to the file represented by the mms URL.</span></span> <span data-ttu-id="f5630-119">En cas d’échec, le programme client tente de se connecter au fichier représenté par l’URL http.</span><span class="sxs-lookup"><span data-stu-id="f5630-119">If that failed, the client program would attempt to connect to the file represented by the http URL.</span></span>


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a><span data-ttu-id="f5630-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f5630-120">Remarks</span></span>

<span data-ttu-id="f5630-121">Le format de fichier ASF englobe un large éventail de types de médias, tels que l’audio et la vidéo.</span><span class="sxs-lookup"><span data-stu-id="f5630-121">The ASF file format encompasses a wide variety of media types including audio and video.</span></span> <span data-ttu-id="f5630-122">Les fichiers ASF utilisent également plusieurs extensions de nom de fichier différentes, y compris. WMA et. wmv.</span><span class="sxs-lookup"><span data-stu-id="f5630-122">ASF files also use several different file name extensions, including .wma and .wmv.</span></span>

<span data-ttu-id="f5630-123">Les entiers représentés par *XX* doivent être dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="f5630-123">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="f5630-124">Autrement dit, l’entier de chaque ligne doit être supérieur à l’entier de la ligne précédente.</span><span class="sxs-lookup"><span data-stu-id="f5630-124">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="f5630-125">Lorsqu’un programme client lit un élément de référence, il tente de se connecter au fichier multimédia représenté par la première URL de la liste.</span><span class="sxs-lookup"><span data-stu-id="f5630-125">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="f5630-126">En cas d’échec, le programme client tente de se connecter au fichier représenté par l’URL suivante dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f5630-126">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="f5630-127">Le programme client continue la liste jusqu’à ce qu’il établisse une connexion réussie ou qu’il atteigne la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="f5630-127">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="f5630-128">Notez que si le programme client effectue une connexion réussie, il ne lit aucune des URL suivantes dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f5630-128">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5630-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f5630-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5630-130">**Versions précédentes des fichiers Windows Media (déconseillés)**</span><span class="sxs-lookup"><span data-stu-id="f5630-130">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




