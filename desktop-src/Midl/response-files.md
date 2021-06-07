---
title: Fichiers réponse
description: Au lieu de placer toutes les options sur la ligne de commande, le compilateur MIDL accepte les fichiers réponse qui contiennent des commutateurs et des arguments.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL du compilateur MIDL, fichiers réponse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387069"
---
# <a name="response-files"></a><span data-ttu-id="dc43c-104">Fichiers réponse</span><span class="sxs-lookup"><span data-stu-id="dc43c-104">Response Files</span></span>

<span data-ttu-id="dc43c-105">Au lieu de placer toutes les options sur la ligne de commande, le compilateur MIDL accepte les fichiers réponse qui contiennent des commutateurs et des arguments.</span><span class="sxs-lookup"><span data-stu-id="dc43c-105">As an alternative to placing all the options on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="dc43c-106">Un fichier réponse est un fichier texte contenant une ou plusieurs options de ligne de commande du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="dc43c-106">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="dc43c-107">Contrairement à une ligne de commande, un fichier réponse autorise plusieurs lignes d’options et de noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dc43c-107">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="dc43c-108">Cela peut être utile en raison des limitations de votre environnement de génération ou de la commodité pour votre processus de génération.</span><span class="sxs-lookup"><span data-stu-id="dc43c-108">This may be useful due to limitations of your build environment or as a convenience for your build process.</span></span> <span data-ttu-id="dc43c-109">Vous pouvez spécifier un fichier réponse MIDL comme suit :</span><span class="sxs-lookup"><span data-stu-id="dc43c-109">You can specify a MIDL response file as:</span></span>

<span data-ttu-id="dc43c-110"> **\@ nom de fichier** MIDL</span><span class="sxs-lookup"><span data-stu-id="dc43c-110">**midl** **\@filename**</span></span>

<dl> <dt>

<span data-ttu-id="dc43c-111"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="dc43c-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="dc43c-112">Spécifie le nom du fichier réponse.</span><span class="sxs-lookup"><span data-stu-id="dc43c-112">Specifies the name of the response file.</span></span> <span data-ttu-id="dc43c-113">Le nom du fichier réponse doit immédiatement suivre le caractère @ sans espace blanc entre le caractère @ et le nom du fichier réponse.</span><span class="sxs-lookup"><span data-stu-id="dc43c-113">The response file name must immediately follow the @ character with no white space between the @ character and the response file name.</span></span>

</dd> </dl>

<span data-ttu-id="dc43c-114">Les options d’un fichier réponse sont interprétées comme si elles étaient présentes à cet emplacement dans la ligne de commande MIDL.</span><span class="sxs-lookup"><span data-stu-id="dc43c-114">Options in a response file are interpreted as if they were present at that place in the MIDL command line.</span></span> <span data-ttu-id="dc43c-115">Chaque argument d’un fichier réponse doit commencer et se terminer sur la même ligne.</span><span class="sxs-lookup"><span data-stu-id="dc43c-115">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="dc43c-116">Vous ne pouvez pas utiliser la barre oblique inverse ( \\ ) pour concaténer des lignes.</span><span class="sxs-lookup"><span data-stu-id="dc43c-116">You cannot use the backslash character (\\) to concatenate lines.</span></span>

<span data-ttu-id="dc43c-117">MIDL prend en charge les arguments de ligne de commande qui incluent un ou plusieurs fichiers réponse, associés à d’autres commutateurs de ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="dc43c-117">MIDL supports command-line arguments that include one or more response files, combined with other command-line switches:</span></span>

<span data-ttu-id="dc43c-118">**MIDL-Oicf @midl1.rsp -envwin32 @midl2.rsp ITF. idl**</span><span class="sxs-lookup"><span data-stu-id="dc43c-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span></span>

<span data-ttu-id="dc43c-119">Le compilateur MIDL ne prend pas en charge les fichiers réponse imbriqués.</span><span class="sxs-lookup"><span data-stu-id="dc43c-119">The MIDL compiler does not support nested response files.</span></span>

 

 




