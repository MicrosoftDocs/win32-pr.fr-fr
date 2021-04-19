---
title: Pour ajouter des données de script à l’en-tête
description: Pour ajouter des données de script à l’en-tête
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media Format SDK, ajout de données de script aux en-têtes
- ASF (Advanced Systems Format), ajout de données de script aux en-têtes
- ASF (format de systèmes avancés), ajout de données de script aux en-têtes
- scripts, ajout de données aux en-têtes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106511065"
---
# <a name="to-add-script-data-to-the-header"></a><span data-ttu-id="6b4e9-107">Pour ajouter des données de script à l’en-tête</span><span class="sxs-lookup"><span data-stu-id="6b4e9-107">To Add Script Data to the Header</span></span>

<span data-ttu-id="6b4e9-108">Vous pouvez inclure des commandes de script dans l’en-tête d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-108">You can include script commands in the header of an ASF file.</span></span> <span data-ttu-id="6b4e9-109">Pour écrire des commandes de script dans l’en-tête au moment de l’encodage, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-109">To write script commands to the header at the time of encoding, perform the following steps.</span></span> <span data-ttu-id="6b4e9-110">Effectuez ces étapes avant d’appeler [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="6b4e9-110">Perform these steps prior to calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

1.  <span data-ttu-id="6b4e9-111">Obtenez un pointeur vers l’interface **IWMHeaderInfo** en appelant **IWMWriter :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-111">Obtain a pointer to the **IWMHeaderInfo** interface by calling **IWMWriter::QueryInterface**.</span></span>
2.  <span data-ttu-id="6b4e9-112">Ajoutez chaque commande de script souhaitée en appelant [**IWMHeaderInfo :: AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span><span class="sxs-lookup"><span data-stu-id="6b4e9-112">Add each desired script command by calling [**IWMHeaderInfo::AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span></span> <span data-ttu-id="6b4e9-113">Chaque appel prend les deux chaînes séparément et l’heure de présentation à utiliser pour la commande en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-113">Each call takes the two strings separately and the presentation time to be used for the command as parameters.</span></span>

<span data-ttu-id="6b4e9-114">Quand une application lit le fichier, elle doit récupérer toutes les commandes de script.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-114">When an application reads the file, it will need to retrieve all of the script commands.</span></span> <span data-ttu-id="6b4e9-115">Pour rechercher toutes les commandes de script dans l’en-tête d’un fichier, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-115">To find all script commands in the header of a file, perform the following steps.</span></span> <span data-ttu-id="6b4e9-116">Cette opération doit être effectuée avant de commencer la lecture.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-116">This should be done before starting playback.</span></span>

1.  <span data-ttu-id="6b4e9-117">Obtenez un pointeur vers l’interface **IWMHeaderInfo** de l’objet lecteur (ou un objet lecteur synchrone) en appelant la méthode **QueryInterface** d’une autre interface dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-117">Obtain a pointer to the **IWMHeaderInfo** interface of the reader object (or synchronous reader object) by calling the **QueryInterface** method of another interface in the object.</span></span>
2.  <span data-ttu-id="6b4e9-118">Récupérez le nombre total de scripts dans l’en-tête en appelant [**IWMHeaderInfo :: GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span><span class="sxs-lookup"><span data-stu-id="6b4e9-118">Get the total number of scripts in the header by calling [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span></span>
3.  <span data-ttu-id="6b4e9-119">Parcourez l’ensemble des scripts de l’en-tête un par un en utilisant des appels à [**IWMHeaderInfo :: GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span><span class="sxs-lookup"><span data-stu-id="6b4e9-119">Loop through all of the scripts in the header one at a time using calls to [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span></span>
4.  <span data-ttu-id="6b4e9-120">Créez une liste des heures de présentation afin que votre application puisse réagir aux commandes au moment opportun.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-120">Create a list of the presentation times so that your application can react to the commands at the appropriate time.</span></span>

> [!Note]  
> <span data-ttu-id="6b4e9-121">Lorsque vous utilisez DRM pour chiffrer un fichier, aucune commande de script ne peut avoir une heure de présentation de 0.</span><span class="sxs-lookup"><span data-stu-id="6b4e9-121">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6b4e9-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b4e9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b4e9-123">**Interface IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="6b4e9-123">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="6b4e9-124">**Interface IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="6b4e9-124">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="6b4e9-125">**Utilisation des commandes de script**</span><span class="sxs-lookup"><span data-stu-id="6b4e9-125">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




