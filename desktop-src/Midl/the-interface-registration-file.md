---
title: Fichier d’inscription de l’interface
description: Le fichier d’inscription de l’interface collecte des informations qui facilitent l’inscription des interfaces COM empaquetées dans un fichier DLL ou EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- MIDL du fichier d’inscription de l’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511284"
---
# <a name="the-interface-registration-file"></a><span data-ttu-id="3b317-104">Fichier d’inscription de l’interface</span><span class="sxs-lookup"><span data-stu-id="3b317-104">The Interface Registration File</span></span>

<span data-ttu-id="3b317-105">Le fichier d’inscription de l’interface collecte des informations qui facilitent l’inscription des interfaces COM empaquetées dans un fichier DLL ou EXE.</span><span class="sxs-lookup"><span data-stu-id="3b317-105">The interface registration file collects information that helps in the registration of COM interfaces packaged into a DLL or EXE file.</span></span> <span data-ttu-id="3b317-106">Le fichier d’inscription de l’interface est différent des autres fichiers générés, car il peut recueillir des informations à partir de la compilation de plusieurs fichiers IDL différents.</span><span class="sxs-lookup"><span data-stu-id="3b317-106">The interface registration file is different from other generated files because it can gather information from compiling several different IDL files.</span></span> <span data-ttu-id="3b317-107">Chaque compilateur MIDL exécuté pour les interfaces COM recherche d’abord un fichier dlldata. c existant, et si le fichier est introuvable, un nouveau fichier dlldata. c est créé.</span><span class="sxs-lookup"><span data-stu-id="3b317-107">Each MIDL compiler run for COM interfaces looks for an existing dlldata.c file first, and if the file is not found, a new dlldata.c file is created.</span></span> <span data-ttu-id="3b317-108">Si un fichier dlldata. c est trouvé, des informations sur l’IDL actuel sont ajoutées (si absentes) ou remplacées.</span><span class="sxs-lookup"><span data-stu-id="3b317-108">If a dlldata.c file is found, information about the current IDL is added (if absent) or replaced.</span></span>

<span data-ttu-id="3b317-109">Le fichier d’inscription de l’interface est généré ou mis à jour en toute sécurité dans un environnement multiprocesseur, car les compilations MIDL parallèles ne peuvent pas écrire dans le fichier en même temps.</span><span class="sxs-lookup"><span data-stu-id="3b317-109">The interface registration file is safely generated or updated in a multiprocessor environment because parallel MIDL compiles are prevented from writing to the file at the same time.</span></span> <span data-ttu-id="3b317-110">Étant donné que tout fichier dlldata. c peut être marqué comme étant en lecture seule par l’environnement de génération ou l’utilisateur, le compilateur MIDL implémente une approche du délai d’attente pour attendre un fichier qu’il ne peut pas ouvrir et émet un message d’erreur approprié si le délai d’attente expire.</span><span class="sxs-lookup"><span data-stu-id="3b317-110">Because any dlldata.c file can be marked as read-only by either the build environment or the user, the MIDL compiler implements a timeout approach to waiting on a file it cannot open, and issues an appropriate error message if the timeout expires.</span></span>

<span data-ttu-id="3b317-111">Le nom par défaut du fichier d’inscription de l’interface généré à partir d’un fichier d’entrée est dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="3b317-111">The default name for the interface registration file generated from an input file is dlldata.c.</span></span> <span data-ttu-id="3b317-112">Le commutateur du compilateur MIDL [**/dlldata**](-dlldata.md) peut être utilisé pour remplacer le nom par défaut du fichier.</span><span class="sxs-lookup"><span data-stu-id="3b317-112">The [**/dlldata**](-dlldata.md) MIDL compiler switch can be used to override the default name of the file.</span></span> <span data-ttu-id="3b317-113">Le remplacement du nom par défaut du fichier d’inscription de l’interface est particulièrement utile lorsque certains fichiers IDL empaquetés dans un fichier binaire commun résident dans des répertoires différents.</span><span class="sxs-lookup"><span data-stu-id="3b317-113">Overriding the default name of the interface registration file is especially useful when some IDL files packaged to a common binary reside in different directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b317-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b317-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b317-115">Génération et inscription d’une DLL proxy</span><span class="sxs-lookup"><span data-stu-id="3b317-115">Building and Registering a Proxy DLL</span></span>](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 