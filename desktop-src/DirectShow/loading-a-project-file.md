---
description: Chargement d’un fichier projet
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Chargement d’un fichier projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200739"
---
# <a name="loading-a-project-file"></a><span data-ttu-id="b7f7f-103">Chargement d’un fichier projet</span><span class="sxs-lookup"><span data-stu-id="b7f7f-103">Loading a Project File</span></span>

<span data-ttu-id="b7f7f-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="b7f7f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b7f7f-105">Pour charger un fichier projet, vous avez besoin de deux composants : l’analyseur XML et une chronologie vide.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-105">To load a project file, you need two components: the XML parser and an empty timeline.</span></span> <span data-ttu-id="b7f7f-106">L’analyseur XML lit un fichier de projet XML et crée chaque objet défini dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-106">The XML parser reads an XML project file and creates each object defined in the file.</span></span> <span data-ttu-id="b7f7f-107">Elle insère ensuite les objets dans la chronologie et définit tous les attributs de la chronologie, tels que la fréquence d’images par défaut.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-107">Then it inserts the objects into the timeline and sets any timeline attributes, such as the default frame rate.</span></span> <span data-ttu-id="b7f7f-108">L’exemple de code suivant charge un fichier.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-108">The following code example loads a file.</span></span>


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



<span data-ttu-id="b7f7f-109">L’analyseur expose l’interface [**IXml2Dex**](ixml2dex.md) , qui contient des méthodes pour le chargement et l’enregistrement des fichiers projet.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-109">The parser exposes the [**IXml2Dex**](ixml2dex.md) interface, which contains methods for loading and saving project files.</span></span> <span data-ttu-id="b7f7f-110">La chronologie expose l’interface [**IAMTimeline**](iamtimeline.md) , qui contient des méthodes pour manipuler la chronologie et créer des objets Timeline.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-110">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface, which contains methods for manipulating the timeline and creating new timeline objects.</span></span> <span data-ttu-id="b7f7f-111">Appelez la fonction **CoCreateInstance** pour créer chaque composant, comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-111">Call the **CoCreateInstance** function to create each component, as shown.</span></span> <span data-ttu-id="b7f7f-112">N’oubliez pas qu’en créant une nouvelle instance, vous incrémentez le décompte de références sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-112">Remember that by creating a new instance, you are incrementing the reference count on the interface.</span></span> <span data-ttu-id="b7f7f-113">Pour éviter les fuites de mémoire, libérez toujours une interface quand vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-113">To avoid memory leaks, always release an interface when you are through with it.</span></span> <span data-ttu-id="b7f7f-114">Dans cet exemple, le pointeur vers **IXml2Dex** n’est pas nécessaire pour d’autres choses. vous pouvez donc libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-114">In this example, the pointer to **IXml2Dex** is not needed for anything more, so you can release the interface.</span></span> <span data-ttu-id="b7f7f-115">Le pointeur vers **IAMTimeline** est toujours nécessaire pour afficher un aperçu de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-115">The pointer to **IAMTimeline** is still needed for previewing the timeline.</span></span>

<span data-ttu-id="b7f7f-116">La méthode [**IXml2Dex :: ReadXMLFile**](ixml2dex-readxmlfile.md) lit le fichier spécifié et remplit la chronologie avec les objets définis dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-116">The [**IXml2Dex::ReadXMLFile**](ixml2dex-readxmlfile.md) method reads the specified file and populates the timeline with the objects defined in the file.</span></span> <span data-ttu-id="b7f7f-117">Le nom de fichier est spécifié à l’aide d’une valeur **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="b7f7f-117">The file name is specified using a **BSTR** value.</span></span> <span data-ttu-id="b7f7f-118">Pour raccourcir l’exemple, le nom de fichier dans l’exemple est donné sous la forme d’une chaîne littérale.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-118">To shorten the example, the file name in the example is given as a literal string.</span></span> <span data-ttu-id="b7f7f-119">Normalement, vous l’obtenez à partir d’une boîte de dialogue Ouvrir un fichier ou d’un nom similaire.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-119">Normally, you obtain it from an Open File dialog or something similar.</span></span>

<span data-ttu-id="b7f7f-120">Si la méthode **ReadXml** réussit, elle retourne un code de réussite.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-120">If the **ReadXML** method is successful, it returns a success code.</span></span> <span data-ttu-id="b7f7f-121">Sinon, elle retourne un code d’erreur tel que VFW \_ E \_ format de fichier non valide \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b7f7f-121">Otherwise, it returns an error code such as VFW\_E\_INVALID\_FILE\_FORMAT.</span></span> <span data-ttu-id="b7f7f-122">Vérifiez toujours la valeur de retour, afin de gérer les conditions d’erreur normalement.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-122">Always check the return value, in order to handle error conditions gracefully.</span></span> <span data-ttu-id="b7f7f-123">Là encore, par souci de concision, l’exemple de code ne vérifie pas les erreurs.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-123">Again for brevity, the example code does not check for errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7f7f-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7f7f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7f7f-125">Chargement et affichage de l’aperçu d’un projet</span><span class="sxs-lookup"><span data-stu-id="b7f7f-125">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



