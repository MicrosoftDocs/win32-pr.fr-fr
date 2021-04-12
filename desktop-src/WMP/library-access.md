---
title: Accès à la bibliothèque
description: Accès à la bibliothèque
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Lecteur Windows Media, bibliothèque
- Modèle objet du lecteur Windows Media, bibliothèque
- modèle objet, bibliothèque
- Windows Media Player Mobile, bibliothèque pour le modèle objet
- Contrôle ActiveX du lecteur Windows Media, bibliothèque pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, bibliothèque pour le modèle objet
- Contrôle ActiveX, bibliothèque pour le modèle objet
- Bibliothèque du lecteur Windows Media, accès
- bibliothèque, accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309978"
---
# <a name="library-access"></a><span data-ttu-id="a552c-112">Accès à la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a552c-112">Library Access</span></span>

<span data-ttu-id="a552c-113">Les propriétés et les méthodes du modèle objet du lecteur Windows Media qui accèdent à la bibliothèque requièrent un accès en lecture seule ou en lecture/écriture à la base de données.</span><span class="sxs-lookup"><span data-stu-id="a552c-113">Properties and methods of the Windows Media Player object model that access the library require either read-only or read/write access to the database.</span></span> <span data-ttu-id="a552c-114">La bibliothèque contient des informations que certains utilisateurs veulent conserver privées et qui doivent être accessibles ou modifiés uniquement avec leur consentement.</span><span class="sxs-lookup"><span data-stu-id="a552c-114">The library contains information that some users want to keep private and that should be accessed or altered only with their consent.</span></span>

<span data-ttu-id="a552c-115">Pour le lecteur Windows Media série 9 ou version ultérieure, vous pouvez déterminer par programmation le niveau d’accès.</span><span class="sxs-lookup"><span data-stu-id="a552c-115">For Windows Media Player 9 Series or later, you can programmatically determine access level.</span></span> <span data-ttu-id="a552c-116">Pour déterminer le niveau d’accès actuel accordé à votre code, récupérez les *paramètres*. propriété **mediaAccessRights** .</span><span class="sxs-lookup"><span data-stu-id="a552c-116">To determine the current level of access granted to your code, retrieve the *Settings*.**mediaAccessRights** property.</span></span> <span data-ttu-id="a552c-117">Cette propriété retourne « None », « Read » ou « Full » (lecture/écriture).</span><span class="sxs-lookup"><span data-stu-id="a552c-117">That property returns "none", "read", or "full" (read/write).</span></span> <span data-ttu-id="a552c-118">Pour demander des droits d’accès spécifiques, appelez les *paramètres*. méthode **requestMediaAccessRights** , en passant un paramètre qui spécifie le niveau que vous demandez.</span><span class="sxs-lookup"><span data-stu-id="a552c-118">To request specific access rights, call the *Settings*.**requestMediaAccessRights** method, passing a parameter that specifies the level you are requesting.</span></span> <span data-ttu-id="a552c-119">La méthode affiche un message à l’utilisateur expliquant le niveau d’accès demandé et retourne une valeur **booléenne** indiquant si l’accès a été accordé.</span><span class="sxs-lookup"><span data-stu-id="a552c-119">The method displays a message to the user explaining the requested level of access, and returns a **Boolean** value indicating whether the access was granted.</span></span>

<span data-ttu-id="a552c-120">Certains droits d’accès sont accordés automatiquement en fonction de l’emplacement d’exécution de votre code par rapport à l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a552c-120">Certain access rights are granted automatically depending on where your code is running relative to the user's computer.</span></span>

-   <span data-ttu-id="a552c-121">Si votre page Web ou votre programme se trouve sur l’ordinateur de l’utilisateur, les droits d’accès complets sont accordés par défaut.</span><span class="sxs-lookup"><span data-stu-id="a552c-121">If your webpage or program is located on the user's computer, full access rights are granted by default.</span></span>
-   <span data-ttu-id="a552c-122">Les pages Web ont un accès en lecture à *Player*. **currentMedia**, *Player*. **currentPlaylist** et *Media*. **sourceURL** lorsque la page Web se trouve dans une zone de sécurité Internet Explorer qui est identique ou moins restreinte à la zone de sécurité de l’élément multimédia ou de la sélection.</span><span class="sxs-lookup"><span data-stu-id="a552c-122">Web pages have read access to *Player*.**currentMedia**, *Player*.**currentPlaylist**, and *Media*.**sourceURL** when the webpage is located in an Internet Explorer security zone that is the same as or less restricted than the security zone of the media item or playlist.</span></span>

    <span data-ttu-id="a552c-123">Du moins limité au plus restreint, les zones de sécurité sont la zone **approuvée** (y compris l’ordinateur local de l’utilisateur), la zone **Intranet local** , la zone **Internet** et la zone **restreinte** .</span><span class="sxs-lookup"><span data-stu-id="a552c-123">Ranging from least restricted to most restricted, the security zones are the **Trusted** zone (including the user's local computer), the **Local intranet** zone, the **Internet** zone, and the **Restricted** zone.</span></span>

    <span data-ttu-id="a552c-124">Par exemple, une page Web dans la zone **Intranet local** dispose de droits d’accès complets à *Player*. **currentMedia** lorsque l’élément multimédia correspondant se trouve sur l’intranet local ou sur Internet, mais que les droits d’accès doivent être demandés pour les éléments multimédias situés sur l’ordinateur local d’un utilisateur ou sur un site Web dans la zone **approuvée** .</span><span class="sxs-lookup"><span data-stu-id="a552c-124">For example, a webpage in the **Local intranet** zone has full access rights to *Player*.**currentMedia** when the corresponding media item is on the local intranet or the Internet, but access rights must be requested for media items located on a user's local computer or on a website in the **Trusted** zone.</span></span>

<span data-ttu-id="a552c-125">Vous devez tester votre application Web ou Windows dans toutes les zones de sécurité qu’elle peut rencontrer.</span><span class="sxs-lookup"><span data-stu-id="a552c-125">You should test your Web-based or Windows-based application in all of the security zones it may encounter.</span></span> <span data-ttu-id="a552c-126">L’application doit être conçue pour gérer correctement le refus d’une demande d’accès.</span><span class="sxs-lookup"><span data-stu-id="a552c-126">The application should be designed to handle denial of an access request correctly.</span></span>

<span data-ttu-id="a552c-127">Les versions du modèle objet du lecteur Windows Media antérieures à Windows Media Player 9 n’incluent pas **mediaAccessRights** ou **requestMediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="a552c-127">Windows Media Player object model versions prior to Windows Media Player 9 Series do not include **mediaAccessRights** or **requestMediaAccessRights**.</span></span> <span data-ttu-id="a552c-128">Ces versions antérieures du lecteur Windows Media permettent à l’utilisateur de définir des niveaux d’accès à l’aide de la boîte de dialogue **options** .</span><span class="sxs-lookup"><span data-stu-id="a552c-128">These earlier versions of Windows Media Player enable the user to set access levels using the **Options** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a552c-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a552c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a552c-130">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="a552c-130">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="a552c-131">**Utilisation de la bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="a552c-131">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




