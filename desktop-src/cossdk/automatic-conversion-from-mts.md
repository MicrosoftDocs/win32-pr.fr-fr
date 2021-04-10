---
description: Conversion automatique à partir de MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversion automatique à partir de MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111050"
---
# <a name="automatic-conversion-from-mts"></a><span data-ttu-id="4dc2d-103">Conversion automatique à partir de MTS</span><span class="sxs-lookup"><span data-stu-id="4dc2d-103">Automatic Conversion from MTS</span></span>

<span data-ttu-id="4dc2d-104">La conversion automatique se produit en deux étapes, comme suit :</span><span class="sxs-lookup"><span data-stu-id="4dc2d-104">Automatic conversion occurs in two steps, as follows:</span></span>

1.  <span data-ttu-id="4dc2d-105">Pendant l’installation de Windows.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-105">During Windows setup.</span></span> <span data-ttu-id="4dc2d-106">La conversion est gérée par le processus d’installation de Windows via l’utilitaire MTSTOCOM.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-106">The conversion is handled by the Windows setup process through the MTSTOCOM utility.</span></span>
    > [!Note]  
    > <span data-ttu-id="4dc2d-107">Si l’étape 1 échoue, une partie ou la totalité des packages MTS peut avoir été convertie, mais certaines propriétés peuvent être manquantes.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-107">If step 1 fails, some or all of the MTS packages may actually have been converted but may be missing certain properties.</span></span> <span data-ttu-id="4dc2d-108">Dans ce cas, utilisez l’outil d’administration Services de composants pour vérifier tous les attributs.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-108">In this case, use the Component Services administrative tool to verify all attributes.</span></span> <span data-ttu-id="4dc2d-109">Les attributs MTS sont toujours présents sur l’ordinateur (dans le registre système de HKEY \_ local \_ machine \\ Microsoft \\ Transaction Server), mais ils sont accessibles uniquement par le biais de l’utilitaire regedit.exe.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-109">The MTS attributes will still be present on the computer (in the system registry at HKEY\_LOCAL\_MACHINE\\Microsoft\\Transaction Server) but will be accessible only through the regedit.exe utility.</span></span>

     

2.  <span data-ttu-id="4dc2d-110">Après le dernier redémarrage, avant l’affichage de la boîte de dialogue ouverture de session Windows.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-110">After the last reboot before the Windows logon dialog box is displayed.</span></span> <span data-ttu-id="4dc2d-111">L’étape 2 gère ces actions de conversion qui requièrent l’accès au réseau (principalement la création de membres de rôle).</span><span class="sxs-lookup"><span data-stu-id="4dc2d-111">Step 2 handles those conversion actions that require network access (primarily role member creation).</span></span>
    > [!Note]  
    > <span data-ttu-id="4dc2d-112">Si l’étape 2 échoue (en raison de défaillances temporaires du réseau ou du contrôleur de domaine), il est possible de réexécuter l’utilitaire de conversion MTSTOCOM un nombre quelconque de fois.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-112">If step 2 fails (due to temporary network or domain controller failures), it is possible to rerun the MTSTOCOM conversion utility any number of times.</span></span> <span data-ttu-id="4dc2d-113">Pour ce faire, à l’invite de commandes ou après avoir sélectionné **exécuter** dans le menu **Démarrer** , tapez la commande suivante : **% windir% \\ system32 \\mtstocom.exe**.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-113">To do this, at the command prompt or after selecting **Run** from the **Start** menu, type the following: **%windir%\\system32\\mtstocom.exe**.</span></span>

     

## <a name="mtstocom-log-file"></a><span data-ttu-id="4dc2d-114">Fichier journal MTSTOCOM</span><span class="sxs-lookup"><span data-stu-id="4dc2d-114">MTSTOCOM Log File</span></span>

<span data-ttu-id="4dc2d-115">L’utilitaire MTSTOCOM génère un fichier journal (MTSTOCOM. log) dans le répertoire Windows.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-115">The MTSTOCOM utility generates a log file (Mtstocom.log) in the Windows directory.</span></span> <span data-ttu-id="4dc2d-116">Ce fichier journal conserve un enregistrement de la conversion des packages MTS en applications COM+.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-116">This log file keeps a record of the conversion from MTS packages to COM+ applications.</span></span> <span data-ttu-id="4dc2d-117">Si des erreurs se sont produites pendant le processus de conversion, il est toujours judicieux de consulter le fichier journal pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-117">If there were any errors during the conversion process, it is always a good idea to check the log file for further information.</span></span> <span data-ttu-id="4dc2d-118">Le fichier journal intercepte les problèmes courants, tels qu’un utilisateur ou un mot de passe non valide.</span><span class="sxs-lookup"><span data-stu-id="4dc2d-118">The log file catches common problems, such as invalid user or password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dc2d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4dc2d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dc2d-120">Résultats et problèmes de conversion COM+</span><span class="sxs-lookup"><span data-stu-id="4dc2d-120">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="4dc2d-121">Conversion manuelle à partir de MTS</span><span class="sxs-lookup"><span data-stu-id="4dc2d-121">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="4dc2d-122">Bibliothèque d’administration MTS</span><span class="sxs-lookup"><span data-stu-id="4dc2d-122">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



