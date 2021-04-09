---
description: Le service de détection de script ELS est appelé détection de script Microsoft.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Détection de scripts Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114195"
---
# <a name="microsoft-script-detection"></a><span data-ttu-id="782f6-103">Détection de scripts Microsoft</span><span class="sxs-lookup"><span data-stu-id="782f6-103">Microsoft Script Detection</span></span>

<span data-ttu-id="782f6-104">Le service de détection de script ELS est appelé détection de script Microsoft.</span><span class="sxs-lookup"><span data-stu-id="782f6-104">The ELS script detection service is called Microsoft Script Detection.</span></span> <span data-ttu-id="782f6-105">Ce service permet aux applications de détecter les scripts dans lesquels le texte est écrit.</span><span class="sxs-lookup"><span data-stu-id="782f6-105">This service allows applications to detect the scripts in which text is written.</span></span> <span data-ttu-id="782f6-106">L’équivalent NLS (National Language Support) d’un service de détection de script est la fonction [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) .</span><span class="sxs-lookup"><span data-stu-id="782f6-106">The National Language Support (NLS) counterpart of a script detection service is the [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) function.</span></span> <span data-ttu-id="782f6-107">Toutefois, le service ELS récupère également les plages de texte qui appartiennent à chaque système d’écriture.</span><span class="sxs-lookup"><span data-stu-id="782f6-107">However, the ELS service additionally retrieves the text ranges that belong to each writing system.</span></span>

## <a name="input-to-microsoft-script-detection"></a><span data-ttu-id="782f6-108">Entrée de la détection de scripts Microsoft</span><span class="sxs-lookup"><span data-stu-id="782f6-108">Input to Microsoft Script Detection</span></span>

<span data-ttu-id="782f6-109">L’entrée du service de détection de script Microsoft est du texte UTF-16 pour lequel le service détermine des plages de scripts.</span><span class="sxs-lookup"><span data-stu-id="782f6-109">The input to the Microsoft Script Detection service is UTF-16 text for which the service determines script ranges.</span></span>

## <a name="output-of-microsoft-script-detection"></a><span data-ttu-id="782f6-110">Sortie de la détection de scripts Microsoft</span><span class="sxs-lookup"><span data-stu-id="782f6-110">Output of Microsoft Script Detection</span></span>

<span data-ttu-id="782f6-111">La sortie du service de détection de script Microsoft est un tableau de plages, chacune contenant une chaîne UTF-16 terminée par un caractère NULL avec le nom spécifié au format Unicode du système d’écriture associé.</span><span class="sxs-lookup"><span data-stu-id="782f6-111">The output of the Microsoft Script Detection service is an array of ranges, each containing a null-terminated UTF-16 string with the Unicode-specified name of the associated writing system.</span></span> <span data-ttu-id="782f6-112">Le service signale les caractères communs standard (ZYYY) et hérité (Qaai) comme appartenant à la plage de scripts précédente.</span><span class="sxs-lookup"><span data-stu-id="782f6-112">The service reports regular common (Zyyy) and inherited (Qaai) characters as belonging to the previous script range.</span></span> <span data-ttu-id="782f6-113">Le début des caractères communs et hérités sont signalés comme appartenant à la plage de scripts suivante.</span><span class="sxs-lookup"><span data-stu-id="782f6-113">Beginning common and inherited characters are reported as belonging to the next script range.</span></span> <span data-ttu-id="782f6-114">Si tous les caractères du texte d’entrée sont communs ou hérités, la sortie du service est une plage unique avec la chaîne vide en tant que données.</span><span class="sxs-lookup"><span data-stu-id="782f6-114">If all the characters in the input text are common or inherited, the output of the service is a single range with the empty string as its data.</span></span>

## <a name="microsoft-script-detection-operation"></a><span data-ttu-id="782f6-115">Opération de détection de script Microsoft</span><span class="sxs-lookup"><span data-stu-id="782f6-115">Microsoft Script Detection Operation</span></span>

<span data-ttu-id="782f6-116">Le service de détection de script Microsoft mappe les points de code appartenant à la plage commune au système d’écriture précédent.</span><span class="sxs-lookup"><span data-stu-id="782f6-116">The Microsoft Script Detection service maps the code points belonging to the common range to the preceding writing system.</span></span> <span data-ttu-id="782f6-117">Le service peut également mapper les points de code au système d’écriture suivant si les points de code sont au début de la chaîne d’entrée.</span><span class="sxs-lookup"><span data-stu-id="782f6-117">Alternatively, the service can map the code points to the next writing system if the code points are at the beginning of the input string.</span></span> <span data-ttu-id="782f6-118">L’application n’a pas à gérer la plage commune du tout.</span><span class="sxs-lookup"><span data-stu-id="782f6-118">The application does not have to deal with the common range at all.</span></span>

## <a name="microsoft-script-detection-guid"></a><span data-ttu-id="782f6-119">GUID de détection de script Microsoft</span><span class="sxs-lookup"><span data-stu-id="782f6-119">Microsoft Script Detection GUID</span></span>

<span data-ttu-id="782f6-120">Le GUID du service de Détection de langue Microsoft est déclaré dans Elssrvc. h, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="782f6-120">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a><span data-ttu-id="782f6-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="782f6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="782f6-122">À propos des services linguistiques étendus</span><span class="sxs-lookup"><span data-stu-id="782f6-122">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



